# Lab 5: Conditionals and Flow Control

---

# Objectives
- Understand how to use conditional statements in Python.
- Learn about flow control mechanisms such as `if`, `elif`, and `else`.
- Practice writing programs that utilize conditionals.

---

# Conditional statements

There are situations in real life when we need to do some specific task and based on some specific conditions, we decide what we should do next. Similarly, there comes a situation in programming where a specific task is to be performed if a specific condition is True. In such cases, conditional statements can be used. 


---

## `if` Statement in Python

If the simple code of block is to be performed if the condition holds true then the `if` statement is used. Here the condition mentioned holds then the code of the block runs otherwise not.

```python
# Syntax
if condition:           
    # Statements to execute if condition is true
```

---

## Basic Conditional Check with if Statement

In this example, an `if` statement checks if 10 is greater than 5. If true, it prints "10 greater than 5"; regardless, it then prints "Program ended" as the next statement, indicating the program flow.

```python
# if statement example
if 10 > 5:
    print("10 greater than 5")

print("Program ended")
```
```
10 greater than 5
Program ended
```

---

## `if-else` Statement in Python

In conditional `if` Statement the additional block of code is merged as $\texttt{else}$ statement which is performed when if condition is false.

```python
# Syntax:
if (condition):
    # Executes this block if condition is true
else:
    # Executes this block if condition is false
```

---

**Example: Handling Conditional Scenarios with `if-else`**

In this example, the code assigns the value 3 to variable x and uses an `if-else` statement to check if x is equal to 4. If true, it prints "Yes"; otherwise, it prints "No", demonstrating a conditional branching structure.

```python
# if-else statement example
x = 3
if x == 4:
    print("Yes")
else:
    print("No")
```

```
No
```

---

**Example: Nested `if-else` Chain for Multiple Conditions**

```python
# if-else chain statement
letter = "A"

if letter == "B":
    print("letter is B")
else:
    if letter == "C":
        print("letter is C")
    else:
        if letter == "A":
            print("letter is A")
        else:
            print("letter isn't A, B and C")
```

```
letter is A
```

---

## Nested `if` Statement

`if` statement can also be checked inside other if statement. This conditional statement is called a nested if statement. This means that inner if condition will be checked only if outer if condition is true and by this, we can see multiple conditions to be satisfied.

```python
# Syntax
if (condition1):
        # Executes when condition1 is true
        if (condition2):
            # Executes when condition2 is true
        # if Block is end here
    # if Block is end here
```

---

**Example: Managing Nested Conditions for Refined Control**

```python
# Nested if statement example
num = 10

if num > 5:
    print("Bigger than 5")

    if num <= 15:
        print("Between 5 and 15")
```
```
Bigger than 5
Between 5 and 15
```

---

## `if-elif` Statement in Python

The `if-elif` statement is shortcut of `if-else` chain. While using `if-elif` statement at the end $\texttt{else}$ block is added which is performed if none of the above `if-elif` statement is true.

```python
# Syntax:
if (condition):
    # statement
elif (condition):
    # statement
else:
    # statement
```

---

**Example: Sequential Evaluation with $\texttt{if-elif-else}$ Structure**

```python
# if-elif statement example
letter = "A"

if letter == "B":
    print("letter is B")

elif letter == "C":
    print("letter is C")

elif letter == "A":
    print("letter is A")

else:
    print("letter isn't A, B or C")
```

```
letter is A
```
