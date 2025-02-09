# **Task 13**
## Python Code Organization: Working with Modules and Packages

## Introduction
Learn how to organize code using modules, import functionality from Python's standard library, and create reusable code components.

## Understanding Modules
A module is a Python file that contains reusable code components:
- Functions
- Classes
- Variables
- Constants

## Creating Custom Modules

### Basic Module Creation
Create a file named `calculator.py`:
```python
def add(x, y):
    return x + y
    
def subtract(x, y):
    return x - y
    
PI = 3.14159
DEFAULT_TAX_RATE = 0.2
```

### Using Your Module
```python
import calculator

result = calculator.add(10, 5)
print(result)                    # Output: 15
print(calculator.PI)             # Output: 3.14159
```

## Import Patterns

### Standard Import
Import the entire module:
```python
import calculator
result = calculator.subtract(10, 5)
```

### Selective Import
Import specific components:
```python
from calculator import add, PI
result = add(10, 5)     # No need for calculator.add
print(PI)               # Direct access to PI
```

### Import with Alias
Create a shorter name for the module:
```python
import calculator as calc
result = calc.add(10, 5)
```

## Working with Built-in Modules

### Date and Time Operations (datetime)
```python
from datetime import datetime, timedelta

# Get current date/time
current_time = datetime.now()
print(current_time)

# Add 5 days to current date
future_date = current_time + timedelta(days=5)
print(future_date)
```

### Mathematical Operations (math)
```python
import math

# Calculate area of a circle
radius = 5
area = math.pi * math.pow(radius, 2)
print(f"Circle area: {area:.2f}")

# Round up and down
print(math.ceil(4.2))    # Output: 5
print(math.floor(4.2))   # Output: 4
```

### Random Number Generation (random)
```python
import random

# Generate random number between 1 and 100
number = random.randint(1, 100)
print(number)

# Choose random item from list
colors = ['red', 'green', 'blue']
chosen = random.choice(colors)
print(chosen)
```

## Creating a Complete Module Example

### File: `data_processor.py`
```python
import datetime

class DataProcessor:
    def __init__(self):
        self.processing_date = datetime.datetime.now()
        
    def format_text(self, text):
        return text.strip().upper()
        
    def generate_id(self):
        return f"ID_{self.processing_date.strftime('%Y%m%d_%H%M%S')}"

# Constants
MAX_ITEMS = 1000
VALID_TYPES = ['text', 'number', 'date']

# Utility functions
def validate_data(data_type):
    return data_type.lower() in VALID_TYPES
```

### Using the Module
```python
from data_processor import DataProcessor, validate_data, MAX_ITEMS

# Create processor instance
processor = DataProcessor()

# Use various components
text = processor.format_text("  hello world  ")
print(text)                        # Output: HELLO WORLD

new_id = processor.generate_id()
print(new_id)                      # Output: ID_20250209_143022

is_valid = validate_data('text')
print(is_valid)                    # Output: True

print(f"Max items: {MAX_ITEMS}")   # Output: Max items: 1000
```

## Module Discovery and Inspection

### List Module Contents
```python
import json
print(dir(json))    # Lists all attributes and methods in json module
```

### Get Module Help
```python
help(json.dumps)    # Shows documentation for json.dumps function
```

## Best Practices

1. **Module Organization**
   - Keep related functionality together
   - Use clear, descriptive names
   - Include documentation

2. **Import Guidelines**
   - Import modules at the top of the file
   - Use specific imports when possible
   - Group imports logically (standard library, third-party, local)

3. **Module Design**
   - Keep modules focused on a single purpose
   - Use clear naming conventions
   - Include docstrings and comments

## Key Takeaways
- Modules help organize and reuse code
- Python's standard library provides many useful modules
- Different import patterns serve different needs
- Good module design improves code maintainability

Remember: Well-organized modules make your code more maintainable, reusable, and easier to understand.
