# Task 4: Detailed Exploration of Strings

## Objective

To understand string manipulation, concatenation, slicing, and formatting using f-strings or `.format()` in Python.

### 1. String Manipulation

Strings in Python are highly versatile. You can manipulate them in various ways, such as altering their case, dividing them into components, and formatting them for display.

### 2. String Methods

Python offers several built-in methods that you can apply to strings for manipulation and processing:

- **`.upper()`**: Converts all characters in a string to uppercase.
- **`.lower()`**: Converts all characters in a string to lowercase.
- **`.split()`**: Divides a string into a list based on a specified delimiter (e.g., space, comma, etc.).

### 3. Practice Example

```python
# User input capturing feedback on travel experiences
travel_feedback = input("Share your thoughts on your recent travel experience: ")

# Convert the string to uppercase
uppercase_feedback = travel_feedback.upper()
print(f"Uppercase Version: {uppercase_feedback}")

# Convert the string to lowercase
lowercase_feedback = travel_feedback.lower()
print(f"Lowercase Version: {lowercase_feedback}")

# Split the string into words (by spaces) and display the list
splitted_feedback = travel_feedback.split()
print(f"Split Version (Words): {splitted_feedback}")

# Format the string with f-string
formatted_string = f"Travel Feedback: {travel_feedback}"
print(formatted_string)
```
