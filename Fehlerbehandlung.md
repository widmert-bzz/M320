### Syntaktische Fehler
- Befehle falsch geschrieben sein (`vor` statt `for`),
- Klammern fehlen oder zu viel stehen (`def a_method(x))`)
- oder Attribut bzw. Methodennamen falsch sein.
### Funktionale Fehler
Bei einem funktionalen Fehler wird ein Teil des Codes nicht resp. falsch ausgeführt.
### Logische Fehler
Bei einem logischen Fehler läuft der Code wohl korrekt ab, aber die Datenverarbeitung führt nicht zum erwarteten Ergebnis.
## Python-Exception
### Exception "fangen"

```python
try:
  # hier folgt der kritische Code, der potentielle Fehlersituationen haben kann.
  # typischerweise im Zusammenhang mit Benutzereingaben.
except:
  # hier folgt die Behandlung des Fehlers
else:
  # hier folgt Code, der nur dann ausgeführt wird, wenn es keine Exception gibt
finally:
  # hier folgt Code der sowohl als auch ausgeführt wird.
```

