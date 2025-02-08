# Task 6: Operators - Arithmetic, Assignment, Comparison, Logical

## Objective:

Operators are utilized to carry out operations on variables and values. In this task, we will:

- Understand various types of operators.
- Use arithmetic operators for calculations.
- Apply comparison and logical operators to evaluate conditions.

### 1. Arithmetic Operators

These operators are used for mathematical computations:

**Example:**
```python
num1 = 15
num2 = 4
print(num1 + num2)  # Addition → 19
print(num1 - num2)  # Subtraction → 11
print(num1 * num2)  # Multiplication → 60
print(num1 / num2)  # Division → 3.75
print(num1 // num2) # Floor Division → 3
print(num1 % num2)  # Modulus (Remainder) → 3
print(num1 ** num2) # Exponentiation → 50625
```

### 2. Assignment Operators

These operators are used to assign values:

**Example:**
```python
value = 20
value -= 4  # value = value - 4 → 16
value /= 2  # value = value / 2 → 8.0
print(value)
```

### 3. Comparison Operators

These operators are used to compare values (returns True/False):

**Example:**
```python
x, y = 20, 15
print(x > y)   # True
print(x < y)   # False
print(x == y)  # False
print(x != y)  # True
```

### 4. Logical Operators

These operators are used to evaluate multiple conditions:

**Example:**
```python
marks = 80
class_participation = 90

if marks > 70 and class_participation > 80:
    print("Eligible for honors")  # Output: Eligible for honors
```

### Best Practices:

1. Use f-strings for clear formatting in print statements.
2. Employ comparison and logical operators to make decisions in your programs.
3. Maintain proper indentation for if-else conditions to avoid errors.
