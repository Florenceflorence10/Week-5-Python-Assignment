# Week-5-Python-Assignment
class Smartphone:
    def __init__(self, brand, model, storage, battery_life):
        self.brand = brand                # Public attribute
        self.model = model                # Public attribute
        self.storage = storage            # Public attribute
        self.__battery_life = battery_life  # Private attribute for encapsulation

    def show_specs(self):
        print(f"Brand: {self.brand}, Model: {self.model}, Storage: {self.storage} GB")

    def get_battery_life(self):           # Public method to access private attribute
        return f"{self.__battery_life} hours"

# Adding an inheritance layer
class GamingSmartphone(Smartphone):       # Subclass inheriting Smartphone class
    def __init__(self, brand, model, storage, battery_life, cooling_system):
        super().__init__(brand, model, storage, battery_life)  # Call parent constructor
        self.cooling_system = cooling_system

    def show_specs(self):                 # Method overriding (polymorphism)
        print(f"Gaming Smartphone - Brand: {self.brand}, Model: {self.model}, Cooling: {self.cooling_system}")
        
         ACTIVITY 2
Program: Polymorphism Example
# Base class
class Mover:
    def move(self):
        pass  # Abstract method; to be overridden by subclasses

# Animal classes
class Dog(Mover):
    def move(self):
        print("Running on paws 🐕")

class Bird(Mover):
    def move(self):
        print("Flying in the sky 🦅")

# Vehicle classes
class Car(Mover):
    def move(self):
        print("Driving on wheels 🚗")

class Plane(Mover):
    def move(self):
        print("Flying through the clouds ✈️")

# Using polymorphism
objects = [Dog(), Bird(), Car(), Plane()]

for obj in objects:
    obj.move()  # Calls the appropriate move() method based on the object




