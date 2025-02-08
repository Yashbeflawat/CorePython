# Phase 1: Python Environment Setup & Basic Syntax

Welcome to the first phase of your Python journey! In this phase, You will be guided how to install python, set up a code editor and writing your first python program. Let's get started with the basics:

# Task 1: Installing Python & Setting Up Your Development Environment

To begin coding in Python, you first need to install Python on your computer and set up a development environment. Follow the steps below:

## Step 1: Download Python
- Head over to the official [Python website](https://www.python.org/downloads/)
- Choose the version that's right for your operating system (Windows, macOS, or Linux)
- Download the latest stable version (e.g., Python 3.10 or later)

## Step 2: Install Python
- Once the installer is downloaded, run it
- Make sure to check the box that says "Add Python to PATH" before you click on "Install Now". This step is very important as it allows you to run Python directly from the command line

## Step 3: Verify Python Installation
To ensure that Python was installed successfully, open your terminal (Command Prompt or Shell), and type the following:
```python
python --version
```
This should display the Python version you installed (e.g., Python 3.x.x).

## Step 4: Setting Up a Code Editor (VS Code)

Now, let's install a code editor to write and run Python code. We recommend using Visual Studio Code (VS Code), which is free, powerful, and easy to use.

1. Download VS Code: Go to the [VS Code download page](https://code.visualstudio.com/Download)
2. Download the version that matches your operating system (Windows, macOS, or Linux)

## Step 5: Install Python Extension in VS Code
1. Open VS Code and go to the Extensions tab (the little square icon on the left sidebar)
2. Search for "Python" in the search bar and click on the first extension by Microsoft
3. Click on Install to add the Python extension

## Step 6: Create Your First Python Program
1. Open VS Code, go to File > New File, and save it as `hello_world.py`
2. Inside the file, type:
```python
print("Hello, World!")
```
To run it, open the terminal in VS Code (Ctrl + `), and type:
```bash
python hello_world.py
```

And doing just that you have written your first python program!

# Task 2: Understanding Comments in Python

## 1. Single-line Comments
Comments are an essential part of writing clean and understandable code. They allow you to explain your code to others (or remind yourself later). In Python, a **single-line comment** starts with the `#` symbol. Everything after the `#` on that line is ignored by Python.

Example:
```python
# This is a single-line comment
x = 10  # This is an inline comment
```

## 2. Multi-line Comments
Python doesn't have a built-in multi-line comment syntax, but you can achieve it by using multiple single-line comments or triple quotes (''' or """).

Example:
```python
"""
This is a multi-line comment.
It can span several lines and is typically used for longer explanations.
"""
```

# The Importance of Indentation in Python

In Python, indentation refers to the spaces or tabs at the beginning of a line of code. It is used to define the structure and hierarchy of the code. This means that Python uses indentation to group code into blocks (e.g., inside loops, conditionals, and functions).

## Why Indentation is Crucial:
1. Defines Code Blocks: Indentation tells Python which statements belong together. For instance, all code inside a function or a loop must be indented.
2. Improves Readability: Proper indentation helps make your code more readable and structured, making it easier for both you and others to understand.

Here's an example of a properly indented Python function:
```python
def greet():
    # This line is indented to show it's inside the function block
    print("Hello, Python!")
```

## Great Job! You've Completed Phase 1!

You've successfully set up Python on your system, created your first Python program, and learned the importance of comments and indentation in Python.
