Sprache: UML ([Unified Modelling Language](https://de.wikipedia.org/wiki/Unified_Modeling_Language "https://de.wikipedia.org/wiki/Unified_Modeling_Language")).

- **Attribute** immer private  
- **Konstruktoren**  bei  Erzeugung eines Objekts als erstes ausgeführt, Initialisieren der Attribute.
- **Methoden** stellen die Funktionalität der Klasse dar, Gesamtheit aller Methoden = «die Schnittstelle» der Klasse

- wenn statisch = Objektname und Klassenbezeichnung unterschrichen

## Beispiel
![[Pasted image 20230930110023.png]]

## Data Hidding
![[Pasted image 20230930110437.png]]
= private
- ohne private können Dinge unabhängig voneinander gemacht werden, was nicht gut ist
#= protected 

### Python
```python
self._das_gekapselte_Attribut = initialWert
```