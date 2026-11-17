# Kapitel 2 – Linux: läsande kontroller på en server

[← Index](README.md) · [← PowerShell](01-powershell.md) · [Python →](03-python-grunder.md)

**Nivå:** 1 – Nybörjare. **Förkunskaper:** inga om du börjar med `clear`, `pwd` och `ls`. [Lärstig nivå 1](larstig/01-nyborjare.md).

**Målet:** förstå de Linux-kommandon vi använder när vi undersöker en server. Exemplen ska provas i en egen **testmiljö**, inte på någon produktionsserver utan en särskild plan.

## Hitta rätt

~~~bash
clear
pwd
ls -la
~~~

| Kommando | Betydelse |
| --- | --- |
| `clear` | Rensar terminalens synliga bild, inte loggar eller filer |
| `pwd` | Visar vilken katalog terminalen befinner sig i |
| `ls -la` | Visar filer, inklusive dolda, och deras rättigheter |

## Läs utan att ändra

~~~bash
clear
sed -n '1,40p' README.md
~~~

`sed -n` gör här en utskrift av raderna 1–40. `p` betyder ”skriv ut”. Filen ändras inte.

~~~bash
clear
grep -n 'TODO' README.md
~~~

`grep` söker efter ordet `TODO`, och `-n` skriver radnummer. Saknas filen får du felmeddelande.

**Viktigt:** Visa aldrig innehållet i signeringsnycklar, lösenordsfiler eller privata konfigurationsfiler i en chatt. Kontrollera endast filmetadata när skydd ska undersökas.

## Läs ägare och rättigheter

~~~bash
clear
stat -c '%A | %a | %U:%G | %n' README.md
~~~

| Kod | Visar |
| --- | --- |
| `%A` | Symboliska rättigheter, t.ex. `-rw-r--r--` |
| `%a` | Numeriskt rättighetsläge, t.ex. `644` |
| `%U:%G` | Ägare och grupp |
| `%n` | Filnamn |

Vanliga exempel: katalog `0700` tillåter normalt endast ägaren att gå in i den. Fil `0600` låter normalt bara ägaren läsa och skriva. Administratören/root kan ha särskild åtkomst; ACL och tjänstesandboxar kan påverka.

## Testa behörighet utan att visa filinnehåll

~~~bash
clear
test -r README.md && echo 'Läsbar' || echo 'Inte läsbar'
~~~

`test -r` kontrollerar läsbarhet för **aktuellt konto**. `&&` betyder ungefär ”om det lyckades”; `||` betyder här ”annars”.

För att kontrollera ett annat konto, med behörig administratör:

~~~bash
clear
runuser -u testkonto -- test -r /sokvag/till/fil
~~~

Det sista är ett **exempel**, inte en instruktion att prova med verkliga produktionskonton. Använd avsiktligt skapade testidentiteter.

## Kontrollera filsystemet

~~~bash
clear
findmnt -T /tmp -no TARGET,SOURCE,FSTYPE
~~~

`findmnt` visar monteringspunkten som innehåller `/tmp`, källan och filsystemstypen.

När två kataloger ska användas för en atomisk katalogflytt är det relevant att de ligger på samma filsystem. Det **ger inte** i sig tillstånd att skriva i katalogerna.

## Läsande kontra skrivande kommandon

| Undersökning | Ändring – kräver separat plan |
| --- | --- |
| `pwd`, `ls`, `stat`, `findmnt`, `grep`, `sed -n` | `mv`, `chmod`, `chown`, `install -d` |

Kommandot `install -d` skapar faktiskt en katalog och är därför en **riktig filsystemsändring**. Kontrollera alltid ägare och läge om du använder det i en egen övningsmiljö.

## Övningar

1. Använd `pwd` och `ls -la` i en egen testkatalog.
2. Kör `stat` på en ofarlig textfil. Beskriv symboliskt och numeriskt rättighetsläge.
3. Kör `findmnt -T /tmp -no TARGET,SOURCE,FSTYPE`. Kan du identifiera monteringspunkten?
4. Förklara varför `test -r` är lämpligare än att skriva ut innehållet i en privat nyckelfil.

[← Index](README.md) · [Nästa: Python →](03-python-grunder.md)
