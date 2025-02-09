# **Task 11**
## Advanced Function Design: Input Handling, Output Processing, and Scope Management

## Purpose
Understanding how to manage function inputs, process outputs, and control variable accessibility.

## Input Handling Fundamentals

### Basic Input Processing
Functions can receive input data as `parameters`. You can include multiple inputs, separated by commas:

```python
def generate_greeting(username):    # Single input parameter
    print(username + " welcome!")
    
generate_greeting("Alex")    # Displays: Alex welcome!
generate_greeting("Sarah")   # Displays: Sarah welcome!
```

### Understanding Terminology
When working with function inputs:
- A `parameter` is the variable in the function definition
- An `input value` is what you actually pass to the function

### Input Quantity Management
Functions require the exact number of inputs specified in their definition:

```python
def create_profile(name, role):    # Expects exactly 2 inputs
    print(name + " - " + role)
    
create_profile("Emma", "Developer")    # Works correctly
create_profile("Emma")    # Error: Missing required input
```

### Flexible Input Handling (Dynamic Arguments)
For variable input quantities, use `*` before the parameter name:

```python
def process_team(*members):    # Accepts any number of inputs
    print("Team lead is: " + members[0])
    
process_team("Emma", "Alex", "Sarah")    # Works with 3 inputs
```

### Named Input Parameters
Use key-value pairs for clearer input specification:

```python
def setup_account(username, email, role):
    print(f"Created {role} account for {username}")

setup_account(username="emma_dev", email="emma@example.com", role="admin")
```

### Dynamic Named Parameters
Use `**` to accept any number of named inputs:

```python
def configure_system(**settings):
    print("Display mode: " + settings["display"])
    
configure_system(display="dark", notifications="on", language="en")
```

### Default Values
Specify fallback values for optional parameters:

```python
def set_theme(mode="light"):    # Default value is "light"
    print(f"Theme set to {mode} mode")
    
set_theme()           # Uses default: "light"
set_theme("dark")     # Uses provided value: "dark"
```

## Working with Different Data Types

### List Processing
Functions can handle complex data structures:

```python
def analyze_data(measurements):
    for value in measurements:
        print(f"Processing: {value}")
        
sensor_data = [24.5, 25.1, 23.8]
analyze_data(sensor_data)
```

## Output Management
Use `return` to send data back from functions:

```python
def calculate_area(width, height):
    return width * height

room_area = calculate_area(4, 5)
print(room_area)    # Displays: 20
```

## Empty Function Handling
Use `pass` for function placeholders:

```python
def initialize_system():
    pass    # Function to be implemented later
```

## Advanced Parameter Controls

### Position-Only Parameters
Use `/` to enforce position-based input:

```python
def calculate_power(base, exponent, /):
    return base ** exponent
    
calculate_power(2, 3)        # Valid
calculate_power(base=2, exponent=3)    # Invalid - must use positions
```

### Name-Only Parameters
Use `*,` to require named inputs:

```python
def configure_display(*, brightness, contrast):
    print(f"Display: {brightness}% brightness, {contrast}% contrast")
    
configure_display(brightness=80, contrast=75)    # Valid
configure_display(80, 75)    # Invalid - must use parameter names
```

### Combined Parameter Rules
Mix different parameter types:

```python
def process_image(format, quality, /, *, width, height):
    print(f"Processing {format} image: {quality}%, {width}x{height}")
    
process_image("PNG", 90, width=800, height=600)
```

## Practical Example

```python
def calculate_total(base_price, tax_rate):
    return base_price * (1 + tax_rate)

total_cost = calculate_total(99.99, 0.08)
print(f"Total: ${total_cost:.2f}")
```

## Key Insights
- Mastered function input handling and parameter types
- Understood named vs positional arguments
- Learned about flexible argument handling
- Gained knowledge of parameter restrictions and defaults

Remember: Well-designed function parameters make your code more flexible, maintainable, and easier to understand.
