# Nivå 3 – Fördjupning och projekttänk

[← Till skriptskolan](../README.md) · [← Nivå 2](02-fortsattning.md) · [Ordlista](../05-ordlista.md)

**Förkunskaper:** Du kan läsa små funktioner och förstå grundläggande testresultat.  
**Ungefärlig studietid:** 3–6 pass, gärna i grupp.

## Kunskapsmål

Du ska kunna förklara skillnaden mellan filintegritet och behörigt godkännande, läsa enkel Git-historik och beskriva varför kod testas innan den används i viktiga system.

## Steg A – Integritet och identitet

Läs om `hashlib.sha256` i [Pythonkapitlet](../03-python-grunder.md) och om säkerhetsgränser i [kapitel 4](../04-sakerhet-och-git.md).

**Resonera:** Om du och en angripare båda kan räkna ut samma SHA256 – varför är hashen inte ett bevis på vem som godkände filen?

## Steg B – Git och spårbarhet

Läs `git status`, `git log` och `git diff` i [Gitkapitlet](../04-sakerhet-och-git.md). Öva bara i ett eget övningsrepo.

**Resonera:** Varför behöver du veta både *vilken kod som kördes* och *vilka tester som kördes* när du felsöker?

## Steg C – Säkra förändringar

Studera *minsta behörighet*, *fail closed*, *isolerad testmiljö* och *dokumentation* i [kapitel 4](../04-sakerhet-och-git.md).

**Gruppövning:** Rita upp ett tänkt program som ska kontrollera en textfil. Markera vilka steg som bara läser och vilka som skulle kräva behörighet för att ändra något. Ingen verklig signering eller systemändring behövs.

## Steg D – Förklara för en annan

Välj ett litet exempel ur skriptskolan. Skriv en kort förklaring med rubrikerna **Vad**, **Varför**, **Risker**, **Hur testar vi?** och **Vad återstår?**

### Självtest

- Kan jag skilja mellan SHA256 och ett behörigt godkännande?
- Kan jag skilja mellan ett enhetstest och ett integrationstest?
- Kan jag förklara varför ett grönt test inte är ett löfte om total säkerhet?

**Efter denna nivå:** Du kan gärna bidra med förbättringsförslag eller skriva en egen nybörjarvänlig förklaring. Se [lärarhandledningen](../for-larare.md) om ni arbetar i grupp.

[← Startsida](../README.md)
