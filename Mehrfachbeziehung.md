## Beispiel

![[Pasted image 20230930120252.png]]![[Pasted image 20230930120337.png]]

## Kardinalität

- 1:1 Beziehung (ein Objekt kennt genau ein anderes Objekt)
- 1:n Beziehung (ein Objekt kenntviele andere Objekte)
- n:n Beziehung (ein Objekt kennt viele andere Objekte und umgekehrt)
_UML n = *_

### Umsetzung in Python
#### wichtige Methoden
- add
- set
- dem **Abfragen** der Grösse der Liste (Anzahl der gespeicherten Objekte)
- dem **Abrufen** einer Referenz über einen Index. Dieser muss aber gegen den size der Liste geprüft werden, damit kein unerlaubter Zugriff erfolgt!
- dem **Entfernen** einer Referenz aus der Liste

```python
class SchoolClass:
 
    def __init__(self, designation):
       self._designation = designation
       self._students = []  # hier wird eine leere Liste bereitgestellt, die dann die Refeenzen der Lernenden hält.
 
    def add_student(a_student):
       if len(self._students) < 24:
          self._students.append(a_student)
```

```python
 @proprty
  def size(self):
     return len(self._students)
 
  def take_student(self, index):
    if index < len(self._students):
       return self._students[index]
    else:
       raise StudentIndexError('search')
 
  def remove_student(self, index):
    if index < len(self._students):
       self._students.remove(index)
    else:
      raise StudentIndexError('remove')
```