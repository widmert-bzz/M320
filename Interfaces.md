UML =<<interface>>
			-------------------------->

- nur abstrakte Funktionen
- Spezialfall von Abstrakten Klassen
- gut für Namensgebung, dass überall gleich ist
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass

    @abstractmethod
    def perimeter(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return 3.14 * self.radius * self.radius

    def perimeter(self):
        return 2 * 3.14 * self.radius

class Rectangle(Shape):
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        return self.length * self.width

    def perimeter(self):
        return 2 * (self.length + self.width)

# Creating instances of different shapes
circle = Circle(5)
rectangle = Rectangle(4, 6)

# Calculate and display the area and perimeter of each shape
print(f"Circle - Area: {circle.area()}, Perimeter: {circle.perimeter()}")
print(f"Rectangle - Area: {rectangle.area()}, Perimeter: {rectangle.perimeter()}")

```