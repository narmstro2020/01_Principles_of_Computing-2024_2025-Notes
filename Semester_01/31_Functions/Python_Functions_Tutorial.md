
# Python Functions Tutorial

## 1. What is a Function?
A function is a reusable block of code that performs a specific task. Functions make programs easier to read, test, and maintain.

## 2. Defining a Function
In Python, you define a function using the `def` keyword, followed by the function name and parentheses `()`. A colon `:` marks the beginning of the function body.

**Syntax:**
```python
def function_name(parameters):
    # function body
    # perform actions
    return result
```

**Example:**
```python
def greet():
    print("Hello, world!")
```

## 3. Calling a Function
Once a function is defined, you can call it by using its name followed by parentheses.

```python
greet()  # Output: Hello, world!
```

## 4. Parameters and Arguments
Parameters are variables listed inside the parentheses in the function definition. Arguments are values passed to the function when it is called.

**Example:**
```python
def greet(name):
    print("Hello, " + name + "!")

greet("Alice")  # Output: Hello, Alice!
```

## 5. Return Statement
The `return` statement is used to send a result back to the caller. When Python encounters a return statement, it exits the function immediately.

**Example:**
```python
def add(a, b):
    return a + b

result = add(5, 3)
print(result)  # Output: 8
```

## 6. The `None` Type
In Python, `None` is a special data type representing the absence of a value. It is often used as a placeholder or default return value when a function does not explicitly return anything.

**Example:**
```python
def greet(name="World"):
    print("Hello, " + name + "!")

result = greet("Alice")
print(result)  # Output: None
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
---

## Assignment 1: Basic Calculator
Create a function called `calculator` that accepts three parameters: two numbers and an operator. The operator can be `+`, `-`, `*`, or `/`. Based on the operator, perform the respective operation and return the result.

**Example:**
```python
def calculator(num1, num2, operator):
    # Your code here

# Test cases
print(calculator(10, 5, '+'))  # Output: 15
print(calculator(10, 5, '-'))  # Output: 5
print(calculator(10, 5, '*'))  # Output: 50
print(calculator(10, 5, '/'))  # Output: 2.0
```

**Bonus:** Add error handling for division by zero.

---

