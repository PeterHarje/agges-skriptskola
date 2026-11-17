# För lärare, studiecirklar och studiegrupper

[← Till skriptskolans startsida](README.md) · [Börja med nivå 0](larstig/00-borja-har.md)

**AggEs lättförståeliga skriptskola** är ett öppet undervisningsmaterial, uppbyggt för att kunna användas i egen takt, i par eller i en lärarledd grupp. Det är **inte en officiellt godkänd kursplan eller certifiering**. Anpassa innehåll, tidsåtgång och tekniska miljöer till deltagarnas behov.

## Pedagogisk idé

Målet är att deltagaren ska kunna säga: **”För sjutton gubbar – jag förstår ju varför det fungerar!”** Inte bara kopiera kod, utan kunna läsa den, förklara den och bedöma vad den får göra.

Uppmuntra nyfikenhet, humor och praktisk problemlösning. Låt gärna eleverna välja en väg – PowerShell på Windows, Linuxterminalen eller Python – och jämföra språken senare.

## Nivåer och bedömning

| Nivå | Förkunskapskrav | Visat kunnande | Exempel på uppgift |
| --- | --- | --- | --- |
| [0. Börja här](larstig/00-borja-har.md) | Inga | Känner igen kommando, variabel, villkor | Förklara tre rader kod muntligt |
| [1. Nybörjare](larstig/01-nyborjare.md) | Nivå 0 eller motsvarande | Läser ett villkor och skiljer på läsande/skrivande | Förklara `if/else` och `Test-Path` |
| [2. Fortsättning](larstig/02-fortsattning.md) | Nivå 1 eller motsvarande | Kan ändra funktion och skriva enkelt test | Tredubbla ett tal och testa |
| [3. Fördjupning](larstig/03-fordjupning.md) | Nivå 2 eller motsvarande | Resonerar om integritet, behörighet och spårbarhet | Beskriv varför rätt SHA256 inte är ett godkännande |

Föreslagna tider är ungefärliga. Nivåerna är **pedagogiska riktmärken**, inte medicinska eller andra personbedömningar. En kunnig deltagare kan hoppa direkt till en lämplig nivå.

## Förslag: 45 minuter

1. **5 min:** välj ett begripligt vardagsproblem (t.ex. ”finns filen?”).
2. **10 min:** läs kod tillsammans och gissa resultatet innan körning.
3. **15 min:** testa i en separat, ofarlig övningsmiljö.
4. **10 min:** ändra ett värde eller ett villkor och förklara skillnaden.
5. **5 min:** deltagarna berättar vad de förstått och vad de fortfarande undrar över.

## Anpassa för olika sätt att lära

- Dela upp i korta uppgifter med ett tydligt mål i taget.
- Låt deltagare växla mellan att **läsa, lyssna, testa och förklara**.
- Erbjud extra repetition utan tidspress; uppgifter kan tas i valfri takt.
- Visa exakta förväntade resultat och skillnaden mellan godkända och nekade fall.
- Låt deltagarna välja roliga projekt utifrån egna intressen: musikfiler, spel, text, datorreparation – med fiktiva eller egna testdata.
- Bedöm förståelse och säkerhetsomdöme, inte hur snabbt någon skriver på tangentbordet.

## Klassrumssäkerhet

Använd skolans eller elevens **egna övningsdatorer eller testcontainrar**, med rätt tillstånd. Dela inte produktionsnycklar, personuppgifter, lösenord eller verkliga nätverksinterna konfigurationer. Börja med läsande kod och diskutera först vad ett skrivande kommando skulle innebära.

Ett grönt automatiskt test visar att just det testet passerat, inte att all möjlig användning är säker. Skilj också mellan ett undervisningsexempel och ett driftklart system.

## Kunskapskontroll som går att visa upp

Be deltagaren lämna in en kort anteckning med:

- **Jag ville undersöka:** vilket problem?
- **Koden gör:** förklara en eller flera rader med egna ord.
- **Jag förväntade mig:** vad skulle hända?
- **Det hände faktiskt:** resultatet i testmiljön.
- **Jag har lärt mig:** en ny sak.
- **Nästa fråga:** vad vill jag förstå bättre?

Det ger en enkel, spårbar portfolio utan att elever behöver dela sina privata datorer eller personuppgifter.

## Förslag på vidareutveckling

Framtida kapitel kan innehålla frivilliga elevprojekt, separat facit, lektions-PDF, övningsfiler med dummydata och en instruktion för lärare som vill bidra. **De delarna är ännu inte producerade.**

Materialet går att läsa i det publika GitHub-repot. En uttrycklig licens för kopiering, bearbetning och återpublicering behöver väljas; publikt läsbart betyder inte automatiskt fri återanvändning.

[Läs om filosofin bakom Junkpile](om-junkpile.md) · [Till innehållsförteckningen](README.md)
