# Task 7

## Conditional Statements (if, elif, else) in Python

### Objective:

To control the flow of a program based on specific conditions using `if`, `elif`, and `else`.

### Example:
```python
temperature = 30

if temperature > 25:
    print("It's a hot day!")  # Execute this block if the condition is True
elif temperature >= 15:
    print("The weather is mild.")  # Execute if the previous condition was False, but this one is True
else:
    print("It's a cool day.")  # Execute if all above conditions are False
```

### Best Practices:

1. Keep conditions clear and well-structured.
2. Use `elif` instead of multiple `if` statements to enhance efficiency.
3. Utilize f-strings for clean and readable output formatting.

