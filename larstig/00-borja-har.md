# Nivå 0 – Börja här

[← Till skriptskolan](../README.md) · [Nästa: Nivå 1 →](01-nyborjare.md)

**För vem?** För dig som är helt ny eller vill börja om från början.  
**Förkunskaper:** Inga.  
**Ungefärlig studietid:** 20–40 minuter i egen takt.

## Vad är ett skript?

Ett skript är ett antal instruktioner som datorn utför. Det kan läsa information, räkna ut något eller hjälpa dig med uppgifter som du annars skulle göra för hand.

Vi börjar med **ofarliga, läsande exempel**. Vi övar inte på att ändra en riktig server.

## Tre byggstenar

- **Kommando** – en instruktion, som `Get-Help` i PowerShell eller `pwd` i Linux.
- **Variabel** – ett namn på ett värde, som `$antal` eller `antal`.
- **Villkor** – ett val: ”om det här stämmer, gör så här”.

## Välj EN startväg

- **Windows:** [PowerShell, kapitel 1](../01-powershell.md).
- **Linux:** [Terminalen, kapitel 2](../02-linux-terminal.md).
- **Allmän programmering:** [Python, kapitel 3](../03-python-grunder.md).

Du behöver inte läsa alla tre samtidigt. Börja med den som lockar dig.

## För sjutton gubbar – första resultatet på två minuter!

Välj **ett enda** alternativ. De här exemplen räknar bara ut ett tal och **skriver ingen fil**.

**Windows / PowerShell:**

~~~powershell
Write-Output (21 * 2)
~~~

**Linux / terminal:**

~~~bash
echo $((21 * 2))
~~~

**Python 3:**

~~~python
print(21 * 2)
~~~

**Förväntat resultat i samtliga tre fall:**

~~~text
42
~~~

**Prova sedan själv:** Ändra `21` till `25`. Vilket resultat tror du att du får **innan** du kör? Kör igen och kontrollera. Då har du redan läst, förstått och ändrat ditt första lilla kodexempel.

Om du inte har något av programmen installerat kan du bara läsa raderna och förklara vad de gör – det räknas också som ett första steg.

## Första övningen – förstå, inte memorera

Öppna ett kodexempel i ditt valda kapitel och svara med egna ord:

1. Vilken rad instruerar datorn?
2. Vad tror du händer när koden körs?
3. Läser den information eller kan den ändra något?

**Du är klar när du kan förklara ett litet exempel utan att behöva kunna varje ord utantill.**

## För lärare och studiegrupper

Låt en person läsa koden och en annan förklara vad den gör. Byt roller. Det viktiga är förståelse, inte hur snabbt någon skriver. [Lärarhandledning](../for-larare.md).

[Nästa: Nivå 1 – Nybörjare →](01-nyborjare.md)
