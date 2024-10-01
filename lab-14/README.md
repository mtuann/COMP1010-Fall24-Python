### Lab 14: GUI Frameworks

#### Objectives:
- Introduce students to basic graphical user interface (GUI) development in Python.
- Learn how to create windows, buttons, labels, and other widgets using **Tkinter**, Python's standard GUI library.
- Build a simple GUI application with user interaction.

---

### Section 1: Introduction to GUI Development

A **Graphical User Interface (GUI)** allows users to interact with applications using graphical elements like windows, buttons, text boxes, etc., instead of command-line inputs. Python’s `Tkinter` module makes it easy to develop GUIs.

---

### Section 2: Setting up Tkinter

Tkinter is Python's de-facto standard for creating GUIs. It comes pre-installed with Python, so no additional installation is required.

To import Tkinter, use:

```python
import tkinter as tk
```

Let's start by creating a simple window.

---

### Section 3: Creating a Basic Window

```python
import tkinter as tk

# Creating the main window
root = tk.Tk()

# Setting window title
root.title("My First GUI")

# Setting window size (width x height)
root.geometry("300x200")

# Starting the event loop
root.mainloop()
```

This code creates a basic window titled “My First GUI” with dimensions 300x200.

---

### Section 4: Adding Widgets

#### 4.1 Labels
Labels are used to display text on the window.

```python
# Adding a label to the window
label = tk.Label(root, text="Hello, World!")
label.pack()  # Pack places the widget in the window
```

#### 4.2 Buttons
Buttons allow users to trigger actions. We’ll create a button that prints a message when clicked.

```python
# Function to handle button click
def on_click():
    print("Button clicked!")

# Adding a button to the window
button = tk.Button(root, text="Click Me", command=on_click)
button.pack()
```

#### 4.3 Text Entry
A text entry widget allows users to input data.

```python
# Adding a text entry widget
entry = tk.Entry(root)
entry.pack()

# Adding a button to retrieve the input
def show_input():
    print("User entered:", entry.get())

button = tk.Button(root, text="Show Input", command=show_input)
button.pack()
```

---

### Section 5: Organizing Layouts

Tkinter provides several ways to organize widgets in the window using different geometry managers: `pack()`, `grid()`, and `place()`.

#### 5.1 Using `pack()`
The `pack()` method places widgets in the window in sequence, from top to bottom or left to right.

```python
label1 = tk.Label(root, text="Label 1")
label1.pack()

label2 = tk.Label(root, text="Label 2")
label2.pack()
```

#### 5.2 Using `grid()`
The `grid()` method organizes widgets in a table-like structure.

```python
label1 = tk.Label(root, text="Row 0, Column 0")
label1.grid(row=0, column=0)

label2 = tk.Label(root, text="Row 1, Column 1")
label2.grid(row=1, column=1)
```

#### 5.3 Using `place()`
The `place()` method positions widgets at specific x and y coordinates.

```python
label = tk.Label(root, text="Placed Label")
label.place(x=50, y=50)
```

---

### Section 6: Building a Simple Calculator App

Let’s combine what we've learned to build a simple calculator GUI.

```python
# Function to evaluate the expression
def evaluate():
    result = eval(entry.get())  # Evaluating the input as a math expression
    label_result.config(text="Result: " + str(result))

# Create the window
root = tk.Tk()
root.title("Simple Calculator")

# Create an entry widget for the user to input an expression
entry = tk.Entry(root)
entry.pack()

# Create a button to trigger the evaluation
button = tk.Button(root, text="Evaluate", command=evaluate)
button.pack()

# Label to show the result
label_result = tk.Label(root, text="Result: ")
label_result.pack()

# Run the event loop
root.mainloop()
```

This code creates a simple calculator that evaluates mathematical expressions entered by the user.

---

### Section 7: Lab Exercises

#### Exercise 1: Create a Currency Converter
- Build a GUI that converts between different currencies (e.g., USD to EUR).
- Use `tk.Entry` for user input and `tk.Button` to trigger the conversion.
- Display the result using a `tk.Label`.

#### Exercise 2: Build a To-Do List Application
- Create a GUI where users can add tasks to a to-do list.
- Use `tk.Entry` to input the task and `tk.Button` to add it to a list.
- Display the list using a series of `tk.Label` widgets or in a `tk.Listbox`.

---

### Section 8: Advanced GUI with Tkinter

#### 8.1 Message Box
Tkinter has built-in support for message boxes to show alert dialogs.

```python
from tkinter import messagebox

# Display an info message box
messagebox.showinfo("Information", "This is a message box")
```

#### 8.2 File Dialog
You can also create file dialogs for opening or saving files.

```python
from tkinter import filedialog

# Function to open a file dialog
def open_file():
    file_path = filedialog.askopenfilename()
    print("Selected file:", file_path)

# Button to trigger the file dialog
button = tk.Button(root, text="Open File", command=open_file)
button.pack()
```