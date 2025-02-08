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
      "id": "23a3c445-ef70-4d91-b36e-a577e7ed7a44",
      "cell_type": "markdown",
      "source": "# Task 2\n\n## Understanding Comments\n\n### 1. Single-Line Comment\n\nA single-line comment begins with the `#` character. Any text following the `#` on that line is regarded as a comment.\n\n**Example:**",
      "metadata": {}
    },
    {
      "id": "aa8163f6-86bb-4001-9b3f-17023cc781ec",
      "cell_type": "code",
      "source": "# This is a single-line comment\ny = 20  # This is an inline comment\n",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "626d6e10-c35d-4d32-921c-fcc133372975",
      "cell_type": "markdown",
      "source": "2. Multi-Line Comment\nWhile Python lacks a dedicated syntax for multi-line comments, you can use several single-line comments or employ triple quotes (''' or \"\"\") to achieve this.\n\nExample:",
      "metadata": {}
    },
    {
      "id": "3bcb4164-7985-4640-930d-db9c13caacb3",
      "cell_type": "code",
      "source": "\"\"\"This is a multi-line comment.\nIt can extend over multiple lines and is useful\nfor providing comprehensive descriptions.\"\"\"\ny = 20",
      "metadata": {
        "trusted": true
      },
      "outputs": [],
      "execution_count": null
    },
    {
      "id": "d9a251e2-a3b2-4483-b8dd-fe1ed149f4ae",
      "cell_type": "markdown",
      "source": "Understanding Indentation\n\nIndentation in Python refers to the use of spaces or tabs at the start of a line of code, which establishes the structure and hierarchy within the code.\n\n\n### Why Indentation Matters in Python:\n\n- **Defines Code Structure:** Indentation indicates which statements are part of the same block, allowing Python to recognize control structures like loops and conditionals.\n- **Enhances Readability:** Proper indentation makes the code visually appealing and easier to follow, helping other developers (or your future self) understand the logic quickly.\n- **Prevents Errors:** Incorrect indentation can lead to syntax errors or unintended behavior in the code, so maintaining consistent indentation helps avoid such pitfalls.\n- **Indicates Scope:** It helps delineate the scope of functions, classes, and loops, clarifying where a particular block of code begins and ends.\n- **Facilitates Collaboration:** In collaborative projects, consistent indentation styles improve teamwork by making the codebase more uniform and easier to navigate for multiple developers.\n",
      "metadata": {}
    }
  ]
}