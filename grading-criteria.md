There are **five main criteria** for grading Python programs in this course. These criteria help evaluate the quality of the code based on different aspects, such as functionality, structure, problem-solving, efficiency, and documentation. Below are examples of each criterion to illustrate what is expected in a well-written Python program.

### 1. **Code Functionality**

This refers to whether the program works as intended and solves the problem. A functional program produces the correct output based on the input.

#### Example: Check if a number is even or odd
```python
# Functionality: The program works as intended and checks if a number is even or odd

number = int(input("Enter a number: "))

if number % 2 == 0:
    print(f"{number} is even.")
else:
    print(f"{number} is odd.")
```

**Explanation:** This program successfully checks whether the user input is even or odd, producing the correct output.

---

### 2. **Code Structure and Organization**

This refers to how well the code is organized, including proper use of functions, separation of logic, and readability. Well-structured code is easier to maintain and understand.

#### Example: Organized structure with functions
```python
# Structure: The program is organized with functions that separate logic into clear blocks

def is_even(number):
    """Check if the number is even."""
    return number % 2 == 0

def main():
    number = int(input("Enter a number: "))
    
    if is_even(number):
        print(f"{number} is even.")
    else:
        print(f"{number} is odd.")

# Start the program
main()
```

**Explanation:** This version uses functions to separate the logic of checking even/odd from user interaction, making the code more organized.

---

### 3. **Problem Solving and Logic**

This refers to how well the problem is broken down and how logical steps are followed to achieve the correct solution. Programs should demonstrate clear and effective problem-solving.

#### Example: Check if a year is a leap year
```python
# Problem Solving: Break down the leap year problem into logical conditions

def is_leap_year(year):
    """Return True if the year is a leap year, False otherwise."""
    if year % 4 == 0:
        if year % 100 == 0:
            if year % 400 == 0:
                return True
            else:
                return False
        else:
            return True
    else:
        return False

year = int(input("Enter a year: "))
if is_leap_year(year):
    print(f"{year} is a leap year.")
else:
    print(f"{year} is not a leap year.")
```

**Explanation:** The problem-solving approach is clear—breaking the leap year problem into three nested conditions following logical steps.

---

### 4. **Code Efficiency**

This refers to how well the code performs, especially when dealing with large inputs. Efficient code avoids unnecessary operations and minimizes time/space complexity.

#### Example: Optimized leap year check (avoiding nested conditions)
```python
# Efficiency: Simplified logic for better performance

def is_leap_year(year):
    """Return True if the year is a leap year, False otherwise."""
    return (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0)

year = int(input("Enter a year: "))
if is_leap_year(year):
    print(f"{year} is a leap year.")
else:
    print(f"{year} is not a leap year.")
```

**Explanation:** This version reduces unnecessary nesting by combining conditions into a single return statement, making the code more efficient.

---

### 5. **Documentation and Comments**

This refers to how well the code is documented. Good comments and documentation explain the purpose of the code and help others (or your future self) understand it quickly.

#### Example: Well-documented program with comments
```python
# Documentation: Clear and helpful comments explain the code

def is_even(number: int) -> bool:
    """
    Check if a number is even.
    
    Args:
        number (int): The number to check.
        
    Returns:
        bool: True if the number is even, False otherwise.
    """
    # Return True if number is divisible by 2, otherwise False
    return number % 2 == 0

def main():
    """
    Main function to get user input and check if the number is even or odd.
    """
    # Ask the user for input
    number = int(input("Enter a number: "))
    
    # Check if the number is even or odd and print the result
    if is_even(number):
        print(f"{number} is even.")
    else:
        print(f"{number} is odd.")

# Call the main function to start the program
main()
```

**Explanation:** The program is thoroughly documented, including docstrings for each function and comments explaining each step.

---

### Summary of the Criteria:
1. **Code Functionality:** The program works as expected.
2. **Code Structure and Organization:** The code is well-organized, often with functions separating tasks.
3. **Problem Solving and Logic:** The problem is broken down logically, and steps are clearly followed to reach the solution.
4. **Code Efficiency:** The code is written in a way that avoids unnecessary operations and is optimized for performance.
5. **Documentation and Comments:** The code is well-documented, making it easy to understand and maintain.
