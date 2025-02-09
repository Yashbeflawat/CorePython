# **Task 10**
## **Understanding Functions: Syntax, Usage, and the DRY Principle**

- **Objective**: What are functions, how are they structured, and why do we use them?

- A function is a `set of instructions that execute only when invoked`.
- We can provide input, known as `arguments`, to a function.
- Functions can return a value after performing operations.
- Functions are reusable sections of code that improve `modularity, efficiency, and clarity`.

**In Python, a function is created using the `def` keyword**.

```python
def example_function():  # Define the function
    print("Greetings")
Calling a Function
To invoke a function, use the function's name followed by parentheses.
python
Copy
Edit
def example_function():
    print("Greetings")

example_function()  # Call the function
Returning Multiple Values (Tuple Return)

python
Copy
Edit
def location():
    return 5, 15  # Return a tuple
a, b = location()
print(a, b)
Practice
python
Copy
Edit
def welcome():
    print("Hello, welcome to the coding platform!")
    
# Invoke the function
welcome()
Key Takeaways
In this exercise, I learned how to define and call functions.
I discovered that functions are defined using the def keyword.
I realized that by defining a function, I can call it as needed instead of writing repetitive code. This follows the DRY principle (Don't Repeat Yourself).