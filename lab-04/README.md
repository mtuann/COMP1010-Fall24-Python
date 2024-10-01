### Lab 04: Strings, Testing, and Debugging

#### Objectives
- Understand string manipulation in Python.
- Learn how to test functions and code segments.
- Explore debugging techniques to identify and fix errors in code.

---

### Table of Contents
1. [Introduction to Strings](#introduction-to-strings)
2. [String Manipulation Techniques](#string-manipulation-techniques)
3. [Testing Functions](#testing-functions)
4. [Debugging Techniques](#debugging-techniques)
5. [Practice Exercises](#practice-exercises)
6. [Using Breakpoints in PyCharm](#using-breakpoints-in-pycharm)

---

## Introduction to Strings
Strings are sequences of characters enclosed in quotes. They are used to represent text in Python.

### Example:
```python
# Creating strings
string1 = "Hello, World!"
string2 = 'Python is fun!'
print(string1)
print(string2)
```

### String Characteristics:
- Strings are immutable: Once created, they cannot be changed.
- Strings can be indexed and sliced.

## String Manipulation Techniques
Python provides various methods to manipulate strings:

### 1. Accessing Characters:
```python
my_string = "Hello"
print(my_string[0])  # H
print(my_string[-1])  # o
```

### 2. Slicing Strings:
```python
print(my_string[1:4])  # ell
print(my_string[:3])    # Hel
print(my_string[2:])    # llo
```

### 3. String Methods:
- **`len()`**: Returns the length of the string.
- **`.lower()`**: Converts string to lowercase.
- **`.upper()`**: Converts string to uppercase.
- **`.replace(old, new)`**: Replaces substrings.
- **`.split(separator)`**: Splits string into a list.
- **`.join(iterable)`**: Joins elements of an iterable into a string.

### Example:
```python
sample_string = "Python Programming"
print("Length:", len(sample_string))  # 18
print("Lowercase:", sample_string.lower())  # python programming
print("Uppercase:", sample_string.upper())  # PYTHON PROGRAMMING
print("Replaced:", sample_string.replace("Programming", "Language"))  # Python Language
print("Split:", sample_string.split(" "))  # ['Python', 'Programming']
```

## Testing Functions
Testing is an essential part of programming to ensure code works as expected.

### 1. Writing Test Cases
You can use assertions to test the expected outcomes of functions.

### Example:
```python
def add(a, b):
    return a + b

# Test cases
assert add(2, 3) == 5, "Test Case 1 Failed"
assert add(-1, 1) == 0, "Test Case 2 Failed"
assert add(0, 0) == 0, "Test Case 3 Failed"

print("All test cases pass")
```

### 2. Using `unittest` Framework
The `unittest` module provides a framework for creating and running tests.

### Example:
```python
import unittest

def multiply(a, b):
    return a * b

class TestMathFunctions(unittest.TestCase):
    def test_multiply(self):
        self.assertEqual(multiply(3, 4), 12)
        self.assertEqual(multiply(-1, 1), -1)

if __name__ == '__main__':
    unittest.main()
```

## Debugging Techniques
Debugging is the process of identifying and fixing errors in your code.

### 1. Using Print Statements
You can insert print statements to check variable values at different stages.

### Example:
```python
def divide(a, b):
    print(f"Dividing {a} by {b}")
    return a / b

result = divide(10, 2)
print("Result:", result)
```

### 2. Using Python Debugger (`pdb`)
Python includes a built-in debugger that allows you to set breakpoints, step through code, and inspect variable states.

### Example:
```python
import pdb

def calculate_area(radius):
    pdb.set_trace()  # Set a breakpoint
    return 3.14 * radius ** 2

area = calculate_area(5)
print("Area:", area)
```

## Practice Exercises
1. **String Manipulation Exercise**:
   - Write a function that takes a string as input and returns the string reversed.

   ```python
   def reverse_string(s):
       return s[::-1]

   print(reverse_string("Hello"))  # Output: olleH
   ```

2. **Testing Exercise**:
   - Write a function that checks if a string is a palindrome and create test cases to verify it.

   ```python
   def is_palindrome(s):
       return s == s[::-1]

   # Test cases
   assert is_palindrome("radar") == True
   assert is_palindrome("hello") == False
   ```

3. **Debugging Exercise**:
   - Create a function that calculates the factorial of a number. Intentionally introduce an error, then use print statements or `pdb` to debug it.

   ```python
   def factorial(n):
       if n == 0:
           return 1
       return n * factorial(n - 1)

   print(factorial(5))  # Output: 120
   ```


---

## Using Breakpoints in PyCharm

### Step 1: Open Your Project
1. Launch **PyCharm** and open your existing project or create a new one.

### Step 2: Write or Open Your Code
1. Write your Python code or open the existing file you want to debug.

   Example:
   ```python
   def factorial(n):
       if n == 0:
           return 1
       return n * factorial(n - 1)

   print(factorial(5))  # This will calculate 5! (120)
   ```

### Step 3: Set a Breakpoint
1. **Set a Breakpoint**: Click in the gutter (the left margin) next to the line number where you want the program to pause execution. A red dot will appear, indicating a breakpoint has been set.
   
2. You can set multiple breakpoints if needed.

### Step 4: Start the Debugger
1. **Run in Debug Mode**: Right-click on your Python file in the Project tool window or the editor and select **Debug 'your_script_name'**. Alternatively, you can click on the green bug icon in the top right corner of the PyCharm window.

### Step 5: Debugging Interface
1. Once the debugger starts, the program will run until it hits the first breakpoint.
2. When execution pauses, the **Debug** tool window will appear at the bottom of the PyCharm interface. This window provides various options and information:
   - **Variables**: Shows the current variable values.
   - **Frames**: Displays the call stack, allowing you to navigate through the function calls.
   - **Watches**: You can add expressions to monitor their values as you step through the code.

### Step 6: Step Through the Code
1. **Step Over (F8)**: Execute the current line and move to the next line in the same function. Use this when you want to skip over function calls without entering them.
2. **Step Into (F7)**: If the current line contains a function call, this will take you into that function to debug it line by line.
3. **Step Out (Shift + F8)**: Finish the current function and return to the calling function.
4. **Resume Program (F9)**: Continue running the code until the next breakpoint or until the program finishes.

### Step 7: Inspect Variables
1. **Hover Over Variables**: While execution is paused, you can hover over variables in your code to see their current values.
2. **Watch Variables**: In the **Watches** panel, you can add expressions or variable names to monitor their values continuously.

### Step 8: Modify Variables
1. While the execution is paused, you can change the value of variables in the **Variables** panel. This can help you test different scenarios without restarting the program.

### Step 9: Remove Breakpoints
1. To remove a breakpoint, click on the red dot in the gutter again, or right-click the line and select **Remove Breakpoint**.
2. You can also disable breakpoints without removing them by clicking on the **Breakpoints** icon in the Debugger panel and unchecking the specific breakpoint.

## Additional Tips
- **Conditional Breakpoints**: Right-click on a breakpoint and choose **Edit Breakpoint** to add conditions. The program will only pause if the condition evaluates to `True`.
- **Log Message Breakpoints**: You can configure a breakpoint to log a message to the console instead of pausing execution.
