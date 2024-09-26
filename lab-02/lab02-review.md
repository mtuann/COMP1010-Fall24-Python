# Lab 02: Expressions, Variables, and Logical Operators

Welcome to Lab 2! In this lab, we will explore expressions, variables, and logical operators in Python. By the end of this lab, you'll be able to write more complex programs with conditions and logic.

---

## Objectives:
- Understand how to use expressions in Python
- Learn the different logical operators
- Use conditions to control program flow
- Practice with variables and expressions

---

## 1. Variables and Expressions

In Python, an **expression** is a combination of values and operators that evaluates to a value. Let's see some examples.

### Example:

```python
# Basic arithmetic expression
x = 10
y = 5

result = (x + y) * 2  # Parentheses are used to control the order of operations
print("The result is:", result)
```

### Task 1:
- Define two variables `a` and `b`.
- Write an expression that adds these two numbers and multiplies the result by 3.
- Print the result.

---

## 2. Logical Operators

Python supports the following logical operators:
- `and`: Returns `True` if both statements are true
- `or`: Returns `True` if one of the statements is true
- `not`: Reverses the result, returns `False` if the result is true

These operators are used with **Boolean** values (`True` or `False`).

### Example:

```python
# Using logical operators
a = True
b = False

print("a and b:", a and b)  # False because both are not True
print("a or b:", a or b)    # True because one is True
print("not a:", not a)      # False because a is True
```

### Task 2:
- Create two variables with Boolean values.
- Print the result of `and`, `or`, and `not` operations on these values.

---

## 3. Comparison Operators

Comparison operators are used to compare two values. They return either `True` or `False`.

- `==`: Equal to
- `!=`: Not equal to
- `>`: Greater than
- `<`: Less than
- `>=`: Greater than or equal to
- `<=`: Less than or equal to

### Example:

```python
# Comparison operators
x = 10
y = 20

print("x == y:", x == y)  # False because 10 is not equal to 20
print("x != y:", x != y)  # True because 10 is not equal to 20
print("x > y:", x > y)    # False because 10 is less than 20
print("x < y:", x < y)    # True because 10 is less than 20
```

### Task 3:
- Write a Python program that asks the user for two numbers.
- Compare the two numbers using the comparison operators and print the results.

---

## 4. Combining Logical and Comparison Operators

You can combine logical and comparison operators to write more complex expressions.

### Example:

```python
# Combining logical and comparison operators
age = 25
has_license = True

if age >= 18 and has_license:
    print("You can drive!")
else:
    print("You cannot drive.")
```

### Task 4:
- Write a program that checks if a person is eligible to vote.
- Ask the user for their age and check if they are 18 or older.

---

## 5. Conditional Statements (if, elif, else)

Conditional statements allow us to execute a block of code only if a certain condition is true. Python supports the following conditional statements:
- `if`: Executes a block of code if the condition is true
- `elif`: Checks another condition if the previous condition is false
- `else`: Executes a block of code if all the previous conditions are false

### Example:

```python
# Using if, elif, and else
temperature = 30

if temperature > 35:
    print("It's hot!")
elif temperature > 20:
    print("It's warm.")
else:
    print("It's cold.")
```

### Task 5:
- Write a program that takes the temperature as input from the user.
- Print "Hot" if the temperature is above 35, "Warm" if it is between 20 and 35, and "Cold" if it is 20 or below.

---

## 6. Practical Application: Even or Odd Checker

Let's combine what we've learned into a practical example. We will write a program that checks whether a number is even or odd.

### Example:

```python
# Checking if a number is even or odd
num = int(input("Enter a number: "))

if num % 2 == 0:
    print(num, "is even.")
else:
    print(num, "is odd.")
```

### Task 6:
- Modify the above program to check if a number is divisible by both 2 and 3.
- Print an appropriate message for each case.

---

## 7. Conclusion

In this lab, you learned how to:
- Work with logical operators and comparison operators.
- Write conditional statements using `if`, `elif`, and `else`.
- Combine multiple conditions to control the flow of your program.

Keep practicing these concepts, as they form the foundation for decision-making in Python programming.

---

## Homework:
1. Write a program that takes three numbers as input from the user and prints the largest one.
2. Write a program that checks whether a year is a leap year or not. A leap year is divisible by 4 but not divisible by 100 unless it is also divisible by 400.

---

**End of Lab 2**

---

### Key Concepts to Emphasize:
1. **Expressions**: Demonstrate how Python evaluates expressions.
2. **Logical Operators**: Teach students how to use `and`, `or`, and `not` to build logical conditions.
3. **Comparison Operators**: Show how to compare values and make decisions.
4. **Conditional Statements**: Emphasize the importance of control flow using `if`, `elif`, and `else`.
