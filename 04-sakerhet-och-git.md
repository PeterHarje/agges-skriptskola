# Kapitel 4 – Säkerhet, Git och dokumentation

[← Innehållsförteckning](README.md) · [← Python](03-python-grunder.md) · [Ordlista →](05-ordlista.md)

**Mål:** kunna skilja mellan kod, test, driftsättning och dokumentation. Förstå varför vi använder GitHub som projektminne.

## Git på två minuter

Git är ett versionshanteringssystem: när en fil ändras kan vi dokumentera **vad som ändrades, varför och av vem**. GitHub kan lagra Git-projekt och köra automatiska tester, men GitHub och Git är inte samma sak.

| Begrepp | Förklaring |
| --- | --- |
| Repository (repo) | Mapp med kod och historik |
| Commit | Sparad ändring med beskrivning |
| Branch | Separat utvecklingsspår |
| Diff | Visar vilka rader som ändrats |
| Pull request | Förslag till ändring som kan granskas innan sammanslagning |
| CI (Continuous Integration) | Automatisk körning av tester vid kodändringar |

## Läskommando med Git

I en **egen klonad testkopia** av ett Git-repo kan du köra:

~~~bash
git status
git log --oneline -5
git diff
~~~

- `git status` visar vilka lokala filer som ändrats.
- `git log --oneline -5` visar de fem senaste commitarna.
- `git diff` visar ännu ej staged ändringar. För tidigare sparade ändringar behövs annan diff-jämförelse.

De här kommandona **läser** status och historik. De publicerar inte något.

## Vad betyder det att ett test är grönt?

Tänk dig ett förenklat program som ska ta emot uppgifter säkert:

1. **Staging:** ta emot opålitliga data i separat katalog.
2. **Preflight:** kontrollera format, filnamn och storleksgränser.
3. **Snapshot:** kopiera exakt kontrollerade bytes till privat plats och verifiera igen.
4. **Godkännande:** en behörig person måste fatta ett separat beslut.
5. **Engångsspärr:** samma godkännande får inte användas om och om igen.
6. **Signering:** skapa HMAC lokalt och skydda nyckeln.
7. **Publicering:** lägg ett komplett jobb i kön utan att skriva över något.

Det här är ett **pedagogiskt exempel**, inte ett färdigt program. Att GitHub Actions visar grönt betyder att de testfall som faktiskt körts har passerat i testmiljön. Det bevisar **inte** att hela systemet är säkert eller installerat på en produktionsserver.

## Fyra enkla säkerhetsprinciper

**Minsta behörighet.** Ett program ska bara ha åtkomst till det som krävs. Exempel: ett konto som hämtar filer ska inte också få läsa en privat signeringsnyckel.

**Fail closed.** Om något är oklart eller saknas ska en riskfylld åtgärd stoppas, inte gissas fram. Exempel: saknad godkänd signatur betyder inget körbart jobb.

**Separera läsning och skrivning.** Vi undersöker först med `stat`, `findmnt` och `test -r`. Kommando som `chmod`, `chown` och `mv` ändrar systemet och planeras separat.

**Testa utan produktion.** Ny kod körs först med dummydata och under testkonto i en isolerad miljö. Skyddad kod kan ändå innehålla buggar.

## Så skriver du en bra överlämning

Använd den här enkla strukturen efter ett viktigt arbetssteg:

~~~text
Datum:
Projekt:
Mål:
Vad gjordes:
Exakta testresultat:
Vad är verifierat:
Vad är fortfarande okänt:
Risker och saker vi INTE ändrat:
Nästa enda säkra steg:
~~~

Det här är skillnaden mellan *”det verkar fungera”* och en spårbar teknisk undersökning.

## Tänk på secrets

Lägg aldrig lösenord, API-nycklar, HMAC-nycklar, privata konfigurationsfiler eller produktionskontots cookies i GitHub eller offentliga kodexempel. Visa hellre rättigheter och status än filinnehåll. Om en hemlighet råkar exponeras ska den normalt betraktas som komprometterad och bytas enligt systemets rutin.

## Övningar

1. Beskriv med egna ord skillnaden mellan en **commit** och en **testkörning**.
2. Varför ger rätt SHA256 inte automatiskt tillåtelse att köra en fil?
3. Förklara varför `renameat2(RENAME_NOREPLACE)` är användbart när ett befintligt jobb inte får skrivas över. **Du ska inte köra något; beskriv bara principen.**
4. Skriv en överlämning för ett eget litet PowerShell-experiment och skilj tydligt på *gjort*, *testat* och *kvar*.

[← Index](README.md) · [Nästa: Ordlista →](05-ordlista.md)
