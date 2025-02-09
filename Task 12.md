# **Task 12**
## Inline Functions & Functional Programming Patterns

## Overview
Understanding compact, single-expression functions and their practical applications in data processing.

## Quick Functions (Inline Functions)
A quick function is a compact `single-expression operation` that can process multiple inputs but returns just one result.

### Basic Structure
```python
operation = lambda inputs: result_expression
```

### Simple Examples
Process a single value:
```python
calculate_tax = lambda price: price * 0.2
print(calculate_tax(100))    # Output: 20.0
```

Handle multiple inputs:
```python
calculate_total = lambda subtotal, tax_rate: subtotal * (1 + tax_rate)
print(calculate_total(100, 0.2))    # Output: 120.0
```

### Advanced Usage
Process three inputs:
```python
calculate_volume = lambda length, width, height: length * width * height
print(calculate_volume(2, 3, 4))    # Output: 24
```

## Function Factories
Create customized processing functions dynamically:

```python
def create_multiplier(factor):
    return lambda x: x * factor

double = create_multiplier(2)
triple = create_multiplier(3)

print(double(10))    # Output: 20
print(triple(10))    # Output: 30
```

## Data Processing Patterns

### Transform Collections (map)
Apply operations to every item in a sequence:

```python
temperatures = [0, 10, 20, 30]
fahrenheit = list(map(lambda celsius: celsius * 9/5 + 32, temperatures))
print(fahrenheit)    # Output: [32.0, 50.0, 68.0, 86.0]
```

### Filter Collections (filter)
Select items meeting specific criteria:

```python
scores = [75, 82, 95, 65, 88]
passing = list(filter(lambda score: score >= 70, scores))
print(passing)    # Output: [75, 82, 95, 88]
```

## Real-World Examples

### Price Calculator
```python
# Create different discount levels
standard_price = lambda base: base
member_price = lambda base: base * 0.9    # 10% discount
vip_price = lambda base: base * 0.8       # 20% discount

# Calculate prices for a $100 item
print(standard_price(100))    # Output: 100
print(member_price(100))      # Output: 90
print(vip_price(100))        # Output: 80
```

### Data Processing Pipeline
```python
data = [1, 2, 3, 4, 5, 6]

# Create a processing pipeline
filtered = filter(lambda x: x % 2 == 0, data)          # Keep even numbers
doubled = map(lambda x: x * 2, filtered)               # Double each number
formatted = map(lambda x: f"Value: {x}", doubled)      # Format as strings

results = list(formatted)
print(results)    # Output: ['Value: 4', 'Value: 8', 'Value: 12']
```

## Key Benefits
- Write cleaner, more concise code
- Create functions on-the-fly
- Simplify data transformation operations
- Enable functional programming patterns

## Best Practices
1. Use inline functions for simple, single-expression operations
2. Combine with map/filter for data processing
3. Consider readability - sometimes a regular function is clearer
4. Perfect for callback functions and data transformations

## Core Takeaways
- Mastered quick, inline function creation
- Understood function factories for dynamic operations
- Learned practical data processing patterns
- Applied concepts to real-world scenarios

Remember: While inline functions are powerful, prioritize code readability. Use them when they make your code clearer and more maintainable.
