### Lab 12: Object-Oriented Programming (Subclasses and Inheritance)

#### Objectives:
- Understand the concept of inheritance in object-oriented programming.
- Learn how to create subclasses that inherit properties and methods from a parent class.
- Understand method overriding in subclasses.
- Explore the `super()` function to access methods from the parent class.
- Practice creating hierarchies of classes and objects.

---

### Section 1: Introduction to Inheritance

#### 1.1 What is Inheritance?
Inheritance is a mechanism in object-oriented programming where a **new class** (subclass/child class) can inherit properties and methods from an **existing class** (parent class/base class). This allows for code reuse and establishes a relationship between classes.

- **Parent class**: The class being inherited from (also called a base class or superclass).
- **Child class**: The class that inherits from the parent class (also called a subclass).

#### 1.2 Example: Inheriting from a Parent Class
Let's define a simple `Animal` class as a parent class, and create a `Dog` subclass that inherits from `Animal`.

```python
# Parent class
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print(f"{self.name} makes a sound.")

# Child class inheriting from Animal
class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)  # Calling the parent class's constructor
        self.breed = breed

    def speak(self):
        print(f"{self.name} says Woof!")

# Creating an object of the Dog class
my_dog = Dog("Buddy", "Golden Retriever")
my_dog.speak()
```

---

### Section 2: Overriding Methods

#### 2.1 What is Method Overriding?
Method overriding occurs when a subclass provides a specific implementation of a method that is already defined in its parent class. This allows a subclass to alter or extend the functionality of the method.

```python
# Overriding the speak() method
class Cat(Animal):
    def speak(self):
        print(f"{self.name} says Meow!")

# Creating an object of the Cat class
my_cat = Cat("Whiskers")
my_cat.speak()  # This will call the overridden method in the Cat class
```

---

### Section 3: Using `super()` to Access Parent Methods

#### 3.1 Why Use `super()`?
The `super()` function allows you to call methods of the parent class from within a subclass. It is especially useful when the subclass needs to extend or modify the functionality of a parent method.

```python
# Using super() to extend the speak method
class Dog(Animal):
    def __init__(self, name, breed):
        super().__init__(name)  # Call the parent constructor
        self.breed = breed

    def speak(self):
        super().speak()  # Call the parent speak method
        print(f"{self.name}, a {self.breed}, says Woof!")

# Creating an object and calling the method
my_dog = Dog("Buddy", "Golden Retriever")
my_dog.speak()
```

---

### Section 4: Inheritance and Multiple Levels

#### 4.1 Multi-level Inheritance
A class can inherit from another class, and then another class can inherit from it. This creates a hierarchy.

```python
# Multi-level inheritance example
class Mammal(Animal):
    def feed_baby(self):
        print(f"{self.name} feeds its baby.")

class Dog(Mammal):
    def speak(self):
        print(f"{self.name} says Woof!")

# Creating an object of the Dog class
my_dog = Dog("Buddy")
my_dog.feed_baby()
my_dog.speak()
```

---

### Section 5: Lab Exercises

#### Exercise 1: Define a `Vehicle` Class and a `Car` Subclass
1. Create a `Vehicle` class with attributes `make`, `model`, and `year`.
2. Define a method `display_info()` that prints out the vehicle information.
3. Create a `Car` subclass that adds an attribute `fuel_type` (e.g., gasoline, electric) and overrides the `display_info()` method to include fuel type.

```python
# Solution to Exercise 1
class Vehicle:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def display_info(self):
        print(f"Vehicle Info: {self.year} {self.make} {self.model}")

class Car(Vehicle):
    def __init__(self, make, model, year, fuel_type):
        super().__init__(make, model, year)
        self.fuel_type = fuel_type

    def display_info(self):
        super().display_info()  # Call parent method
        print(f"Fuel Type: {self.fuel_type}")

# Test the class
my_car = Car("Toyota", "Corolla", 2020, "Gasoline")
my_car.display_info()
```

#### Exercise 2: Create an `Employee` Class and a `Manager` Subclass
1. Define an `Employee` class with attributes `name` and `salary`.
2. Add a method `work()` that prints a message indicating the employee is working.
3. Create a `Manager` subclass that adds an attribute `department` and overrides the `work()` method to print the department.

```python
# Solution to Exercise 2
class Employee:
    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    def work(self):
        print(f"{self.name} is working.")

class Manager(Employee):
    def __init__(self, name, salary, department):
        super().__init__(name, salary)
        self.department = department

    def work(self):
        print(f"{self.name} is managing the {self.department} department.")

# Creating an object and testing
manager = Manager("Alice", 75000, "HR")
manager.work()
```

#### Exercise 3: Implement a `Shape` Class and `Rectangle` and `Circle` Subclasses
1. Create a `Shape` class with a method `area()` that returns `0`.
2. Create a `Rectangle` subclass with attributes `length` and `width`, and override `area()` to calculate the rectangle's area.
3. Create a `Circle` subclass with an attribute `radius`, and override `area()` to calculate the circle’s area.

```python
# Solution to Exercise 3
import math

class Shape:
    def area(self):
        return 0

class Rectangle(Shape):
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        return self.length * self.width

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius

    def area(self):
        return math.pi * self.radius ** 2

# Creating objects and testing
rect = Rectangle(4, 5)
circle = Circle(3)

print("Rectangle Area:", rect.area())
print("Circle Area:", circle.area())
```

#### Exercise 4: Create a `Person` Class and a `Student` Subclass
1. Define a `Person` class with attributes `name` and `age`, and a method `greet()`.
2. Create a `Student` subclass that adds an attribute `student_id` and overrides the `greet()` method to include the student ID.

```python
# Solution to Exercise 4
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def greet(self):
        print(f"Hello! My name is {self.name} and I am {self.age} years old.")

class Student(Person):
    def __init__(self, name, age, student_id):
        super().__init__(name, age)
        self.student_id = student_id

    def greet(self):
        print(f"Hello! My name is {self.name}, I am {self.age} years old, and my student ID is {self.student_id}.")

# Creating an object and testing
student = Student("John", 21, "S12345")
student.greet()
```