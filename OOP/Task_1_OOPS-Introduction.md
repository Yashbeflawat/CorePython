# Understanding OOP with Concepts #

## Basic Concepts of OOP ##
### 1. Class ###
• A class is a blueprint for creating objects.

• It defines the properties (attributes) and behaviors (methods) that the objects of this class will have.
#### Real-world analogy: ####
 Think of a class like a blueprint for a house—while the blueprint itself is not a house, it defines how one will be constructed.
#### Purpose: ####
 Classes enable the organization of data and functionality into reusable and logical units.
#### How to create: ####
 You can define a class using the class keyword in Python.
```python
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model
```
In this example, Car is a class that describes cars and can have attributes like make and model.

### 2. Object ###
• An object is an instance of a class. It is created based on the blueprint defined by the class and represents a specific entity.
#### Real-world analogy: ####
 If a class is a blueprint of a house, an object is an actual house built using that blueprint.
#### Purpose: ####
Objects represent real-world entities and store their state and behavior.
#### How to create: ####
 You create an object by calling the class as if it were a function and passing the necessary arguments.
```python
my_car = Car("Toyota", "Corolla")
```
Here, my_car is an object of the class Car.

### 3. Attributes ###
• Attributes are variables that hold data specific to an object. 

• They define the properties or state of the object.

#### Real-world analogy: ####
Think of attributes as characteristics of an object, such as the color, size, or name of an item.
#### Purpose: ####
 They store data that is unique to each object of the class.
How to create: You can define attributes in the class's constructor method __init__.
```python
class Car:
    def __init__(self, make, model):
        self.make = make  # attribute
        self.model = model  # attribute
```
In this example, make and model are attributes of the Car class.

### 4. Methods ###
Definition: Methods are functions that are defined inside a class and define the behavior of the object.
#### Real-world analogy: ####
 Methods are actions that an object can perform, such as starting a car or driving it.
#### Purpose: ####
 They allow objects to interact with each other and modify their state.
#### How to create: ####
 Methods are defined just like functions but within a class. The first parameter is always self, which refers to the instance of the class.
```
class Car:
    def __init__(self, make, model):
        self.make = make
        self.model = model
    
    def start_engine(self):
        print(f"The {self.make} {self.model}'s engine is starting.")
```
