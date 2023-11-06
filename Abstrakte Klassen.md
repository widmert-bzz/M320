UML = {abstract}

Blaupause für andere Klassen
- min. 1 abstrakte Funktion
- kann auch implementierte Funktionen haben

Sie ermöglicht es, eine Reihe von Methoden zu erstellen, die **in allen untergeordneten Klassen implementiert werden müssen** (= Vertrag für die Implememtation), die von der abstrakten Klasse ableiten

![[Pasted image 20231104120445.png]]

## Bsp

```python
from abc import ABC, abstractmethod  
 
class Polygon(ABC):  
    """
    Ein unbestimmtes Polygon, das
    a) weiss, dass es eine gewisse Anzahl Seiten hat
    b) aber nicht weiss, wie viele es wirklich sind.
    """
    @abstractmethod
    def __init__(self):
        """
        Konstruktor: Abstrakte Methode um die Instantiierung zu verhindern
        """
        pass
 
 
    @abstractmethod  
    def my_sides(self): 
        """
        Abstrakte Methode ohne Implementierung. Diese muss
        zwingend in einer abgeleiteten Klasse erfolgen.
        """
        pass  
 
class Triangle(Polygon):  
    # overriding abstract method  
    def my_sides(self):  
        print('I have 3 sides')  
 
class Quadrilateral(Polygon):  
    # overriding abstract method  
    def my_sides(self):  
        print('I have 4 sides')  
 
 
if __name__ == '__main__':  
    polygons = [  
        Triangle(),  
        Quadrilateral(),   
    ]  
    for p in polygons:  
        p.my_sides()
```
