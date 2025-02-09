# **Task 14**
## Python Error Management: Graceful Exception Handling

## Understanding Error Management
Learn how to handle errors gracefully to create robust and reliable applications.

## Basic Error Handling Structure
```python
try:
    # Code that might raise an error
    result = 10 / 0
except:
    # Code to handle the error
    print("An error occurred")
```

## Common Error Handling Patterns

### Handling Specific Errors
```python
def divide_numbers(a, b):
    try:
        result = a / b
        return result
    except ZeroDivisionError:
        return "Error: Cannot divide by zero"
    except TypeError:
        return "Error: Please provide numbers only"
```

### Multiple Error Types
```python
def process_data(data):
    try:
        value = data['count'] * 2
        return value
    except KeyError:
        return "Error: 'count' not found in data"
    except TypeError:
        return "Error: Invalid data type"
    except Exception as e:
        return f"Unexpected error: {str(e)}"
```

## Using else and finally

### Successful Execution Block (else)
```python
def save_user_data(username):
    try:
        user_file = open(f"{username}.txt", "w")
        user_file.write("User profile created")
    except IOError:
        print("Error: Could not create user file")
    else:
        print("User profile saved successfully")
        return True
    finally:
        user_file.close()
```

### Cleanup Operations (finally)
```python
def process_file(filename):
    file = None
    try:
        file = open(filename, "r")
        content = file.read()
        return content
    except FileNotFoundError:
        print(f"Error: File {filename} not found")
    finally:
        if file:
            file.close()
            print("File closed successfully")
```

## Custom Error Handling

### Raising Custom Exceptions
```python
class InvalidAgeError(Exception):
    pass

def verify_age(age):
    if age < 0:
        raise InvalidAgeError("Age cannot be negative")
    if age > 150:
        raise InvalidAgeError("Age seems invalid")
    return "Age verified successfully"
```

### Custom Error Messages
```python
def validate_password(password):
    try:
        if len(password) < 8:
            raise ValueError("Password too short")
        if not any(c.isupper() for c in password):
            raise ValueError("Password needs an uppercase letter")
        return "Password is valid"
    except ValueError as e:
        return f"Invalid password: {str(e)}"
```

## Real-World Examples

### Database Connection Handler
```python
class DatabaseConnection:
    def connect(self, connection_string):
        try:
            # Simulate database connection
            if "invalid" in connection_string:
                raise ConnectionError
            print("Connected to database")
        except ConnectionError:
            print("Failed to connect to database")
        else:
            print("Connection established successfully")
        finally:
            print("Connection attempt completed")
```

### File Processing System
```python
def process_csv_file(filename):
    try:
        with open(filename, 'r') as file:
            header = file.readline()
            if not header:
                raise ValueError("File is empty")
            return "File processed successfully"
    except FileNotFoundError:
        return "Error: File does not exist"
    except PermissionError:
        return "Error: No permission to access file"
    except ValueError as e:
        return f"Error: {str(e)}"
```

## Advanced Error Handling

### Context Managers
```python
class ResourceManager:
    def __enter__(self):
        print("Resource acquired")
        return self
        
    def __exit__(self, exc_type, exc_val, exc_tb):
        print("Resource released")
        return False  # Re-raise any exceptions

def use_resource():
    with ResourceManager() as resource:
        print("Using resource")
        # raise Exception("Something went wrong")
```

### Chaining Exceptions
```python
def process_data_safely(data):
    try:
        processed = process_step_one(data)
    except ValueError as e:
        raise RuntimeError("Data processing failed") from e
```

## Best Practices

1. **Be Specific**
   - Catch specific exceptions rather than using bare except
   - Provide meaningful error messages
   - Use appropriate exception types

2. **Clean Up Resources**
   - Always use finally or context managers for cleanup
   - Close files, connections, and other resources properly

3. **Error Recovery**
   - Implement proper error recovery mechanisms
   - Log errors for debugging
   - Provide useful feedback to users

## Key Takeaways
- Error handling makes programs more robust
- Use specific exception types for better error management
- Always clean up resources properly
- Implement proper error recovery mechanisms

Remember: Good error handling improves user experience and makes debugging easier.
