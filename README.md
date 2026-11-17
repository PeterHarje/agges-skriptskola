# AggEs lättförståeliga skriptskola

### AggE's Script School for Easy Learning

**Lär dig förstå skript – från första raden till säkrare programmering.**

En öppet läsbar, svenskspråkig skriptskola från **Junkpile Tech Studio**. Här ska ingen behöva känna sig dum för att ett kommando ser obegripligt ut. Vi tar en tråd i taget: **vad gör det, varför gör det så, hur provar jag själv och hur vet jag att det fungerade?**

> **Målet:** Att någon provar ett exempel och utbrister: **”För sjutton gubbar … det fungerar ju! Jag fattar varför!”** 😄

**Version:** 0.2 – november 2026 · **Språk:** svenska med vanliga engelska kodtermer · **Format:** Markdown på GitHub

## Välj din kunskapsnivå

Du får börja var som helst. Om något känns för svårt, gå tillbaka en nivå; om det känns enkelt, hoppa vidare. Tiderna är uppskattningar, inte krav.

| Nivå | För dig som … | Det här övar du på | Starta här |
| --- | --- | --- | --- |
| **0 · Börja här** | aldrig programmerat | Vad är skript, kommando, variabel och villkor? | [Öppna nivå 0](larstig/00-borja-har.md) |
| **1 · Nybörjare** | vill förstå små kodexempel | Variabler, `if/else`, läsande kommandon | [Öppna nivå 1](larstig/01-nyborjare.md) |
| **2 · Fortsättning** | kan grunderna och vill bygga vidare | Funktioner, data, felhantering, automatiska tester | [Öppna nivå 2](larstig/02-fortsattning.md) |
| **3 · Fördjupning** | vill förstå säkrare system och utveckling | SHA256, behörighet, Git, isolerade tester | [Öppna nivå 3](larstig/03-fordjupning.md) |

### Eller välj ett språk direkt

| Kapitel | Innehåll | Passar från |
| --- | --- | --- |
| [1. PowerShell](01-powershell.md) | Variabler, villkor, pipeline, funktioner och felhantering | **Nivå 1** |
| [2. Linux och terminalen](02-linux-terminal.md) | `clear`, `pwd`, `ls`, `stat`, `grep`, rättigheter | **Nivå 1** |
| [3. Python](03-python-grunder.md) | Funktioner, JSON, SHA256, undantag och `unittest` | **Nivå 1–2** |
| [4. Säkerhet och Git](04-sakerhet-och-git.md) | Git, commits, CI, minsta behörighet, dokumentation | **Nivå 2–3** |
| [5. Kommandoindex och ordlista](05-ordlista.md) | Slå upp begrepp och hitta tillbaka till exemplen | **Alla nivåer** |

Du behöver **inte** lära dig alla språk. Välj det som passar din dator eller ditt intresse.

## För skolan, studiecirkeln eller den som hjälper en vän

Vi vill göra det lätt att använda skriptskolan tillsammans. Varje nivå har **förkunskaper, lärandemål, praktiska uppgifter och självtest**.

[Läs lärarhandledningen](for-larare.md) för ett lektionsupplägg, förslag till bedömning och sätt att anpassa tempot efter olika deltagare. Det är ett öppet undervisningsunderlag, **inte en officiell kursplan eller certifiering**.

## Varför heter det Junkpile?

> **”Där du ser tre trasiga datorer ser vi en hel.”**

Det sammanfattar vår tro på **återbruk före onödiga nyinköp**. Går något att felsöka, reparera eller använda igen är det värt att undersöka. Ibland kan fungerande delar från flera trasiga datorer bli en fungerande dator. Samma idé gäller för kod: förstå vad som redan fungerar, ändra en sak och testa igen.

**Junkpile Tech Studio** är ett planerat teknik- och skapandeföretag där återbruk, programmering, AI och praktisk hjälp hör ihop.

**Frankenstein Junkpile** är musikprojektet där vi förenar rock, industriella och elektroniska ljud, science fiction och teknikglädje. Vår fiktiva robotfigur **AggE/Algot Rustborn** är en del av det kreativa universumet – och har fått låna sitt namn till skriptskolan.

[Läs hela berättelsen om Junkpile, återbruket och musiken](om-junkpile.md).

## Så lär vi oss: en tråd i taget

1. **Förstå** problemet innan du försöker lösa det.
2. **Läs** vad kommandot gör och vilka rättigheter det kräver.
3. **Gissa** resultatet innan du provar.
4. **Testa** med ofarliga exempel i en egen testmiljö.
5. **Jämför** resultatet med det du väntade dig.
6. **Förklara** med egna ord och dokumentera det du lärt dig.

Om du kan förklara något för en annan människa har du ofta förstått det på riktigt.

## Säkerhet

- Kör aldrig okända skript som administratör bara för att det står så i ett exempel.
- Lärobokens kod ska provas med testdata – **inte på arbetsplatsens eller skolans produktionssystem**.
- Publicera inte lösenord, API-nycklar, privata filer eller andra personers uppgifter.
- Ett grönt test betyder att **just det testet** lyckades. Det är inte ett bevis på att all kod är säker.
- Följ regler och behörigheter på den dator där du arbetar.

## Hur boken växer

Nya kapitel ska **alltid märkas med kunskapsnivå** och länkas från både den här startsidan och [ordlistan](05-ordlista.md) när nya kommandon introduceras.

Vi planerar bland annat fortsättningar om PowerShell-objekt, loggfelsökning, Bash-loopar, JSON/API:er, SQLite och mer automatiserad testning. **Det är planerat material, inte färdigskrivna kapitel.**

[Läs principerna för att bidra till skriptskolan](BIDRA.md).

**Delning:** Repot är offentligt och kan läsas av alla. En uttrycklig licens för vidarekopiering, bearbetning och återpublicering ska väljas; publik åtkomst innebär inte automatiskt fri licens.

---

**Vi ska inte bara kopiera ett kommando – vi ska förstå det.** ❤️🤘
