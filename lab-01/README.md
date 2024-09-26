# Lab 1: Introduction to Programming in Python

Welcome to the first lab of your Python programming journey! In this lab, we will cover the basics of Python syntax, variables, data types, and simple input/output operations. These concepts are the foundation of programming and will be used throughout this course.

---

## Objectives:
- Understand basic Python syntax
- Learn how to use variables and data types
- Practice basic input and output operations
- Write your first Python program

---

## 1. Introduction to Python

Python is a high-level, interpreted programming language known for its simplicity and readability. Let's get started by writing and running our first Python program.

```python
# This is a comment
# Let's print 'Hello, World!' to the console
print("Hello, World!")
```

In Python, we use the `print()` function to display output. The text inside the quotation marks will be printed to the console.

---

## 2. Variables and Data Types

A **variable** is a container that holds data. In Python, you don't need to declare the type of a variable explicitly. Let's see how to define and use variables.

### Example:

```python
# Assigning values to variables
name = "Alice"
age = 20
is_student = True

# Printing variable values
print("Name:", name)
print("Age:", age)
print("Is a student:", is_student)
```

### Task 1:
- Create variables to store your name, age, and whether you are a student or not.
- Print them using the `print()` function.

### Explanation:
- `name` is a **string** (a sequence of characters).
- `age` is an **integer** (a whole number).
- `is_student` is a **boolean** (True or False).

---

## 3. Basic Data Types in Python

Python has several built-in data types that are commonly used in programming. These include:

- **int**: Whole numbers (e.g., `5`, `100`)
- **float**: Numbers with decimal points (e.g., `3.14`, `0.001`)
- **str**: Strings, which are sequences of characters (e.g., `"hello"`, `"123"`)
- **bool**: Boolean values (`True`, `False`)

### Example:

```python
# Different data types
x = 10          # int
y = 3.14        # float
z = "Python"    # str
flag = True     # bool

print(x, y, z, flag)
```

### Task 2:
- Create variables for an integer, a floating-point number, a string, and a boolean.
- Print the values of these variables.

---

## 4. Simple Input/Output Operations

Python can take input from the user using the `input()` function. The `input()` function reads a line from the user and returns it as a string.

### Example:

```python
# Taking input from the user
name = input("Enter your name: ")
print("Hello, " + name + "!")
```

The `input()` function always returns a string, so if you want to convert it to another data type (like an integer), you need to cast it using the appropriate function (e.g., `int()`, `float()`).

### Example:

```python
# Taking numerical input
age = int(input("Enter your age: "))
print("You are", age, "years old.")
```

### Task 3:
- Ask the user for their name and age.
- Print a message that says, "Hello, [name]! You are [age] years old."

---

## 5. Basic Arithmetic Operations

Python can perform arithmetic operations like addition, subtraction, multiplication, and division. Here's a quick overview of the basic operators:

- `+` : Addition
- `-` : Subtraction
- `*` : Multiplication
- `/` : Division
- `//` : Floor division (returns the quotient)
- `%` : Modulus (returns the remainder)
- `**` : Exponentiation

### Example:

```python
# Arithmetic operations
a = 10
b = 3

print("Addition:", a + b)
print("Subtraction:", a - b)
print("Multiplication:", a * b)
print("Division:", a / b)
print("Floor Division:", a // b)
print("Modulus:", a % b)
print("Exponentiation:", a ** b)
```

### Task 4:
- Ask the user for two numbers and perform the following operations: addition, subtraction, multiplication, and division.
- Display the results to the user.

---

## 6. Conclusion

In this lab, you learned how to:
- Write basic Python programs.
- Use variables to store and manipulate data.
- Take user input and display output.
- Perform arithmetic operations.

Continue practicing by experimenting with different data types and writing small programs to reinforce what you've learned.

---

## Homework:
1. Write a program that asks the user for the length and width of a rectangle and then calculates and prints the area and perimeter.
2. Write a program that asks the user for a number and checks if it is even or odd.

---