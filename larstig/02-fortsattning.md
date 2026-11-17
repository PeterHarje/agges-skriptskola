# Nivå 2 – Fortsättning

[← Till skriptskolan](../README.md) · [← Nivå 1](01-nyborjare.md) · [Nivå 3 →](03-fordjupning.md)

**Förkunskaper:** Du förstår variabler och villkor.  
**Ungefärlig studietid:** 3–5 korta pass.

## Kunskapsmål

När du är klar ska du förstå och kunna ändra en enkel funktion, följa hur data skickas vidare, hantera fel och köra ett litet automatiskt test i **egen testmiljö**.

## Steg A – Funktioner

Läs `function` och `param` i [PowerShell](../01-powershell.md). Läs `def` och `return` i [Python](../03-python-grunder.md).

**Övning:** Gör om funktionen som dubblerar ett tal så att den tredubblar det. Vilka rader måste ändras?

## Steg B – Data som flyttas mellan steg

Läs om `|` och `$_` i [PowerShell](../01-powershell.md), och om dictionaries/JSON i [Python](../03-python-grunder.md).

**Övning:** Beskriv vart datan kommer från och vart den tar vägen i ett kodexempel.

## Steg C – När något går fel

Läs `try/catch` i PowerShell och `raise/except` i Python. Ett tydligt felmeddelande är ofta bättre än att programmet gissar.

**Övning:** Beskriv vad användaren bör få veta när ett program försöker läsa en fil som inte finns.

## Steg D – Små automatiska tester

Följ `unittest`-exemplet i [Pythonkapitlet](../03-python-grunder.md). Använd en **egen testkatalog**, aldrig en produktionsserver.

**Övning:** Lägg till ett test som provar ett negativt tal.

### Självtest

- Vet jag skillnaden mellan en funktion och ett vanligt anrop?
- Vet jag hur man testar både ett lyckat fall och ett felaktigt?
- Kan jag förklara varför ett test som förväntar sig ett fel ändå kan vara grönt?

[Nästa: Nivå 3 – Fördjupning →](03-fordjupning.md)
