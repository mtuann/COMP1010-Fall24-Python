### Lab 06: Lists and Objects

#### Objectives:
- Understand how to create and manipulate lists in Python.
- Practice using list methods and accessing elements.
- Introduction to objects and methods in Python.

---

### Section 1: Working with Lists

#### 1.1 Creating a List
A **list** is a collection of items that are ordered and changeable. You can create a list using square brackets.

```python
# Creating a list of fruits
fruits = ["apple", "banana", "cherry", "date", "elderberry"]
print("List of fruits:", fruits)
```

#### 1.2 Accessing List Elements
Lists are zero-indexed, meaning the first element is at index `0`. You can also use negative indices to access elements from the end of the list.

```python
# Access the first and the last element of the list
print("First fruit:", fruits[0])
print("Last fruit:", fruits[-1])
```

#### 1.3 Modifying List Elements
Lists are **mutable**, which means you can change their elements by assigning new values.

```python
# Changing the second fruit to blueberry
fruits[1] = "blueberry"
print("Updated list of fruits:", fruits)
```

#### 1.4 List Slicing
You can use **slicing** to access a range of elements in the list.

```python
# Slicing the list to get a subset of elements
print("First three fruits:", fruits[:3])  # From index 0 to 2
print("Fruits from index 2 to 4:", fruits[2:4])  # From index 2 to 3
```

#### 1.5 Adding Elements to a List
To add new elements, use `append()` to add to the end of the list or `insert()` to add at a specific position.

```python
# Adding an element at the end of the list
fruits.append("fig")
print("List after appending fig:", fruits)

# Inserting an element at a specific index
fruits.insert(2, "grape")
print("List after inserting grape at index 2:", fruits)
```

#### 1.6 Removing Elements from a List
You can remove elements using `remove()`, `pop()`, or the `del` keyword.

```python
# Removing an element by value
fruits.remove("date")
print("List after removing date:", fruits)

# Removing an element by index and returning it
removed_fruit = fruits.pop(1)
print("Removed fruit:", removed_fruit)
print("List after pop:", fruits)
```

#### 1.7 List Length
The `len()` function returns the number of elements in a list.

```python
# Getting the length of the list
print("Length of the list:", len(fruits))
```

#### 1.8 Iterating Over a List
You can use a `for` loop to iterate over the elements of a list.

```python
# Iterating over the list and printing each fruit
print("Fruits in the list:")
for fruit in fruits:
    print(fruit)
```

---

### Section 2: Objects in Python

#### 2.1 Introduction to Objects and Classes
In Python, everything is an **object**, and objects belong to **classes**. You can define your own class using the `class` keyword.

```python
# Defining a simple class to represent a Book object
class Book:
    def __init__(self, title, author, pages):
        self.title = title
        self.author = author
        self.pages = pages

    # A method to get information about the book
    def get_info(self):
        return f"{self.title} by {self.author}, {self.pages} pages"

# Creating an instance of the Book class
book1 = Book("1984", "George Orwell", 328)
print("Book info:", book1.get_info())
```

#### 2.2 Attributes and Methods
Attributes are variables that belong to an object, while methods are functions that belong to an object. You can access attributes directly or use methods to manipulate them.

```python
# Accessing attributes directly
print("Book title:", book1.title)
print("Book author:", book1.author)
print("Book pages:", book1.pages)

# Modifying an attribute
book1.pages = 350
print("Updated book info:", book1.get_info())
```

#### 2.3 Creating Multiple Instances
You can create multiple instances of a class, each with its own attributes.

```python
# Creating multiple instances of the Book class
book2 = Book("To Kill a Mockingbird", "Harper Lee", 281)
book3 = Book("The Great Gatsby", "F. Scott Fitzgerald", 180)

print("Book 2 info:", book2.get_info())
print("Book 3 info:", book3.get_info())
```

---

### Section 3: List of Objects

#### 3.1 Creating a List of Objects
You can store objects in a list and use a loop to access their methods.

```python
# Storing Book objects in a list
library = [book1, book2, book3]

# Iterating over the list of books and printing their information
print("Books in the library:")
for book in library:
    print(book.get_info())
```

---

### Section 4: List Comprehensions

#### 4.1 Simple List Comprehension
List comprehensions allow you to create lists in a concise way.

```python
# Creating a list of squared numbers using list comprehension
numbers = [1, 2, 3, 4, 5]
squared_numbers = [x**2 for x in numbers]
print("Squared numbers:", squared_numbers)
```

#### 4.2 Filtering with List Comprehension
You can also add conditions to a list comprehension.

```python
# Creating a list of even numbers using list comprehension
even_numbers = [x for x in numbers if x % 2 == 0]
print("Even numbers:", even_numbers)
```

---

### Section 5: Lab Exercises

#### Exercise 1: List Operations
1. Create a list of integers from 1 to 10.
2. Print the square of each number.
3. Remove all odd numbers from the list.
4. Add 11 to the list.

```python
# Solution to Exercise 1
integers = list(range(1, 11))
print("List of integers:", integers)

# Squaring each integer
squares = [x**2 for x in integers]
print("Squares of integers:", squares)

# Removing odd numbers
integers = [x for x in integers if x % 2 == 0]
print("Even integers:", integers)

# Adding 11 to the list
integers.append(11)
print("List after adding 11:", integers)
```

#### Exercise 2: Creating and Using a Class
1. Create a `Car` class with attributes `brand`, `model`, and `year`.
2. Add a method `car_info()` to return the car's details.
3. Create three instances of the class, store them in a list, and print each car's details.

```python
# Solution to Exercise 2
class Car:
    def __init__(self, brand, model, year):
        self.brand = brand
        self.model = model
        self.year = year

    def car_info(self):
        return f"{self.brand} {self.model}, {self.year}"

# Creating instances of the Car class
car1 = Car("Toyota", "Camry", 2020)
car2 = Car("Honda", "Accord", 2018)
car3 = Car("Tesla", "Model 3", 2021)

# Storing cars in a list
garage = [car1, car2, car3]

# Printing car details
print("Cars in the garage:")
for car in garage:
    print(car.car_info())
```