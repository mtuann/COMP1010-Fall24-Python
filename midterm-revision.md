# Midterm Revision Class Notebook

### Overview
This notebook provides a comprehensive review of the key concepts covered in Labs 2 to 7, preparing students for the midterm exam. Each section includes definitions, code examples, and practice questions.

---

## Lab 2: Expressions, Variable Assignments, and Logical Operators

### 1. Expressions
An expression is a combination of values and operators that can be evaluated to produce another value.

**Example:**
```python
# Arithmetic expressions
result = (5 + 3) * 2
```

### 2. Variable Assignments
Variables are used to store data values. You can assign values to variables using the `=` operator.

**Example:**
```python
x = 10
y = 5
```

### 3. Logical Operators
Logical operators are used to combine conditional statements:
- `and`
- `or`
- `not`

**Example:**
```python
a = True
b = False

# Using logical operators
if a and not b:
    print("Condition met")
```

### Practice Questions
1. What is the output of the following expression: `3 * (2 + 5)`?
2. Write a variable assignment for your age and print it.
3. Create a logical expression using `and`, `or`, and `not`.

---

## Lab 3: Functions & Modules

### 1. Functions
Functions are reusable blocks of code that perform a specific task. They are defined using the `def` keyword.

**Example:**
```python
def add(a, b):
    return a + b
```

### 2. Modules
Modules are files containing Python code that can define functions, classes, and variables. Use the `import` statement to include a module in your program.

**Example:**
```python
import math
print(math.sqrt(16))
```

### Practice Questions
1. Define a function `multiply(a, b)` that returns the product of `a` and `b`.
2. What will happen if you try to use a function before defining it?
3. Create a simple module that includes a function to calculate the area of a rectangle.

---

## Lab 4: Strings, Testing and Debugging

### 1. Strings
Strings are sequences of characters enclosed in quotes. They can be manipulated using various methods.

**Example:**
```python
text = "Hello, World!"
print(text.lower())  # Output: hello, world!
```

### 2. Testing and Debugging
Testing ensures your code works as expected. Debugging helps identify and fix errors.

**Example:**
```python
# Testing a function
def is_even(n):
    return n % 2 == 0

# Debugging
print(is_even(4))  # Expected: True
print(is_even(3))  # Expected: False
```

### Practice Questions
1. Write a string that contains your name and print its length.
2. Create a function that checks if a string is a palindrome.
3. Discuss a debugging technique you can use when your code doesn’t work as expected.

---

## Lab 5: Conditionals and Flow Control

### 1. Conditionals
Conditionals allow you to execute code based on whether a condition is true or false.

**Example:**
```python
age = 18
if age >= 18:
    print("You are an adult.")
else:
    print("You are a minor.")
```

### 2. Flow Control
Flow control statements like `if`, `elif`, and `else` help manage the flow of execution.

**Example:**
```python
score = 85
if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
else:
    print("Grade: C")
```

### Practice Questions
1. Write a program that checks whether a number is positive, negative, or zero.
2. Create a grading system that assigns letter grades based on a numeric score.
3. How does the `elif` statement differ from the `if` statement?

---

## Lab 6: Lists and Objects

### 1. Lists
Lists are ordered collections of items that can be of different types. You can create and manipulate lists using various methods.

**Example:**
```python
fruits = ["apple", "banana", "cherry"]
fruits.append("orange")
```

### 2. Objects
Objects are instances of classes, which can encapsulate data and functionality.

**Example:**
```python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        return "Woof!"

my_dog = Dog("Rex")
print(my_dog.bark())
```

### Practice Questions
1. Create a list of your favorite colors and print the first color.
2. Define a class `Car` with attributes for make, model, and year.
3. What are some common list methods in Python?

---

## Lab 7: Lists, Iteration, and Loops

### 1. Iteration
Iteration allows you to execute a block of code multiple times. The `for` and `while` loops are commonly used.

**Example of a `for` loop:**
```python
for fruit in fruits:
    print(fruit)
```

**Example of a `while` loop:**
```python
count = 0
while count < 5:
    print(count)
    count += 1
```

### Practice Questions
1. Write a `for` loop to print all even numbers from 1 to 20.
2. Create a `while` loop that sums numbers from 1 to 100.
3. Explain the difference between a `for` loop and a `while` loop.

---

### Tips for Midterm Preparation
- Review and practice coding exercises related to each topic.
- Ensure you understand the concepts and can explain them in your own words.
- Work on sample problems and previous assignments to reinforce learning.