# Task 9

## While Loop in Python

### Objective:

A `while` loop continues to execute as long as a specified condition evaluates to True.

### Syntax:
```python
while condition:
    # Code that runs in the loop
```

### Example:
```python
# Initialize a variable
count = 1

# Loop while count is less than or equal to 4
while count <= 4:
    print(count)  # Print the current count
    count += 1    # Increase the count by 1
```

### Explanation:
1. We start with `count = 1`
2. The while loop executes as long as `count <= 4`
3. Inside the loop, `print(count)` displays the current value, and `count += 1` increments the count by 1 in each iteration
4. When count reaches 5, the condition `count <= 4` evaluates to False, and the loop terminates

### Best Practices:
1. Ensure that loops have a clear exit condition to avoid infinite loops
2. Use `.lower()` on user input to make it case-insensitive
3. Utilize `break` to exit the loop when necessary

### Additional Example:
```python
# Example of a while loop with user input
password = ""
while password != "secret":
    password = input("Enter the password: ").lower()
    if password != "secret":
        print("Incorrect password, try again!")
print("Access granted!")

# Example of using break statement
counter = 0
while True:
    counter += 1
    if counter > 5:
        break
    print(f"Count: {counter}")
```
