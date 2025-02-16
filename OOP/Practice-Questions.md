# Practice Questions #
##### Given below are questions which arose while learning about OOP in depth, with the answers i came up with. #####

### Q1. Can we define a class without using the 'class' keyword in Python?
Yes, you can create a class without using the 'class' keyword by using Python's built-in `type()` function. However, this approach isn't recommended for everyday use since it makes code harder to read and maintain. The conventional 'class' keyword approach is clearer and provides better access to Python's class features.

### Q2. What is the difference between a class variable and an instance variable?
A class variable is shared by all instances of a class, while instance variables are unique to each instance. Think of a class variable like a shared trait all objects have in common, and instance variables like individual characteristics. For example:

```python
class Student:
    school_name = "Python Academy"  # Class variable
    
    def __init__(self, name, grade):
        self.name = name        # Instance variable
        self.grade = grade      # Instance variable

student1 = Student("Alice", "A")
student2 = Student("Bob", "B")
```

### Q3. What happens when we don't use the __init__ constructor in a class?
When you don't define an `__init__` method, you'll need to set object attributes manually after creating the object. While this is possible, it's not recommended as it can lead to inconsistent object states. Here's an example:

```python
class Book:
    def show_info(self):
        print(f"Title: {self.title}, Author: {self.author}")

my_book = Book()
my_book.title = "Python Programming"  # Setting attributes manually
my_book.author = "John Smith"
```

### Q4. What happens if we don't include 'self' in the __init__ method?
If you omit 'self' from the `__init__` method, Python will raise an error because it can't properly associate the attributes with the instance being created. The 'self' parameter is essential as it represents the instance being initialized.

### Q5. Why should we create methods inside classes instead of using standalone functions?
While standalone functions might seem simpler, including methods within classes offers several benefits:
1. Better organization of related code
2. Data encapsulation
3. Code reusability
4. Easier maintenance
5. Better object-oriented design

### Q6. Is __init__ actually a constructor, and what does the double underscore mean?
The `__init__` method isn't technically a constructor - it's an initializer. The actual constructor in Python is `__new__`, which creates the object. `__init__` just sets up the initial state of that object. The double underscores (called "dunders") indicate that this is a special Python method with specific behavior. These methods are automatically called in certain situations.

### Q7. What happens when we assign one object to another object?
When you assign one object to another in Python, you're creating a reference to the same object in memory. Changes to either variable will affect both because they point to the same data. For example:

```python
class Pet:
    def __init__(self, name):
        self.name = name

cat1 = Pet("Whiskers")
cat2 = cat1  # Both variables now point to the same object
cat2.name = "Mittens"
print(cat1.name)  # Will print "Mittens"
```

### Q8. Why do we use the dot operator (.) to call object methods instead of parentheses?
The dot operator (.) is used to access attributes and methods of an object. It's part of Python's syntax for working with objects. Parentheses () are used to execute functions or methods, but you need the dot operator first to tell Python which object's method you're trying to call.

### Q9. What happens if we don't create any objects from a class, and can we create multiple objects from one class?
A class without objects is just a blueprint - it doesn't do anything on its own. You can create as many objects as you need from a single class. Each object will have its own set of instance variables but share the same methods. For example:

```python
class Restaurant:
    def __init__(self, name, cuisine):
        self.name = name
        self.cuisine = cuisine

italian = Restaurant("La Pasta", "Italian")
chinese = Restaurant("Golden Dragon", "Chinese")
mexican = Restaurant("El Taco", "Mexican")
```

[continued in next section due to length...]

### Q10. What happens when we define the same variable name inside and outside a class method?
When you define a variable with the same name inside and outside a class method, they are treated as separate variables with different scopes. The inner variable is only accessible within the method, while the outer variable maintains its original value. For example:

```python
class Calculator:
    def add_numbers(self):
        result = 10  # Local variable
        print(f"Inside method: {result}")

calc = Calculator()
result = 20  # Global variable
calc.add_numbers()  # Prints: Inside method: 10
print(f"Outside method: {result}")  # Prints: Outside method: 20
```

### Q11. Is a class mandatory for creating objects in Python?
No, you don't always need a class to create objects in Python. Many built-in types like strings, lists, and dictionaries are objects that can be created directly. For example:

```python
# Creating objects without classes
my_list = [1, 2, 3]  # List object
my_dict = {"name": "John"}  # Dictionary object
my_string = "Hello"  # String object
```

### Q12. Can you create an instance of a class without providing required parameters?
No, if a class's `__init__` method requires parameters, you must provide them when creating an instance. Otherwise, Python will raise a TypeError. You can make parameters optional by providing default values:

```python
class Course:
    def __init__(self, name="Python", level="Beginner"):
        self.name = name
        self.level = level

course1 = Course()  # Uses default values
course2 = Course("JavaScript", "Advanced")  # Uses provided values
```

### Q13. What is an instance dictionary?
An instance dictionary (`__dict__`) is a special attribute that stores all instance variables of an object as a dictionary. It contains the mapping of attribute names to their values. For example:

```python
class Employee:
    def __init__(self, name, role):
        self.name = name
        self.role = role

emp = Employee("Jane", "Developer")
print(emp.__dict__)  # Prints: {'name': 'Jane', 'role': 'Developer'}
```

### Q14. How can we avoid memory overhead when creating multiple instances?
To reduce memory usage when creating multiple instances, you can use the `__slots__` attribute. This replaces the instance dictionary with a fixed-size array, reducing memory usage. Here's how:

```python
class Point:
    __slots__ = ['x', 'y']
    
    def __init__(self, x, y):
        self.x = x
        self.y = y
```

### Q15. Does a class get stored in memory before we create an object?
Yes, when Python reads your code, it loads class definitions into memory during the compilation phase, even before any objects are created. This allows Python to know how to create objects when needed.

### Q16. Can we create a class with only methods and no attributes?
Yes, you can create a class with only methods. This is useful for grouping related functions together, especially for utility classes that perform operations but don't need to store data. For example:

```python
class StringHelper:
    def capitalize_words(self, text):
        return text.title()
    
    def count_vowels(self, text):
        return sum(1 for char in text.lower() if char in 'aeiou')
```

### Q17. How can we ensure that an attribute can only be accessed inside a class?
To make an attribute private (only accessible inside the class), prefix it with double underscores (__). This triggers name mangling in Python. For example:

```python
class BankAccount:
    def __init__(self, balance):
        self.__balance = balance  # Private attribute
    
    def get_balance(self):
        return self.__balance

account = BankAccount(1000)
# print(account.__balance)  # This would raise an error
print(account.get_balance())  # This works
```

### Q18. Can you create unlimited objects inside a class, and how can you restrict the number of objects?
While you can technically create as many objects as your computer's memory allows, you can restrict the number of instances using the Singleton pattern or by implementing a counter. Here's a simple example:

```python
class LimitedPool:
    _instance_count = 0
    _MAX_INSTANCES = 3
    
    def __init__(self):
        if LimitedPool._instance_count >= LimitedPool._MAX_INSTANCES:
            raise Exception("Cannot create more instances")
        LimitedPool._instance_count += 1
```
