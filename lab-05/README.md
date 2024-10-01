# Lab 5: Conditionals and Flow Control

## Objectives
- Understand how to use conditional statements in Python.
- Learn about flow control mechanisms such as `if`, `elif`, and `else`.
- Practice writing programs that utilize conditionals.

---

## 1. Introduction to Conditionals

In Python, conditional statements are used to perform different actions based on different conditions. The most common conditional statements are `if`, `elif`, and `else`.

### 1.1 Syntax of Conditional Statements

```python
if condition:
    # code to execute if condition is true
elif another_condition:
    # code to execute if the previous conditions were false and this condition is true
else:
    # code to execute if none of the conditions were true
```

### Example
```python
x = 10

if x > 0:
    print("x is positive")
elif x < 0:
    print("x is negative")
else:
    print("x is zero")
```

---

## 2. Exercise 1: Simple Conditionals

### Task
Write a program that checks if a number is even or odd.

```python
# Your code here
number = int(input("Enter a number: "))

# Check if the number is even or odd
if number % 2 == 0:
    print(f"{number} is even.")
else:
    print(f"{number} is odd.")
```

---

## 3. Nested Conditionals

You can also nest conditionals to check multiple conditions.

### Example
```python
age = 18

if age >= 18:
    print("You are an adult.")
    if age >= 65:
        print("You are a senior citizen.")
else:
    print("You are a minor.")
```

---

## 4. Exercise 2: Nested Conditionals

### Task
Write a program that determines whether a person is a child, adult, or senior based on their age.

```python
# Your code here
age = int(input("Enter your age: "))

if age < 18:
    print("You are a child.")
elif age < 65:
    print("You are an adult.")
else:
    print("You are a senior citizen.")
```

---

## 5. Flow Control: `if` with Logical Operators

You can use logical operators such as `and`, `or`, and `not` to combine multiple conditions.

### Example
```python
temperature = 30
is_raining = False

if temperature > 20 and not is_raining:
    print("It's a nice day!")
```

---

## 6. Exercise 3: Flow Control with Logical Operators

### Task
Write a program that checks if a person is eligible for a discount based on their age and membership status.

```python
# Your code here
age = int(input("Enter your age: "))
is_member = input("Are you a member? (yes/no): ").lower() == "yes"

if age < 18 or is_member:
    print("You are eligible for a discount.")
else:
    print("You are not eligible for a discount.")
```

---

## 7. Additional Resources

- [Python Official Documentation on Control Flow](https://docs.python.org/3/tutorial/controlflow.html)
- [W3Schools Python If...Else](https://www.w3schools.com/python/python_conditions.asp)
