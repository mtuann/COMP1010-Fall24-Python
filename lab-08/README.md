### Lab 08: Tuples and Dictionaries

#### Objectives:
- Understand the concept of **tuples** and how they differ from lists.
- Learn how to create and manipulate **dictionaries**.
- Practice accessing and modifying data in dictionaries.
- Explore use cases where tuples and dictionaries are useful in programming.

---

### Section 1: Tuples in Python

#### 1.1 Introduction to Tuples
A **tuple** is an immutable collection of ordered elements. Once a tuple is created, its elements cannot be changed, added, or removed.

```python
# Creating a tuple
coordinates = (10, 20, 30)
print("Tuple of coordinates:", coordinates)
```

Tuples are often used to represent fixed collections of items, such as coordinates, days of the week, or color codes.

#### 1.2 Accessing Elements in a Tuple
You can access elements in a tuple using indexing, similar to lists.

```python
# Accessing elements in a tuple
print("First coordinate:", coordinates[0])
print("Last coordinate:", coordinates[-1])
```

#### 1.3 Tuple Unpacking
You can **unpack** a tuple by assigning its elements to variables.

```python
# Unpacking the tuple into variables
x, y, z = coordinates
print(f"x: {x}, y: {y}, z: {z}")
```

#### 1.4 Immutability of Tuples
Tuples are **immutable**, meaning you cannot change their elements after creation. Any attempt to modify a tuple will result in an error.

```python
# Trying to change an element in a tuple (this will raise an error)
# coordinates[0] = 50  # Uncommenting this line will result in a TypeError
```

#### 1.5 Tuples vs Lists
The key difference between tuples and lists is that tuples are immutable, while lists are mutable. Use tuples when you want to ensure data cannot be modified.

---

### Section 2: Dictionaries in Python

#### 2.1 Introduction to Dictionaries
A **dictionary** is a collection of key-value pairs. Each key must be unique, and it is used to access its corresponding value.

```python
# Creating a dictionary
student = {
    "name": "Alice",
    "age": 20,
    "major": "Computer Science"
}
print("Student dictionary:", student)
```

In this example, `"name"`, `"age"`, and `"major"` are the keys, and `"Alice"`, `20`, and `"Computer Science"` are the corresponding values.

#### 2.2 Accessing Dictionary Values
You can access values in a dictionary using their keys.

```python
# Accessing values by their keys
print("Student name:", student["name"])
print("Student age:", student["age"])
```

#### 2.3 Modifying Dictionary Values
Dictionaries are mutable, so you can change the values associated with keys or add new key-value pairs.

```python
# Changing a value in the dictionary
student["age"] = 21
print("Updated age:", student["age"])

# Adding a new key-value pair
student["graduation_year"] = 2025
print("Updated student dictionary:", student)
```

#### 2.4 Dictionary Methods
Dictionaries come with various built-in methods, such as `keys()`, `values()`, `items()`, and `get()`.

```python
# Getting all keys in the dictionary
print("Keys:", student.keys())

# Getting all values in the dictionary
print("Values:", student.values())

# Using the get() method to safely access a key's value
print("Major:", student.get("major"))
print("Graduation year:", student.get("graduation_year", "N/A"))
```

---

### Section 3: Iterating Over Dictionaries

#### 3.1 Iterating Over Keys
You can use a `for` loop to iterate over the keys in a dictionary.

```python
# Iterating over keys in the dictionary
for key in student:
    print(f"{key}: {student[key]}")
```

#### 3.2 Iterating Over Key-Value Pairs
You can use the `items()` method to iterate over both keys and values.

```python
# Iterating over key-value pairs
for key, value in student.items():
    print(f"{key}: {value}")
```

---

### Section 4: Tuples as Dictionary Keys

Tuples can be used as keys in a dictionary because they are immutable. This is useful when you want to represent data that has multiple attributes as a single key.

```python
# Using a tuple as a dictionary key
location_dict = {
    (10.5, 25.3): "Point A",
    (40.7, 90.5): "Point B"
}

# Accessing a value using a tuple key
print("Location of (10.5, 25.3):", location_dict[(10.5, 25.3)])
```

---

### Section 5: Lab Exercises

#### Exercise 1: Tuple Operations
1. Create a tuple that contains the names of five cities.
2. Print the second and fourth cities in the tuple.
3. Use tuple unpacking to assign the cities to separate variables.

```python
# Solution to Exercise 1
cities = ("New York", "London", "Tokyo", "Sydney", "Paris")

# Printing second and fourth cities
print("Second city:", cities[1])
print("Fourth city:", cities[3])

# Unpacking the tuple
city1, city2, city3, city4, city5 = cities
print(f"Unpacked cities: {city1}, {city2}, {city3}, {city4}, {city5}")
```

#### Exercise 2: Dictionary Operations
1. Create a dictionary to store information about a book (title, author, year, pages).
2. Update the dictionary to include the price of the book.
3. Write a loop to print all key-value pairs in the dictionary.

```python
# Solution to Exercise 2
book = {
    "title": "1984",
    "author": "George Orwell",
    "year": 1949,
    "pages": 328
}

# Adding a new key-value pair for price
book["price"] = 19.99

# Printing all key-value pairs
for key, value in book.items():
    print(f"{key}: {value}")
```

#### Exercise 3: Dictionary Search
1. Create a dictionary where the keys are student names and the values are their grades.
2. Write a loop that checks if a given student (e.g., "Alice") exists in the dictionary and prints their grade if found.
3. If the student is not found, print "Student not found."

```python
# Solution to Exercise 3
grades = {
    "Alice": 90,
    "Bob": 85,
    "Charlie": 95
}

# Searching for a student's grade
student_name = "Alice"
if student_name in grades:
    print(f"{student_name}'s grade: {grades[student_name]}")
else:
    print("Student not found")
```

#### Exercise 4: Nested Dictionary
1. Create a dictionary where each key is a student's name and the value is another dictionary containing their age and major.
2. Write a loop to print each student's name along with their age and major.

```python
# Solution to Exercise 4
students = {
    "Alice": {"age": 20, "major": "Computer Science"},
    "Bob": {"age": 21, "major": "Mathematics"},
    "Charlie": {"age": 19, "major": "Physics"}
}

# Printing each student's details
for name, info in students.items():
    print(f"{name} - Age: {info['age']}, Major: {info['major']}")
```
