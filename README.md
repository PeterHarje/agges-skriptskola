# AggEs lättförståeliga skriptskola

### AggE's Script School for Easy Learning

### Från nyfikenhet till förståelse – en praktisk lärobok om PowerShell, Linux, Python och säker programmering

**En öppen, svenskspråkig programmeringsskola från Junkpile Tech Studio · Version 0.1 · november 2026**

> **Grundidé:** Det räcker inte att kod fungerar. Vi ska också kunna förstå **varför** den fungerar, **vad** den får göra och **hur** vi verifierar resultatet.

Det här är en växande, svenskspråkig kodbok för personer som är nyfikna på programmering, från första försöket till praktiskt säkerhetsarbete. Vi använder ofarliga, verklighetsnära exempel utan lösenord, produktionsnycklar eller instruktioner för att ändra någon verklig produktionsserver.

Boken är skriven för att gå att läsa **uppifrån och ned** eller slå upp som referens. Varje kapitel har korta exempel, förklaringar av kommandon, varför vi använder dem och små övningar.

---

## Innehållsförteckning

| Kapitel | Ämne | Vad du lär dig |
| --- | --- | --- |
| [01. PowerShell – förstå vad kommandot gör](01-powershell.md) | Windows/PowerShell | Variabler, Test-Path, if/else, funktioner, pipeline och felhantering |
| [02. Linux – läsande kontroller](02-linux-terminal.md) | Linux/terminal | clear, sed, grep, stat, rättigheter och filsystem |
| [03. Python – begriplig kod och testning](03-python-grunder.md) | Python | Funktioner, JSON, SHA256, undantag och unittest |
| [04. Säkerhet, Git och dokumentation](04-sakerhet-och-git.md) | Arbetsmetod | Git, commits, CI, minsta behörighet, fail-closed och överlämning |
| [05. Kommandoindex och ordlista](05-ordlista.md) | Snabbreferens | Alfabetiskt orienterad begreppssamling och länkar till kodexempel |

## Så använder du boken

**Om du är nybörjare:** Börja med PowerShell eller Linux och prova de små, läsande kommandona i en egen testmiljö. Läs ett kodblock i taget och försök formulera med egna ord vad varje rad gör.

**Om du redan programmerar:** Använd kapitlen som snabb uppslagsbok. Jämför framför allt hur vi hanterar fel, filrättigheter, verifiering och gränsen mellan observation och exekvering.

**Om du undervisar eller delar:** Länka till det kapitel som passar. Exemplen innehåller inga verkliga hemligheter. Kontrollera dock alltid programversioner, lokala rättigheter och miljö innan någon kör ett kommando.

### Vårt arbetssätt: en tråd i taget

När ett projekt innehåller hundra idéer behöver vi inte göra allt samtidigt. Vi arbetar enligt samma mönster:

1. **Förstå** vad problemet faktiskt är.
2. **Läs och undersök** innan vi skriver eller ändrar.
3. **Förklara** vad varje viktigt kommando gör.
4. **Testa i isolerad miljö** med testdata.
5. **Dokumentera** vad som är verifierat och vad som återstår.
6. **Ändra produktion endast med tydlig plan och lämpliga rättigheter.**

En lyckad testkörning är värdefull, men den är inte ett universellt bevis på säkerhet.

## Återkommande struktur för nya kapitel

Varje nytt kapitel bör innehålla: mål, när kommandot används, körbart litet exempel, rad-för-rad-förklaring, risker/rättigheter, en eller två egna övningar och en länk till nästa kapitel. Nya kommandon ska läggas till i [ordlistan](05-ordlista.md) och i tabellen här.

**Planerade framtida ämnen:** PowerShell-objekt och moduler, regex och loggfelsökning, Bash-villkor och loopar, systemd som begrepp, JSON/API:er, Git-arbetsflöden, SQLite, enhetstester och säker filhantering. Dessa kapitel är **ännu inte skrivna**.

## Om säkerhet och användning

- Övningarna är avsedda för **egna testmiljöer**, inte för okontrollerade ändringar på produktion.
- Exempel får inte innehålla faktiska API-nycklar, signeringsnycklar eller känsliga personuppgifter.
- Kommandon och beteenden kan skilja sig mellan operativsystem och versioner. Läs alltid dokumentationen för din miljö.
- Det är tillåtet att läsa materialet i ett publikt repo. Villkor för vidare kopiering, ändring och återpublicering bestäms av projektets licens när den har valts.

### Projektanknytning

Kodboken är inspirerad av praktiskt arbete med programmering och felsökning, men är **undervisningsmaterial, inte en driftsättningsmanual**. Teknikexemplen är förenklade för lärande och ska inte ersätta säkerhetsgranskning.

---

**Bokens löfte:** Vi ska inte bara kopiera ett kommando – vi ska förstå det. ❤️🤘

**Språk:** Svenska, med engelska programmeringstermer och en engelsk undertitel. Licens för återanvändning fastställs innan extern publicering.
