{
  "metadata": {
    "kernelspec": {
      "name": "python",
      "display_name": "Python (Pyodide)",
      "language": "python"
    },
    "language_info": {
      "codemirror_mode": {
        "name": "python",
        "version": 3
      },
      "file_extension": ".py",
      "mimetype": "text/x-python",
      "name": "python",
      "nbconvert_exporter": "python",
      "pygments_lexer": "ipython3",
      "version": "3.8"
    }
  },
  "nbformat_minor": 5,
  "nbformat": 4,
  "cells": [
    {
      "id": "9ab1e10f-821b-4abb-b8be-d7ee189ac9c9",
      "cell_type": "markdown",
      "source": "# Task 3\n\n## Variables & Basic Data Types (Numbers & Strings)\n\n### Objective: \nTo grasp the concept of variables and understand how integer, float, and string data types function in Python.\n\n### 1. What are Variables?\n\nIn Python, a variable acts as a container for storing data. You can assign a value to a variable, which will hold that value. This value can be anything from a number to a string or even more complex data types.\n\n**Syntax:**\n\n```python\nvariable_name = value\nExample:",
      "metadata": {}
    },
    {
      "id": "e0485b54-99c8-4a1b-94bf-29548e8bf8b2",
      "cell_type": "code",
      "source": "y = 20",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "aac3f33a-aaab-4721-9b3e-5bff086d643a",
      "cell_type": "markdown",
      "source": "2. Data Types in Python\nPython includes several data types, but we will focus on three fundamental types: Integer, Float, and String.\n\na) Integer (int)\n\nAn integer is a complete number without any decimal component.\n\nExample:",
      "metadata": {}
    },
    {
      "id": "4761ba7d-4cf7-4404-90e7-503ab1806986",
      "cell_type": "code",
      "source": "number_of_apples = 15  # integer",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "3f52e2a0-8714-4385-af00-57fa9e55ec37",
      "cell_type": "markdown",
      "source": "b) Float (float)\n\nA float is a number that contains a decimal point.\n\nExample:",
      "metadata": {}
    },
    {
      "id": "5d997510-89c4-432a-be7b-9cf0a5108669",
      "cell_type": "code",
      "source": "price_per_kg = 2.75  # float",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "ad22fe6d-202b-4c31-9918-ae1109109587",
      "cell_type": "markdown",
      "source": "c) String (str)\n\nA string is a sequence of characters enclosed in either single or double quotes.\n\nExamples:",
      "metadata": {}
    },
    {
      "id": "5a18169c-439b-45bb-88ae-eeddb451c1bb",
      "cell_type": "code",
      "source": "city_name = \"New York\"  # string\ngreeting_message = 'Welcome to the party!'  # string",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "75bf5304-4be0-4a69-8cb2-9ee3f4ad4a40",
      "cell_type": "markdown",
      "source": "3. Best Practices\nDescriptive Names: Choose meaningful variable names. Instead of using x or a, opt for names like number_of_apples, price_per_kg, or city_name to clarify the variable's purpose.\n\nConsistency: Maintain a single naming convention throughout your code. Generally, variables should be written in lowercase letters with underscores separating words (snake_case), such as student_age or course_name.\n\nAvoid Overwriting Built-in Names: Steer clear of naming your variables after Python's built-in functions or keywords, like list, print, or input.\n\nExample Code:",
      "metadata": {}
    },
    {
      "id": "b099dc95-110c-4550-b7a1-227497d8956a",
      "cell_type": "code",
      "source": "# Integer Variable\nnumber_of_books = 12\n\n# Float Variable\naverage_score = 88.5\n\n# String Variable\nfavorite_color = \"blue\"\n\n# Printing variables\nprint(f\"My favorite color is {favorite_color}, I have {number_of_books} books, and my average score is {average_score}.\")\n",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    }
  ]
}
