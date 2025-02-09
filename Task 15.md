# **Task 15**
# Python File Operations: Complete Guide to Data Management

## Understanding File Operations
Learn how to work with files effectively for data persistence and management.

## File Access Modes

| Mode | Description | Action if File Exists | Action if File Doesn't Exist |
|------|-------------|----------------------|----------------------------|
| 'r'  | Read        | Open for reading     | Error                     |
| 'w'  | Write       | Overwrite           | Create new                |
| 'a'  | Append      | Add to end          | Create new                |
| 'x'  | Exclusive   | Error               | Create new                |

Additional modifiers:
- 't' - Text mode (default)
- 'b' - Binary mode
- '+' - Read and write access

## Basic File Operations

### Reading Files
```python
def read_file_content(filename):
    try:
        with open(filename, 'r') as file:
            content = file.read()
            return content
    except FileNotFoundError:
        return "Error: File not found"
```

### Writing Files
```python
def save_log_entry(filename, message):
    with open(filename, 'a') as file:
        timestamp = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
        file.write(f"[{timestamp}] {message}\n")
```

## Advanced File Operations

### Reading with Different Methods
```python
def display_file_content(filename):
    with open(filename, 'r') as file:
        # Read entire file
        content = file.read()
        print("Entire file:", content)
        
        # Reset file pointer
        file.seek(0)
        
        # Read line by line
        print("\nLine by line:")
        for line in file:
            print(f"Line: {line.strip()}")
```

### Working with CSV Files
```python
import csv

def process_user_data(filename):
    users = []
    with open(filename, 'r', newline='') as file:
        reader = csv.DictReader(file)
        for row in reader:
            users.append({
                'name': row['name'],
                'age': int(row['age']),
                'city': row['city']
            })
    return users

def save_user_data(filename, users):
    with open(filename, 'w', newline='') as file:
        writer = csv.DictWriter(file, fieldnames=['name', 'age', 'city'])
        writer.writeheader()
        writer.writerows(users)
```

### JSON File Operations
```python
import json

class ConfigManager:
    def __init__(self, config_file):
        self.config_file = config_file
        
    def load_config(self):
        try:
            with open(self.config_file, 'r') as file:
                return json.load(file)
        except FileNotFoundError:
            return {}
            
    def save_config(self, config_data):
        with open(self.config_file, 'w') as file:
            json.dump(config_data, file, indent=4)
```

## File Management

### Safe File Operations
```python
def safe_write(filename, content):
    try:
        with open(filename, 'w') as file:
            file.write(content)
        return True
    except IOError as e:
        print(f"Error writing to file: {e}")
        return False
```

### File Existence Check
```python
import os

def ensure_file_exists(filename, default_content=""):
    if not os.path.exists(filename):
        with open(filename, 'w') as file:
            file.write(default_content)
        return False
    return True
```

## Practical Examples

### Log File Manager
```python
class LogManager:
    def __init__(self, log_file):
        self.log_file = log_file
        
    def log_event(self, event_type, message):
        timestamp = datetime.now().strftime("%Y-%m-%d %H:%M:%S")
        log_entry = f"[{timestamp}] {event_type}: {message}\n"
        
        with open(self.log_file, 'a') as file:
            file.write(log_entry)
            
    def get_recent_logs(self, num_lines=10):
        try:
            with open(self.log_file, 'r') as file:
                lines = file.readlines()
                return lines[-num_lines:]
        except FileNotFoundError:
            return []
```

### Data Processor
```python
class DataProcessor:
    @staticmethod
    def process_text_file(input_file, output_file):
        try:
            with open(input_file, 'r') as infile:
                content = infile.read()
                
            # Process content (example: convert to uppercase)
            processed = content.upper()
            
            with open(output_file, 'w') as outfile:
                outfile.write(processed)
                
            return True
        except Exception as e:
            print(f"Error processing file: {e}")
            return False
```

## Best Practices

1. **Always Use Context Managers**
   - Use `with` statements to ensure proper file closure
   - Handles errors gracefully
   - Automatically manages resources

2. **Error Handling**
   - Check for file existence when needed
   - Handle IOError and FileNotFoundError
   - Provide meaningful error messages

3. **File Naming**
   - Use clear, descriptive filenames
   - Include appropriate file extensions
   - Consider using timestamps in log files

4. **Resource Management**
   - Close files properly
   - Don't keep files open longer than necessary
   - Use appropriate buffer sizes for large files

## Key Takeaways
- File operations are crucial for data persistence
- Always use proper error handling
- Context managers ensure proper resource cleanup
- Choose appropriate file modes for operations

Remember: Good file handling practices prevent data corruption and resource leaks.
