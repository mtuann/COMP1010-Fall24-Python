# Final Revision Class Notebook

### Overview
This notebook provides a comprehensive review of the key concepts covered in Labs 8 to 14, preparing students for the final exam. Each section includes definitions, code examples, and practice questions.

---

## Lab 8: Tuples and Dictionaries

### 1. Tuples
A **tuple** is an immutable ordered collection of elements. Tuples are defined by placing elements in parentheses.

**Example:**
```python
my_tuple = (1, 2, 3, "apple")
print(my_tuple[0])  # Output: 1
```

### 2. Dictionaries
A **dictionary** is an unordered collection of key-value pairs. It allows for fast retrieval of values based on their keys.

**Example:**
```python
my_dict = {"name": "Alice", "age": 25}
print(my_dict["name"])  # Output: Alice
```

### Practice Questions
1. Create a tuple with your three favorite fruits and print the second fruit.
2. Write a program that counts the frequency of each character in a string using a dictionary.
3. Explain the differences between tuples and lists.

---

## Lab 9: Sorting Algorithms

### 1. Introduction to Sorting
Sorting algorithms arrange elements in a specific order (ascending or descending). Common sorting algorithms include Bubble Sort, Insertion Sort, and Quick Sort.

### 2. Bubble Sort
A simple comparison-based sorting algorithm that repeatedly steps through the list, compares adjacent elements, and swaps them if they are in the wrong order.

**Example:**
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr

numbers = [64, 34, 25, 12, 22, 11, 90]
print(bubble_sort(numbers))  # Output: Sorted list
```

### 3. Quick Sort
A more efficient sorting algorithm that follows the divide-and-conquer principle.

**Example:**
```python
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quick_sort(left) + middle + quick_sort(right)

print(quick_sort(numbers))  # Output: Sorted list
```

### Practice Questions
1. Implement the Insertion Sort algorithm.
2. Compare the time complexity of Bubble Sort and Quick Sort.
3. Write a function that sorts a list of strings in alphabetical order.

---

## Lab 10: Sequential and Recursive Algorithms

### 1. Sequential Algorithms
Sequential algorithms perform tasks in a linear step-by-step manner.

**Example:**
```python
def find_max(arr):
    max_value = arr[0]
    for num in arr:
        if num > max_value:
            max_value = num
    return max_value
```

### 2. Recursive Algorithms
Recursive algorithms solve problems by calling themselves with smaller inputs.

**Example:**
```python
def factorial(n):
    if n == 0:
        return 1
    else:
        return n * factorial(n - 1)

print(factorial(5))  # Output: 120
```

### Practice Questions
1. Write a recursive function to compute the nth Fibonacci number.
2. Discuss the advantages and disadvantages of using recursion.
3. Explain the concept of a base case in a recursive function.

---

## Lab 11: Basic OOP Concepts

### 1. Object-Oriented Programming (OOP)
OOP is a programming paradigm based on the concept of "objects," which can contain data and methods.

### 2. Classes and Objects
A **class** is a blueprint for creating objects. An **object** is an instance of a class.

**Example:**
```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("Alice", 30)
print(person1.name)  # Output: Alice
```

### Practice Questions
1. Define a class `Rectangle` with methods to calculate its area and perimeter.
2. What is the difference between a class variable and an instance variable?
3. Explain the concept of encapsulation in OOP.

---

## Lab 12: Object-oriented Programming (Subclasses and Inheritance)

### 1. Inheritance
Inheritance allows a class (child class) to inherit attributes and methods from another class (parent class).

**Example:**
```python
class Animal:
    def speak(self):
        return "Animal speaks"

class Dog(Animal):
    def bark(self):
        return "Woof!"

dog = Dog()
print(dog.speak())  # Output: Animal speaks
```

### 2. Subclasses
A subclass can override methods of its parent class.

### Practice Questions
1. Create a class `Car` that inherits from a class `Vehicle`.
2. What is method overriding, and why is it used?
3. Discuss the advantages of using inheritance in OOP.

---

## Lab 13: Python Tools for Machine Learning

### 1. Introduction to Machine Learning
Machine learning involves using algorithms and statistical models to enable computers to perform specific tasks without explicit programming.

### 2. Key Libraries
- **NumPy**: For numerical operations and handling arrays.
- **Pandas**: For data manipulation and analysis.
- **Matplotlib**: For data visualization.
- **Scikit-learn**: For machine learning algorithms.

**Example of using Pandas:**
```python
import pandas as pd

data = {'Name': ['Alice', 'Bob'], 'Age': [30, 25]}
df = pd.DataFrame(data)
print(df)
```

### Practice Questions
1. Explain the purpose of NumPy in machine learning.
2. Write a simple example of loading a dataset using Pandas.
3. Discuss the role of data preprocessing in machine learning.

---

## Lab 14: GUI Frameworks in Python

### 1. Introduction to GUI Programming
Graphical User Interface (GUI) programming allows users to interact with applications through graphical elements.

### 2. Tkinter
Tkinter is the standard GUI toolkit for Python, providing a simple way to create windows, buttons, and other GUI components.

**Example:**
```python
import tkinter as tk

def on_button_click():
    print("Button clicked!")

root = tk.Tk()
button = tk.Button(root, text="Click Me", command=on_button_click)
button.pack()
root.mainloop()
```

### Practice Questions
1. Create a simple Tkinter application with a button that displays a message when clicked.
2. Discuss the main components of a GUI application.
3. Explain how event-driven programming works in GUI frameworks.

---

### Tips for Final Exam Preparation
- Review key concepts and practice coding exercises related to each topic.
- Ensure you understand how to apply OOP principles in practical scenarios.
- Work on sample problems and previous assignments to reinforce learning.