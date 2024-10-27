
# Python `while` Loop Tutorial

A `while` loop in Python allows you to repeatedly execute a block of code as long as a specified condition is true. It’s useful when you don’t know the exact number of times to run a loop but have a condition that determines the loop's lifespan.

## Syntax

```python
while condition:
    # code to be executed
```

- **condition**: The loop continues to execute as long as this condition is `True`.
- The **loop body**: Contains the statements that you want to execute repeatedly.

## Example: Basic `while` Loop

```python
count = 0
while count < 5:
    print("Count is:", count)
    count += 1
```

### Explanation

- Here, `count` starts at 0.
- The `while` loop checks if `count` is less than 5. If true, it executes the code block inside the loop.
- Each time the loop runs, `count` is incremented by 1. This continues until `count` reaches 5.

## Example: Infinite Loop

An infinite loop occurs when the condition always evaluates to `True`.

```python
while True:
    print("This will print forever!")
```

Use **infinite loops** with caution and ensure there’s a way to break out of them, such as using the `break` statement.

## Using `break` and `continue`

- **`break`**: Exits the loop entirely.
- **`continue`**: Skips the current iteration and moves to the next one.

### Example with `break`

```python
count = 0
while True:
    print(count)
    count += 1
    if count == 3:
        break  # Exits the loop when count reaches 3
```

### Example with `continue`

```python
count = 0
while count < 5:
    count += 1
    if count == 2:
        continue  # Skips the rest of the loop when count is 2
    print(count)
```

---

## Using `random.randint`

The `random.randint` function generates a random integer between two specified values, including both endpoints. It’s commonly used to create random numbers in games, simulations, and test scenarios.

### Syntax

```python
import random
random_number = random.randint(start, end)
```

- **`start`**: The smallest integer that can be generated.
- **`end`**: The largest integer that can be generated.

### Example

```python
import random
random_number = random.randint(1, 10)
print("Random number between 1 and 10:", random_number)
```

Each time you run the code, `random_number` will be a new random integer between 1 and 10.

---

## Nested `while` Loops

A **nested `while` loop** is a `while` loop inside another `while` loop. The inner loop will complete all its iterations for each single iteration of the outer loop. Nested loops are useful in scenarios where you need to repeat multiple layers of operations.

### Example of a Nested `while` Loop

```python
outer_count = 1
while outer_count <= 3:
    inner_count = 1
    while inner_count <= 2:
        print(f"Outer loop count: {outer_count}, Inner loop count: {inner_count}")
        inner_count += 1
    outer_count += 1
```

#### Explanation

1. The **outer loop** runs as long as `outer_count` is less than or equal to 3.
2. Inside this loop, we define an **inner loop** that runs as long as `inner_count` is less than or equal to 2.
3. For each iteration of the outer loop, the inner loop completes its full cycle (prints twice).

The output would look like:

```plaintext
Outer loop count: 1, Inner loop count: 1
Outer loop count: 1, Inner loop count: 2
Outer loop count: 2, Inner loop count: 1
Outer loop count: 2, Inner loop count: 2
Outer loop count: 3, Inner loop count: 1
Outer loop count: 3, Inner loop count: 2
```
