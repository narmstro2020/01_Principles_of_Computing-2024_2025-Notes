
# Tutorial: If-Else Statements in Python (with Flowcharts)

Let's start by visualizing how conditional statements work using flowcharts. A flowchart is a graphical representation of a decision-making process, which helps us understand how conditions lead to specific actions.

In Python, the `if`, `else`, and `elif` statements form the backbone of decision-making, and we can represent this using simple flowcharts.

---

## 1. Basic Flowchart for an `if` Statement

An `if` statement checks a condition and performs an action if the condition is true. Here's how it looks in a flowchart:

```
          ┌───────────────────────┐
          │       Condition        │
          └─────────┬──────────────┘
                    │
          True ─────┴─────► Execute code
                    │
         False ───────────► Skip code
```

### Example Flowchart:

Imagine you are checking if someone is eligible to vote, with the condition being whether their age is greater than or equal to 18:

```
          ┌─────────────────────────────┐
          │ Is age greater than or equal │
          │         to 18?               │
          └─────────────┬───────────────┘
                        │
              True ─────┴──────► You can vote
                        │
             False ────────────► You cannot vote
```

## 2. Flowchart for an `if-else` Statement

In an `if-else` statement, when the condition is `True`, one block of code runs, and when it is `False`, another block runs. The flowchart for this structure looks like this:

```
          ┌───────────────────────┐
          │       Condition        │
          └─────────┬──────────────┘
                    │
          True ─────┴─────► Execute code A
                    │
         False ───────────► Execute code B
```

### Example Flowchart:

Consider the same voting eligibility scenario, but this time with an `else` block to cover both possible outcomes:

```
          ┌─────────────────────────────┐
          │ Is age greater than or equal │
          │         to 18?               │
          └─────────────┬───────────────┘
                        │
              True ─────┴──────► "You can vote"
                        │
             False ────────────► "You cannot vote yet"
```

## 3. Flowchart for an `if-elif-else` Statement

When multiple conditions need to be checked, we use the `elif` statement. The flowchart becomes more complex because it introduces additional decision points.

```
          ┌───────────────────────┐
          │       Condition 1      │
          └─────────┬──────────────┘
                    │
          True ─────┴─────► Execute code A
                    │
         False ────────────► Check Condition 2
                               ┌───────────────┐
                               │   Condition 2 │
                               └───────┬───────┘
                                       │
                            True ──────┴─────► Execute code B
                                       │
                          False ────────────► Execute code C
```

### Example Flowchart:

Let's extend our voting example by introducing categories based on age:

```
          ┌─────────────────────────────┐
          │ Is age greater than or equal │
          │         to 18?               │
          └─────────────┬───────────────┘
                        │
              True ─────┴──────► "You can vote"
                        │
             False ────────────► Check if age is >= 13
                                   ┌─────────────────────┐
                                   │ Is age greater than │
                                   │     or equal to 13? │
                                   └─────────┬───────────┘
                                             │
                                  True ──────┴─────► "You are a teenager"
                                             │
                                False ────────────► "You are a child"
```

## 4. Translating Flowcharts to Code

### Example: Voting Eligibility Program (with `if-else`)

Now that we’ve visualized the flowchart, let's convert it into Python code:

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("You can vote.")
else:
    print("You cannot vote yet.")
```

This code matches the simple `if-else` flowchart above. The condition (`age >= 18`) decides which block of code is executed.

### Example: Age Categorization Program (with `if-elif-else`)

The flowchart for categorizing based on age can be translated into the following Python code:

```python
age = int(input("Enter your age: "))

if age >= 18:
    print("You are an adult and can vote.")
elif age >= 13:
    print("You are a teenager.")
else:
    print("You are a child.")
```

This code follows the logic of the `if-elif-else` flowchart, checking each condition in turn.

---

## Conclusion

Using flowcharts can help visualize how conditions flow through an `if`, `else`, or `elif` structure in Python. Once you understand the logic visually, it becomes much easier to implement in code. Keep these flowcharts in mind as you work with conditionals in Python, and always think about how the flow of logic works behind the scenes!
