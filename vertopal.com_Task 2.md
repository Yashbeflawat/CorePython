---
jupyter:
  kernelspec:
    display_name: Python (Pyodide)
    language: python
    name: python
  language_info:
    codemirror_mode:
      name: python
      version: 3
    file_extension: .py
    mimetype: text/x-python
    name: python
    nbconvert_exporter: python
    pygments_lexer: ipython3
    version: 3.8
  nbformat: 4
  nbformat_minor: 5
---

::: {#23a3c445-ef70-4d91-b36e-a577e7ed7a44 .cell .markdown}
# Task 2

## Understanding Comments

### 1. Single-Line Comment {#1-single-line-comment}

A single-line comment begins with the `#` character. Any text following
the `#` on that line is regarded as a comment.

**Example:**
:::

::: {#aa8163f6-86bb-4001-9b3f-17023cc781ec .cell .code trusted="true"}
``` python
# This is a single-line comment
y = 20  # This is an inline comment
```
:::

::: {#626d6e10-c35d-4d32-921c-fcc133372975 .cell .markdown}
1.  Multi-Line Comment While Python lacks a dedicated syntax for
    multi-line comments, you can use several single-line comments or
    employ triple quotes (\'\'\' or \"\"\") to achieve this.

Example:
:::

::: {#3bcb4164-7985-4640-930d-db9c13caacb3 .cell .code trusted="true"}
``` python
"""This is a multi-line comment.
It can extend over multiple lines and is useful
for providing comprehensive descriptions."""
y = 20
```
:::

::: {#d9a251e2-a3b2-4483-b8dd-fe1ed149f4ae .cell .markdown}
Understanding Indentation

Indentation in Python refers to the use of spaces or tabs at the start
of a line of code, which establishes the structure and hierarchy within
the code.

### Why Indentation Matters in Python:

-   **Defines Code Structure:** Indentation indicates which statements
    are part of the same block, allowing Python to recognize control
    structures like loops and conditionals.
-   **Enhances Readability:** Proper indentation makes the code visually
    appealing and easier to follow, helping other developers (or your
    future self) understand the logic quickly.
-   **Prevents Errors:** Incorrect indentation can lead to syntax errors
    or unintended behavior in the code, so maintaining consistent
    indentation helps avoid such pitfalls.
-   **Indicates Scope:** It helps delineate the scope of functions,
    classes, and loops, clarifying where a particular block of code
    begins and ends.
-   **Facilitates Collaboration:** In collaborative projects, consistent
    indentation styles improve teamwork by making the codebase more
    uniform and easier to navigate for multiple developers.
:::
