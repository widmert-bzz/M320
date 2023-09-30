
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