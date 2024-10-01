### Lab 11: Basic Object-Oriented Programming (OOP)

#### Objectives:
- Understand the basic principles of Object-Oriented Programming (OOP).
- Learn how to define classes and create objects in Python.
- Understand the concept of attributes (variables) and methods (functions) within a class.
- Practice using constructors and the `self` parameter.
- Learn about encapsulation and access control using public and private attributes.

---

### Section 1: Introduction to OOP

#### 1.1 What is Object-Oriented Programming?
Object-Oriented Programming (OOP) is a programming paradigm based on the concept of **objects**, which contain both **data** (attributes) and **behavior** (methods). OOP helps to structure programs by bundling related data and functionality together.

#### 1.2 Key Concepts of OOP
- **Class**: A blueprint for creating objects. It defines the attributes and methods that the objects of the class will have.
- **Object**: An instance of a class.
- **Attributes**: Variables that store data related to the object.
- **Methods**: Functions that operate on the object's data.

---

### Section 2: Defining a Class

#### 2.1 Creating a Simple Class
Let’s create a simple class called `Dog`. This class will have attributes like `name` and `age`, and a method to make the dog bark.

```python
# Defining the Dog class
class Dog:
    def __init__(self, name, age):  # Constructor
        self.name = name  # Attribute: name
        self.age = age  # Attribute: age

    def bark(self):  # Method
        print(f"{self.name} says Woof!")
```

#### 2.2 Creating Objects (Instances of a Class)
Once we have defined the class, we can create objects (instances of the class).

```python
# Creating an object of the Dog class
my_dog = Dog("Buddy", 3)
print(f"My dog's name is {my_dog.name} and he is {my_dog.age} years old.")
my_dog.bark()  # Calling the bark method
```

---

### Section 3: Methods and the `self` Parameter

#### 3.1 Understanding `self`
In Python, `self` is a reference to the current object (instance) of the class. It allows access to the attributes and methods of the class. All methods in a class need to have `self` as the first parameter.

#### 3.2 Adding More Methods
Let’s add a method to the `Dog` class that allows us to change the dog’s age.

```python
# Adding a method to update age
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def bark(self):
        print(f"{self.name} says Woof!")

    def update_age(self, new_age):
        self.age = new_age
        print(f"{self.name} is now {self.age} years old.")

# Using the new method
my_dog = Dog("Buddy", 3)
my_dog.update_age(4)
```

---

### Section 4: Encapsulation and Access Control

#### 4.1 Public and Private Attributes
In Python, attributes are **public** by default, which means they can be accessed and modified from outside the class. We can make attributes private by prefixing their name with two underscores (`__`).

```python
# Encapsulating the Dog class with private attributes
class Dog:
    def __init__(self, name, age):
        self.__name = name  # Private attribute
        self.__age = age  # Private attribute

    def bark(self):
        print(f"{self.__name} says Woof!")

    def get_name(self):
        return self.__name

    def set_name(self, new_name):
        self.__name = new_name

# Accessing private attributes through methods
my_dog = Dog("Buddy", 3)
print("Dog's name:", my_dog.get_name())
my_dog.set_name("Max")
print("Dog's new name:", my_dog.get_name())
```

---

### Section 5: Constructors (`__init__` method)

#### 5.1 Understanding the Constructor
The `__init__` method is the **constructor** in Python. It gets called automatically when an object is created and is used to initialize the object’s attributes.

#### 5.2 Example: Car Class with Constructor
Let’s create a `Car` class with a constructor to initialize attributes like `make`, `model`, and `year`.

```python
# Car class with constructor
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

    def car_info(self):
        print(f"Car Info: {self.year} {self.make} {self.model}")

# Creating objects
my_car = Car("Toyota", "Corolla", 2020)
my_car.car_info()
```

---

### Section 6: Lab Exercises

#### Exercise 1: Define a `Person` Class
1. Create a `Person` class with the following attributes: `name`, `age`, and `city`.
2. Add a method `greet()` that prints a greeting message.
3. Create an object of the `Person` class and call the `greet()` method.

```python
# Solution to Exercise 1
class Person:
    def __init__(self, name, age, city):
        self.name = name
        self.age = age
        self.city = city

    def greet(self):
        print(f"Hello! My name is {self.name}, I'm {self.age} years old, and I live in {self.city}.")

# Creating an object
person = Person("Alice", 30, "New York")
person.greet()
```

#### Exercise 2: Define a `BankAccount` Class
1. Create a `BankAccount` class with attributes `owner` and `balance`.
2. Add methods `deposit()` and `withdraw()` to modify the balance.
3. Create an object and test the deposit and withdraw methods.

```python
# Solution to Exercise 2
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner = owner
        self.balance = balance

    def deposit(self, amount):
        self.balance += amount
        print(f"{amount} deposited. New balance is {self.balance}.")

    def withdraw(self, amount):
        if amount > self.balance:
            print("Insufficient balance.")
        else:
            self.balance -= amount
            print(f"{amount} withdrawn. New balance is {self.balance}.")

# Creating an object and testing
account = BankAccount("John Doe", 500)
account.deposit(200)
account.withdraw(100)
```

#### Exercise 3: Create a `Rectangle` Class
1. Define a `Rectangle` class with attributes `length` and `width`.
2. Add methods to calculate the area and perimeter of the rectangle.
3. Create an object and test the methods.

```python
# Solution to Exercise 3
class Rectangle:
    def __init__(self, length, width):
        self.length = length
        self.width = width

    def area(self):
        return self.length * self.width

    def perimeter(self):
        return 2 * (self.length + self.width)

# Creating an object and testing
rect = Rectangle(5, 3)
print("Area:", rect.area())
print("Perimeter:", rect.perimeter())
```

#### Exercise 4: Create a `Book` Class with Encapsulation
1. Define a `Book` class with private attributes `title`, `author`, and `price`.
2. Add methods to get and set the values of these attributes.
3. Create an object and test the methods.

```python
# Solution to Exercise 4
class Book:
    def __init__(self, title, author, price):
        self.__title = title  # Private attribute
        self.__author = author  # Private attribute
        self.__price = price  # Private attribute

    def get_title(self):
        return self.__title

    def set_title(self, new_title):
        self.__title = new_title

    def get_author(self):
        return self.__author

    def set_author(self, new_author):
        self.__author = new_author

    def get_price(self):
        return self.__price

    def set_price(self, new_price):
        self.__price = new_price

# Creating an object and testing
my_book = Book("1984", "George Orwell", 15.99)
print("Title:", my_book.get_title())
my_book.set_price(12.99)
print("New price:", my_book.get_price())
```