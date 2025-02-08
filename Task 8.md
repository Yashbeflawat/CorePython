# Task 8  
# For Loop in Python

## Objective:

A `for` loop is employed to iterate over a sequence (such as a list, tuple, string, or dictionary).

### Syntax:
```python
for variable in sequence:
    # Code to execute in the loop
```

### Example:
```python
# Using a for loop to print even numbers from 2 to 10
for even_number in range(2, 11, 2):  
    print(even_number)
```

### Explanation:
- `range(2, 11, 2)` generates even numbers from 2 to 10 (the last number, 11, is not included).
- `for even_number in range(2, 11, 2):` loops through each even number in the specified range.
- `print(even_number)` prints each even number on a new line.

### Best Practices:

1. Use `enumerate()` if you need to access index values while iterating.
2. Use `.items()` for iterating over key-value pairs in dictionaries.
3. Avoid modifying lists during looping to prevent unexpected errors.

### Additional Examples:
```python
# Using enumerate to access both index and value
fruits = ["apple", "banana", "cherry"]
for index, fruit in enumerate(fruits):
    print(f"Index {index}: {fruit}")

# Iterating over dictionary items
student = {"name": "John", "age": 20, "grade": "A"}
for key, value in student.items():
    print(f"{key}: {value}")
```
