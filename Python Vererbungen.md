## Erweitern
```python
class Vehicle:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def get_info(self):
        return f"{self.year} {self.make} {self.model}"

class Car(Vehicle):
    def __init__(self, make, model, year, num_doors):
        super().__init__(make, model, year)
        self.num_doors = num_doors

    def get_info(self):
        return f"{super().get_info()}, {self.num_doors} doors"

class Motorcycle(Vehicle):
    def __init__(self, make, model, year, engine_type):
        super().__init__(make, model, year)
        self.engine_type = engine_type

    def get_info(self):
        return f"{super().get_info()}, {self.engine_type} engine"

# Creating instances of the derived classes
my_car = Car("Toyota", "Camry", 2022, 4)
my_motorcycle = Motorcycle("Honda", "CBR", 2021, "Inline-4")

# Accessing information about vehicles
print(my_car.get_info())  # Output: "2022 Toyota Camry, 4 doors"
print(my_motorcycle.get_info())  # Output: "2021 Honda CBR, Inline-4 engine"

```

## Anpassen
```python
class Animal:
    def speak(self):
        pass

class Dog(Animal):
    def speak(self):
        return "Woof!"

class Cat(Animal):
    def speak(self):
        return "Meow"

class Cow(Animal):
    pass

# Create instances of different animals
dog = Dog()
cat = Cat()
cow = Cow()

# Call the speak method for each animal
print(dog.speak())  # Output: "Woof!"
print(cat.speak())  # Output: "Meow"
print(cow.speak())  # Output: (No output, as Cow does not override the speak method)

```