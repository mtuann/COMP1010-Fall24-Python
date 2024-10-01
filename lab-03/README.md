### Lab 3: Functions & Modules

#### Objectives:
- Understand the concept of functions and their importance in programming.
- Learn how to define and call functions in Python.
- Understand how to pass arguments to functions and return values from them.
- Introduce the use of modules for organizing code and reusability.
- Practice importing and using built-in and custom modules in Python.

---

### Section 1: Introduction to Functions

A **function** is a block of code that performs a specific task. Functions allow us to reuse code, making programs easier to read and maintain.

#### 1.1 Defining a Function

We define functions using the `def` keyword. Here is a simple function that prints a greeting:

```python
# Defining a function
def greet():
    print("Hello, World!")
```

#### 1.2 Calling a Function

After defining a function, we can call it by using its name followed by parentheses:

```python
# Calling the greet function
greet()
```

---

### Section 2: Parameters and Arguments

Functions can take **parameters**, which are variables that hold the data passed to the function. These are specified in the parentheses when defining the function.

```python
# Function with a parameter
def greet_with_name(name):
    print(f"Hello, {name}!")
```

#### 2.1 Example of Calling a Function with Arguments

You can pass data (arguments) when calling the function:

```python
# Calling the function with an argument
greet_with_name("Alice")
```

#### 2.2 Default Arguments

You can define default values for parameters:

```python
# Function with default argument
def greet_with_default(name="Guest"):
    print(f"Hello, {name}!")
```

Now, you can call it with or without passing an argument:

```python
greet_with_default("Bob")  # Output: Hello, Bob!
greet_with_default()       # Output: Hello, Guest!
```

---

### Section 3: Return Values from Functions

Functions can return a result using the `return` statement:

```python
# Function that returns a value
def add(a, b):
    return a + b
```

When you call this function, you can store the returned value:

```python
result = add(5, 3)
print(result)  # Output: 8
```

---

### Section 4: Scope of Variables

Variables created inside a function are **local** to that function and cannot be accessed outside of it.

```python
def example():
    x = 10  # Local variable
    print(x)

example()
# print(x)  # This will cause an error since x is local to the example function
```

---

### Section 5: Modules in Python

A **module** is a file containing Python code that can define functions, classes, and variables. Python has many built-in modules, and you can create your own.

#### 5.1 Importing Built-in Modules

To use functions from a module, you need to import the module first:

```python
import math

# Using a function from the math module
result = math.sqrt(16)
print(result)  # Output: 4.0
```

#### 5.2 Importing Specific Functions from a Module

You can import only specific functions from a module:

```python
from math import sqrt

result = sqrt(25)
print(result)  # Output: 5.0
```

#### 5.3 Creating and Importing Custom Modules

You can also create your own module. Save the following code in a file named `mymodule.py`:

```python
# mymodule.py
def greet(name):
    return f"Hello, {name}!"
```

In another Python file, import and use this module:

```python
import mymodule

# Using the greet function from mymodule
print(mymodule.greet("Charlie"))  # Output: Hello, Charlie!
```

---

### Section 6: Using `if __name__ == "__main__"` in Modules

When writing reusable code, it’s common to include the following construct to ensure that code runs only when the file is executed directly, not when it's imported as a module:

```python
# mymodule.py
def greet(name):
    return f"Hello, {name}!"

if __name__ == "__main__":
    print(greet("Direct Run"))
```

---

### Section 7: Lab Exercises

#### Exercise 1: Temperature Conversion Function
- Write a function `celsius_to_fahrenheit(celsius)` that converts a temperature from Celsius to Fahrenheit.
- Write a function `fahrenheit_to_celsius(fahrenheit)` that converts Fahrenheit to Celsius.

#### Exercise 2: Custom Math Module
- Create a module named `mymath.py` with the following functions:
  - `add(a, b)`: Returns the sum of two numbers.
  - `subtract(a, b)`: Returns the difference between two numbers.
  - `multiply(a, b)`: Returns the product of two numbers.
  - `divide(a, b)`: Returns the quotient of two numbers.
- Import and use the functions in another script.

#### Exercise 3: Simple Calculator Using Functions
- Create a program that asks the user for two numbers and an operator (`+`, `-`, `*`, `/`).
- Use functions to perform the desired calculation and display the result.

---

### Section 8: Best Practices for Functions and Modules

- **Use Descriptive Names**: Choose function names that describe what they do.
- **Keep Functions Small**: Each function should perform a single task.
- **Use Comments and Docstrings**: Provide explanations for what your functions do, especially for more complex code.
- **Modularize Your Code**: Break down large programs into smaller modules for better organization and reusability.