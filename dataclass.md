## Use case

![[Pasted image 20230930105556.png]]

Human:
- size
- hair_color
- weight

- breath()
- eat()
- go()
- …

Address
-  street
- number
- postal_code
- city

Adress ist eine Typische datacalss, da sie nur getter und setter braucht(wird selbst generiert)
## Minimal Form
```python
from dataclasses import dataclass  
  
  
@dataclass  
class Grade:  
    value: float  
    date: str = 'no date'  

```
## Beispiel
```python
from dataclasses import dataclass  
  
  
@dataclass  
class Grade:  
    value: float  
    date: str = 'no date'  
  
    def __init__(self, value: float, date: str = 'no date'):  
        if value < 1 or value > 6:  
            self.value = -1.0  
        else:  
            self.value = value  
        self.date = date
```