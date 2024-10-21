
# Tutorial: Booleans, Relational Operators, and Logical Operators in Python

In this tutorial, we will cover:
1. **Booleans in Python**
2. **Relational (Comparison) Operators**
3. **Logical Operators**

## 1. Booleans in Python

A **boolean** is a data type that can only have one of two values:
- `True`
- `False`

Booleans are used to represent truth values and are often the result of comparisons or logical operations. Python treats `True` as `1` and `False` as `0` internally.

**Example:**

```python
is_raining = True
has_umbrella = False
```

In the above example, `is_raining` holds the value `True`, and `has_umbrella` holds the value `False`.

## 2. Relational (Comparison) Operators

Relational operators are used to compare two values. The result of a comparison is always a boolean (`True` or `False`). Here are the common relational operators in Python:

| Operator | Description                     | Example          |
|----------|---------------------------------|------------------|
| `==`     | Equal to                        | `5 == 5` is `True` |
| `!=`     | Not equal to                    | `5 != 4` is `True` |
| `>`      | Greater than                    | `7 > 3` is `True`  |
| `<`      | Less than                       | `3 < 7` is `True`  |
| `>=`     | Greater than or equal to        | `5 >= 5` is `True` |
| `<=`     | Less than or equal to           | `4 <= 5` is `True` |

**Examples:**

```python
a = 10
b = 20

print(a == b)  # False, because 10 is not equal to 20
print(a != b)  # True, because 10 is not equal to 20
print(a < b)   # True, because 10 is less than 20
print(a >= 5)  # True, because 10 is greater than or equal to 5
```

## 3. Logical Operators

Python provides three logical operators:
- **`and`**: Returns `True` if both statements are `True`.
- **`or`**: Returns `True` if at least one statement is `True`.
- **`not`**: Reverses the boolean value.

| Operator | Description                                  | Example                          |
|----------|----------------------------------------------|----------------------------------|
| `and`    | Returns `True` if both conditions are `True` | `(5 > 3) and (8 > 5)` is `True`  |
| `or`     | Returns `True` if at least one is `True`     | `(5 > 3) or (8 < 5)` is `True`   |
| `not`    | Inverts the result                          | `not(5 > 3)` is `False`          |

**Examples:**

```python
a = 5
b = 10
c = 15

# Logical AND
print(a < b and b < c)  # True, because both conditions are True

# Logical OR
print(a > b or b < c)   # True, because the second condition is True

# Logical NOT
print(not(a > b))       # True, because a is not greater than b, so the result is inverted
```

## Combining Relational and Logical Operators

You can combine relational and logical operators to build complex expressions.

**Example:**

```python
age = 25
has_driver_license = True

# Check if the person is eligible to drive
is_eligible = age >= 18 and has_driver_license
print(is_eligible)  # True, because both conditions are True

# Checking multiple conditions
a = 10
b = 20
c = 30

result = (a < b or b > c) and not(c == b)
print(result)  # True, because the combination of conditions results in True
```

## Truthy and Falsy Values in Python

In Python, values such as numbers and strings can be evaluated as `True` or `False` when used in logical operations.

- **Falsy values**: `0`, `None`, `''` (empty string), `[]` (empty list), `False`
- **Truthy values**: Any non-zero number, non-empty string, non-empty list, etc.

**Example:**

```python
x = 0
y = "Hello"
z = []

print(bool(x))  # False, because 0 is falsy
print(bool(y))  # True, because non-empty strings are truthy
print(bool(z))  # False, because empty lists are falsy
```

## Summary
- **Booleans** are either `True` or `False`.
- **Relational operators** compare two values and return a boolean result.
- **Logical operators** (`and`, `or`, `not`) are used to combine boolean expressions.
- Python considers certain values truthy and others falsy.

By mastering these concepts, you’ll be able to write more complex decision-making code in Python!







