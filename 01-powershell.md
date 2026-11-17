# Kapitel 1 – PowerShell: förstå vad kommandot gör

[← Innehållsförteckning](README.md) · [Linux →](02-linux-terminal.md)

**Nivå:** 1 – Nybörjare (funktioner och felhantering passar även nivå 2). **Förkunskaper:** inga om du börjar med variabler. [Lärstig nivå 1](larstig/01-nyborjare.md).

**Målet:** förstå vanliga PowerShell-konstruktioner och kunna förklara vad ett skript gör innan det körs. Exemplen nedan ändrar inga systeminställningar.

## Kommandon som består av verb och substantiv

| Kommando | Vad det gör | Ändrar filer? |
| --- | --- | --- |
| `Get-Help` | Visar hjälp och exempel | Nej |
| `Get-Command` | Hittar kommandon | Nej |
| `Test-Path` | Kontrollerar om en sökväg finns | Nej |
| `Get-Item` | Hämtar information om en fil eller katalog | Nej |
| `Get-Content` | Läser text från en fil | Nej |
| `Get-FileHash` | Beräknar en kontrollsumma för en fil | Nej |

~~~powershell
Get-Help Test-Path -Examples
Get-Command Get-FileHash
~~~

`Get-Help` förklarar hur kommandot används. `-Examples` visar färdiga exempel.

## Variabler och utskrifter

~~~powershell
$meddelande = "Hej från Junkpile!"
$antal = 3

Write-Output $meddelande
Write-Output ($antal * 2)
~~~

`$meddelande` är en variabel: ett namn som pekar på ett värde. `=` tilldelar värdet. `Write-Output` skickar värden vidare i PowerShells pipeline, medan `Write-Host` främst skriver direkt till skärmen.

## Villkor: if och else

~~~powershell
$plats = $env:TEMP

if (Test-Path -LiteralPath $plats -PathType Container) {
    Write-Output "Katalogen finns: $plats"
} else {
    Write-Output "Katalogen hittades inte."
}
~~~

- `Test-Path` frågar om sökvägen finns.
- `-LiteralPath` tolkar sökvägen bokstavligt (ingen jokerteckentolkning).
- `-PathType Container` kräver en katalog.
- `if` gör något om resultatet är sant; `else` hanterar det andra fallet.

**Säkerhetsnotis:** Att en fil finns innebär inte automatiskt att den är säker eller bör ändras.

## Pipeline och funktioner

~~~powershell
1..5 | ForEach-Object { $_ * 10 }
~~~

`1..5` ger talen 1–5, `|` skickar dem ett i taget vidare och `$_` syftar på det aktuella talet.

~~~powershell
function Get-Dubbel {
    param([int]$Tal)
    return ($Tal * 2)
}

Get-Dubbel -Tal 21
~~~

`function` bygger en återanvändbar del. `param` definierar indata. `return` lämnar resultatet (här 42).

## Felhantering

~~~powershell
$minFil = Join-Path $env:TEMP "saknas-i-detta-exempel.txt"

try {
    Get-Content -LiteralPath $minFil -ErrorAction Stop
} catch {
    Write-Warning "Det gick inte att läsa filen: $($_.Exception.Message)"
}
~~~

`try` försöker utföra en åtgärd och `catch` tar hand om fel. `-ErrorAction Stop` ser till att ett läsfel blir ett undantag som kan fångas.

## Övningar

1. Ändra `$antal` och se vad beräkningen skriver ut.
2. Ändra funktionen så att den tredubblar talet. Vilket funktionsnamn passar då?
3. Skriv en `if`-kontroll som berättar om din egen dokumentkatalog finns, utan att skapa något.

**Kom ihåg:** Titta på vilka sökvägar ett skript använder, vilka filer det läser, vilka rättigheter det kräver och om det kan skriva något innan du kör det.

[← Index](README.md) · [Nästa: Linux →](02-linux-terminal.md)
