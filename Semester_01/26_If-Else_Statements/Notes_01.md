
# Tutorial: If-Else Statements in Python

In Python, conditional statements allow you to execute certain pieces of code based on whether a condition is true or false. The most basic conditional statements are `if`, `else`, and `elif`.

## 1. Basic `if` Statement

The `if` statement evaluates a condition. If the condition is `True`, the code inside the `if` block is executed. If it’s `False`, Python skips over the block.

### Syntax:
```python
if condition:
    # code block executed if the condition is true
```

### Example:
```python
age = 20

if age >= 18:
    print("You are an adult.")
```

In this example, the program checks if the variable `age` is greater than or equal to 18. Since it is, the message "You are an adult." is printed.

## 2. The `else` Statement

The `else` block runs when the condition in the `if` statement is `False`.

### Syntax:
```python
if condition:
    # code block if the condition is true
else:
    # code block if the condition is false
```

### Example:
```python
age = 16

if age >= 18:
    print("You are an adult.")
else:
    print("You are not an adult.")
```

Here, since `age` is less than 18, the output will be "You are not an adult."

## 3. The `elif` Statement

The `elif` (short for "else if") statement allows you to check multiple conditions in sequence. If the `if` condition is `False`, Python moves to the next `elif` condition.

### Syntax:
```python
if condition1:
    # code block if condition1 is true
elif condition2:
    # code block if condition2 is true
else:
    # code block if all conditions are false
```

### Example:
```python
age = 16

if age >= 18:
    print("You are an adult.")
elif age >= 13:
    print("You are a teenager.")
else:
    print("You are a child.")
```

In this case, since `age` is 16, the output will be "You are a teenager."

## 4. Nested `if` Statements

You can nest `if` statements inside each other for more complex conditions.

### Example:
```python
age = 20
is_student = True

if age >= 18:
    if is_student:
        print("You are an adult and a student.")
    else:
        print("You are an adult but not a student.")
else:
    print("You are not an adult.")
```

Here, the outer `if` checks if the person is an adult, and the nested `if` checks if the person is also a student.

## 5. Using Logical Operators with `if`

You can use logical operators like `and`, `or`, and `not` to combine conditions.

### Example with `and`:
```python
age = 20
has_ID = True

if age >= 18 and has_ID:
    print("You can enter the club.")
else:
    print("You cannot enter the club.")
```

Here, both conditions must be `True` for the message "You can enter the club." to print.

### Example with `or`:
```python
age = 20
has_invite = False

if age >= 18 or has_invite:
    print("You can attend the event.")
else:
    print("You cannot attend the event.")
```

In this case, the person can attend the event if they meet either of the conditions.

### Example with `not`:
```python
is_raining = False

if not is_raining:
    print("You can go outside without an umbrella.")
else:
    print("You need an umbrella.")
```

The `not` operator reverses the condition, so the message "You can go outside without an umbrella." will print because `is_raining` is `False`.

## 6. Practical Example: A Simple Voting Eligibility Program

Let’s combine everything we’ve learned to create a program that checks if someone is eligible to vote:

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("You are eligible to vote.")
else:
    print("You are not eligible to vote yet.")
```

This program takes the user's age as input and checks if they are 18 or older. If they are, it tells them they can vote. Otherwise, it tells them they are not eligible yet.

---

## Conclusion:
- The `if` statement checks a condition and runs the associated code if the condition is `True`.
- The `else` statement provides code to run when the `if` condition is `False`.
- The `elif` statement allows for multiple conditions to be checked in sequence.
- You can use logical operators to combine conditions for more complex decisions.

Try experimenting with different conditions and combinations to understand how Python handles control flow!
