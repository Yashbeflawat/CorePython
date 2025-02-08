# Task 3

## Variables & Basic Data Types (Numbers & Strings)

### Objective: 
To grasp the concept of variables and understand how integer, float, and string data types function in Python.

### 1. What are Variables?

In Python, a variable acts as a container for storing data. You can assign a value to a variable, which will hold that value. This value can be anything from a number to a string or even more complex data types.

**Syntax:**

```python
variable_name = value
```

Example:
```python
y = 20
```

### 2. Data Types in Python
Python includes several data types, but we will focus on three fundamental types: Integer, Float, and String.

#### a) Integer (int)

An integer is a complete number without any decimal component.

Example:
```python
number_of_apples = 15  # integer
```

#### b) Float (float)

A float is a number that contains a decimal point.

Example:
```python
price_per_kg = 2.75  # float
```

#### c) String (str)

A string is a sequence of characters enclosed in either single or double quotes.

Examples:
```python
city_name = "New York"  # string
greeting_message = 'Welcome to the party!'  # string
```

### 3. Best Practices

1. **Descriptive Names:** Choose meaningful variable names. Instead of using x or a, opt for names like number_of_apples, price_per_kg, or city_name to clarify the variable's purpose.

2. **Consistency:** Maintain a single naming convention throughout your code. Generally, variables should be written in lowercase letters with underscores separating words (snake_case), such as student_age or course_name.

3. **Avoid Overwriting Built-in Names:** Steer clear of naming your variables after Python's built-in functions or keywords, like list, print, or input.

Example Code:
```python
# Integer Variable
number_of_books = 12

# Float Variable
average_score = 88.5

# String Variable
favorite_color = "blue"

# Printing variables
print(f"My favorite color is {favorite_color}, I have {number_of_books} books, and my average score is {average_score}.")
```
