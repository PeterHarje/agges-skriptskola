# Kapitel 5 – Snabbordlista och kommandoindex

[← Innehållsförteckning](README.md) · [← Säkerhet och Git](04-sakerhet-och-git.md)

**Nivå:** Alla. **Förkunskaper:** inga. Använd uppslagsdelen när som helst under din [lärstig](larstig/00-borja-har.md).

Här finns korta förklaringar och länkar till lärobokens praktiska exempel. Alla kapitel går att läsa separat.

## PowerShell

| Ord / kommando | Kort förklaring | Kapitel |
| --- | --- | --- |
| `$variabel` | Namngivet värde | [PowerShell](01-powershell.md) |
| `Get-Help` | Hjälp och exempel | [PowerShell](01-powershell.md) |
| `Test-Path` | Finns en sökväg? | [PowerShell](01-powershell.md) |
| `Get-FileHash` | Beräkna filens hash | [PowerShell](01-powershell.md) |
| `if / else` | Välj väg utifrån villkor | [PowerShell](01-powershell.md) |
| `try / catch` | Hantera fel öppet | [PowerShell](01-powershell.md) |
| `function / param` | Återanvänd kod och ge indata | [PowerShell](01-powershell.md) |
| `| / $_` | Pipeline och aktuell post | [PowerShell](01-powershell.md) |

## Linux

| Ord / kommando | Kort förklaring | Kapitel |
| --- | --- | --- |
| `clear` | Rensa terminalbild | [Linux](02-linux-terminal.md) |
| `pwd` | Visa aktuell katalog | [Linux](02-linux-terminal.md) |
| `ls -la` | Lista filer och rättigheter | [Linux](02-linux-terminal.md) |
| `sed -n '1,40p'` | Visa ett radintervall | [Linux](02-linux-terminal.md) |
| `grep -n` | Sök text och visa radnummer | [Linux](02-linux-terminal.md) |
| `stat` | Visa filmetadata | [Linux](02-linux-terminal.md) |
| `test -r` | Kontrollera läsbarhet | [Linux](02-linux-terminal.md) |
| `findmnt -T` | Visa filsystemsmontering | [Linux](02-linux-terminal.md) |
| `runuser -u` | Kontrollera under annat konto (adminbehörighet krävs) | [Linux](02-linux-terminal.md) |

## Python

| Ord / kommando | Kort förklaring | Kapitel |
| --- | --- | --- |
| `def / return` | Funktion och returvärde | [Python](03-python-grunder.md) |
| `dict / JSON` | Nycklar och värden i dataformat | [Python](03-python-grunder.md) |
| `hashlib.sha256` | Fingeravtryck av bytes | [Python](03-python-grunder.md) |
| `raise / except` | Uttryckligt fel och felhantering | [Python](03-python-grunder.md) |
| `unittest` | Automatiska tester | [Python](03-python-grunder.md) |

## Begrepp i säker automatisering

| Begrepp | Kort förklaring |
| --- | --- |
| **Staging** | Avskild plats för ännu opålitliga data |
| **Manifest** | Beskrivning av ett jobb och dess tillhörande filer |
| **SHA256** | Kontrollsumma av bytes; inte ett operatörsgodkännande |
| **HMAC** | Kontroll av meddelandets autenticitet/integritet med en hemlig nyckel |
| **Snapshot** | En kontrollerad kopia av exakt det innehåll som granskats |
| **TOCTOU** | Risk för byte mellan kontrollen och själva användningen |
| **Replay** | Återanvändning av ett äldre meddelande eller godkännande |
| **Atomisk publicering** | Hela färdiga objektet blir synligt vid ett steg |
| **No-replace** | Ett redan existerande namn/objekt får inte skrivas över |
| **Dummy-nyckel** | Offentlig testnyckel som aldrig är produktionshemlig |
| **CI** | Automatiska tester som körs utanför utvecklarens dator |
| **Fail closed** | Stoppa riskfylld åtgärd när giltig kontroll saknas |

### Kom ihåg

En **grön testsvit** är ett gott tecken, inte ett slutligt säkerhetsintyg. En **känd hash** säger att innehåll matchar, inte att en person godkänt det. Och kod i GitHub är **inte automatiskt installerad** på någon server.

[← Index](README.md)
