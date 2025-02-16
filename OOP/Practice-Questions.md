# Python Classes: Questions and Answers

[Previous questions 1-9...]

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
