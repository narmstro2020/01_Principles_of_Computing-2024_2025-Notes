
# Python Functions Part 02 Tutorial

## 1. Default Parameters
Python allows you to specify default values for parameters.

**Example:**
```python
def greet(name="World"):
    print("Hello, " + name + "!")

greet()          # Output: Hello, World!
greet("Alice")   # Output: Hello, Alice!
```

## 2. Keyword Arguments
You can specify arguments by the parameter name.

**Example:**
```python
def greet(name, age):
    print(f"{name} is {age} years old.")

greet(age=25, name="Alice")  # Output: Alice is 25 years old.
```

## 3. Variable-Length Arguments
Python provides `*args` for arbitrary positional arguments and `**kwargs` for arbitrary keyword arguments.

**Example with `*args`:**
```python
def add(*numbers):
    total = sum(numbers)
    return total

print(add(1, 2, 3))  # Output: 6
```

**Example with `**kwargs`:**
```python
def display_info(**info):
    for key, value in info.items():
        print(f"{key}: {value}")

display_info(name="Alice", age=25)  # Output: name: Alice, age: 25
```

**Usage in Functions:**
- `None` is commonly used as a default parameter value.
- Functions that perform an action rather than compute a value (like printing) often implicitly return `None`.

**Example with `None` as Default Parameter:**
```python
def display_info(name=None):
    if name is None:
        print("No name provided.")
    else:
        print("Hello, " + name + "!")

display_info()         # Output: No name provided.
display_info("Alice")  # Output: Hello, Alice!
```

## 4. Further Elaboration on `*args` and `**kwargs`

### `*args` (Positional Variable-Length Arguments)
The `*args` syntax in a function definition allows you to pass a variable number of positional arguments to a function. It collects all additional positional arguments into a tuple, enabling the function to process them as needed.

**Examples and Use Cases:**
- Summing numbers:
  ```python
  def sum_numbers(*args):
      return sum(args)

  print(sum_numbers(1, 2, 3, 4))  # Output: 10
  ```

- Working with varying positional arguments:
  ```python
  def describe_person(name, *qualities):
      print(f"{name} has qualities like: {', '.join(qualities)}")

  describe_person("Alice", "kind", "intelligent", "curious")  
  # Output: Alice has qualities like: kind, intelligent, curious
  ```

### `**kwargs` (Keyword Variable-Length Arguments)
The `**kwargs` syntax allows you to pass a variable number of keyword arguments (name-value pairs) to a function. It collects all additional keyword arguments into a dictionary, enabling you to handle them in a flexible way.

**Examples and Use Cases:**
- Displaying dynamic user information:
  ```python
  def display_user_info(**kwargs):
      for key, value in kwargs.items():
          print(f"{key}: {value}")

  display_user_info(name="Alice", age=25, location="New York")
  # Output: name: Alice
  #         age: 25
  #         location: New York
  ```

- Specifying optional settings:
  ```python
  def configure_device(name, **settings):
      print(f"Configuring {name} with settings:")
      for setting, value in settings.items():
          print(f" - {setting}: {value}")

  configure_device("Phone", brightness="70%", volume="80%", bluetooth="On")
  # Output: Configuring Phone with settings:
  #          - brightness: 70%
  #          - volume: 80%
  #          - bluetooth: On
  ```

### Combining `*args` and `**kwargs` in Functions
You can combine both `*args` and `**kwargs` in a single function. This allows the function to accept any combination of positional and keyword arguments.

**Example:**
```python
def mixed_args(name, *args, **kwargs):
    print("Name:", name)
    print("Args:", args)
    print("Kwargs:", kwargs)

mixed_args("Alice", 25, "Developer", city="New York", language="Python")
# Output:
# Name: Alice
# Args: (25, 'Developer')
# Kwargs: {'city': 'New York', 'language': 'Python'}
```

---
## Assignment 1: Grade Average Calculator
Write a function `calculate_average` that takes a variable-length argument list of grades (integers). The function should calculate and return the average of these grades.

**Example:**
```python
def calculate_average(*grades):
    # Your code here

# Test cases
print(calculate_average(85, 90, 78, 92))  # Output: 86.25
print(calculate_average(100, 95))         # Output: 97.5
```

**Bonus:** Add error handling for an empty list of grades.
