# Kapitel 3 – Python: begriplig kod och testning

[← Index](README.md) · [← Linux](02-linux-terminal.md) · [Säkerhet/Git →](04-sakerhet-och-git.md)

**Målet:** förstå variabler, villkor, funktioner, JSON, SHA256 och automatiska tester. Exemplen kräver bara vanlig Python.

## Variabler, villkor och funktioner

~~~python
namn = "AggE"
antal = 3

if antal > 2:
    print(f"Hej {namn}, det finns {antal} uppgifter.")
else:
    print("Färre uppgifter.")
~~~

Indraget efter `if` är viktigt i Python. `f"..."` gör att variabler kan skrivas in i en text.

~~~python
def tillaten_uppgift(task: str) -> bool:
    return task in {"echo", "inventory", "sha256"}

print(tillaten_uppgift("echo"))    # True
print(tillaten_uppgift("reboot"))  # False
~~~

`def` skapar en funktion. `return` lämnar ett svar. Typangivelserna (`str` och `bool`) förklarar vad vi avser; Python kontrollerar dem inte automatiskt vid varje anrop.

Funktionen illustrerar hur ett program kan ha en **begränsad lista med tillåtna uppgifter**. Den ger inte exekveringsbehörighet.

## Dictionaries och JSON

~~~python
import json

jobb = {"id": "demo-001", "task": "echo", "payload": {"message": "Hej"}}
text = json.dumps(jobb, ensure_ascii=False)
print(text)
~~~

En *dictionary* lagrar nycklar och värden. JSON är ett textformat som liknar det. Många program använder JSON för förfrågningar, inställningar och resultat.

## SHA256: kontrollsumma, inte signatur

~~~python
import hashlib

data = "Hej!".encode("utf-8")
fingeravtryck = hashlib.sha256(data).hexdigest()
print(fingeravtryck)
~~~

`encode("utf-8")` gör text till bytes. SHA256 räknar ett fingeravtryck av bytes, som blir 64 hexadecimaltecken.

**Viktig skillnad:** SHA256 kan jämföra innehåll men kan inte bevisa vem som godkände det. För en HMAC behövs dessutom en hemlig nyckel. En kontrollsumma är aldrig i sig ett mänskligt godkännande.

## Fånga fel öppet

~~~python
def dela(a, b):
    if b == 0:
        raise ValueError("Division med noll är inte tillåten")
    return a / b

try:
    print(dela(12, 0))
except ValueError as fel:
    print(f"Kontrollerat fel: {fel}")
~~~

Att **avvisa** felaktiga data kan vara det korrekta säkerhetsbeteendet.

## Automatiska tester

Skapa `test_matematik.py` i en **egen övningskatalog**:

~~~python
import unittest

def dubbla(tal):
    return tal * 2

class TestDubbla(unittest.TestCase):
    def test_positivt(self):
        self.assertEqual(dubbla(4), 8)

    def test_noll(self):
        self.assertEqual(dubbla(0), 0)

if __name__ == "__main__":
    unittest.main()
~~~

Kör i samma testkatalog:

~~~bash
python3 -m unittest -v test_matematik.py
~~~

På Windows med Python Launcher: `py -m unittest -v test_matematik.py`.

**Tre olika testnivåer:**

- *Enhetstest* undersöker en liten funktion.
- *Integrationstest* provar flera riktiga moduler tillsammans.
- *Systemtest* provar hela flödet i en isolerad testmiljö.

Gröna tester är värdefulla, men de är **inte samma sak som garanterad säkerhet eller produktionsgodkännande**.

## Övningar

1. Ändra funktionen så att den accepterar bara `echo`. Vad händer för `inventory`?
2. Skriv ett nytt test av `dubbla(-2)` och förklara förväntat resultat.
3. Ändra `data` i SHA256-exemplet. Jämför de två fingeravtrycken.
4. Förklara skillnaden mellan att en fil har rätt SHA256 och att någon behörig har godkänt att köra den.

[← Index](README.md) · [Nästa: Säkerhet och Git →](04-sakerhet-och-git.md)
