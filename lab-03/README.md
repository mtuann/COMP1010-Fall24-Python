### Lab 3: Functions & Modules

#### Objectives:
- Understand the functions and make function calls. Use built-in functions.
- Understand and use modules. Use module functions and variables. Understand and use the most important Python modules. Create Python modules. 


---

### Section 1. Python Functions

Python Functions is a block of statements that return the specific task. The idea is to put some commonly or repeatedly done tasks together and make a function so that instead of writing the same code again and again for different inputs, we can do the function calls to reuse code contained in it over and over again.

Some **Benefits of Using Functions**

- Increase Code Readability 
- Increase Code Reusability

#### 1.1. Creating a Function in Python

We can define a function in Python, using the def keyword. We can add any type of functionalities and properties to it as we require. By the following example, we can understand how to write a function in Python. In this way we can create Python function definition by using def keyword.

```python
# A simple Python function
def welcome():
    print("Welcome to COMP1010")
```

#### 1.2. Calling a Function in Python

After creating a function in Python we can call it by using the name of the functions Python followed by parenthesis containing parameters of that particular function. Below is the example for calling def function Python.

```python
# A simple Python function
def welcome():
    print("Welcome to COMP1010")

# Driver code to call a function
welcome()
```

---

#### 1.3. Python Function with Parameters

You must be thinking about the **return type** of the function and **data type** of arguments. That is possible in Python as well (specifically for Python 3.5 and above).

**Python Function Syntax with Parameters**

```python
def function_name(parameter: data_type) -> return_type:
    """Docstring"""
    # body of the function
    return expression
```

**Example**

```python
def add(num1: int, num2: int) -> int:
    """Add two numbers"""
    num3 = num1 + num2

    return num3

# Driver code
num1, num2 = 5, 15
ans = add(num1, num2)
print(f"The addition of {num1} and {num2} results {ans}.")
```

```python
# some more functions
def is_prime(n):
    if n in [2, 3]:
        return True
    if (n == 1) or (n % 2 == 0):
        return False
    r = 3
    while r * r <= n:
        if n % r == 0:
            return False
        r += 2
    return True
print(is_prime(78), is_prime(79))
```

#### 1.4. Python Function Arguments

Arguments are the values passed inside the parenthesis of the function. A function can have any number of arguments separated by a comma.

In this example, we will create a simple function in Python to check whether the number passed as an argument to the function is even or odd.

```python
# A simple Python function to check
# whether x is even or odd
def evenOdd(x):
    if (x % 2 == 0):
        print("even")
    else:
        print("odd")


# Driver code to call the function
evenOdd(2)
evenOdd(3)
```

#### 1.5. Types of Python Function Arguments

Python supports various types of arguments that can be passed at the time of the function call. In Python, we have the following function argument types in Python:

- Default argument
- Keyword arguments (named arguments)
- Arbitrary arguments (variable-length arguments *args and **kwargs)

**Default argument**

A default argument is a parameter that assumes a default value if a value is not provided in the function call for that argument. The following example illustrates Default arguments to write functions in Python.

```python
# Python program to demonstrate
# default arguments
def print_default(x, y=50):
    print("x: ", x)
    print("y: ", y)


# Driver code (We call print_default() with only
# argument)
print_default(10)
```

**Keyword Arguments**
The idea is to allow the caller to specify the argument name with values so that the caller does not need to remember the order of parameters.

```python
# Python program to demonstrate Keyword Arguments
def student(firstname, lastname):
    print(firstname, lastname)


# Keyword arguments
student(firstname='Lucaz', lastname='Nguyen')
student(lastname='Tuan', firstname='Nguyen')
student(lastname='Anh', firstname='Vu')
```

**Arbitrary Keyword  Arguments**
In Python Arbitrary Keyword Arguments, **\*args**, and **\*\*kwargs** can pass a variable number of arguments to a function using special symbols. There are two special symbols:

- *args in Python (Non-Keyword Arguments)
- **kwargs in Python (Keyword Arguments)

```python
# Python program to illustrate
# *args for variable number of arguments
def print_all(*argv):
    for arg in argv:
        print(arg)

print_all('Hello', 'Welcome', 'to', 'VinUniversity')
```

```python
# Python program to illustrate
# *kwargs for variable number of keyword arguments

def myFun(**kwargs):
    for key, value in kwargs.items():
        print("%s == %s" % (key, value))

# Driver code
myFun(first='Geeks', mid='for', last='Geeks')
```
#### 1.6. Docstring

The first string after the function is called the Document string or Docstring in short. This is used to describe the functionality of the function. The use of docstring in functions is optional but it is considered a good practice.

The below syntax can be used to print out the docstring of a function.

```
Syntax: print(function_name.__doc__)
```

**Example:** Adding Docstring to the function

```python
# A simple Python function to check
# whether x is even or odd

def evenOdd(x):
    """Function to check if the number is even or odd"""
    
    if (x % 2 == 0):
        print("even")
    else:
        print("odd")

# Driver code to call the function
print(evenOdd.__doc__)
```

#### 1.7. Python Function within Functions
A function that is defined inside another function is known as the **inner function** or **nested function**. Nested functions can access variables of the enclosing scope. Inner functions are used so that they can be protected from everything happening outside the function.

```python
# Python program to
# demonstrate accessing of
# variables of nested functions

def f1():
    s = 'I love professor Kok-Seng'
    
    def f2():
        print(s)
        
    f2()

# Driver's code
f1()
```

#### 1.8. Return Statement in Python Function
The function return statement is used to exit from a function and go back to the function caller and return the specified value or data item to the caller. The syntax for the return statement is:
```
return [expression_list]
```

The return statement can consist of a variable, an expression, or a constant which is returned at the end of the function execution. If none of the above is present with the return statement a None object is returned.

**Example:** Python Function Return Statement

```python
def square_value(num):
    """This function returns the square
    value of the entered number"""
    return num**2

print(square_value(2))
print(square_value(-4))
```

---

### Section 2. Python Modules

Consider a module to be the same as a code library. A file containing a set of functions you want to include in your application.

#### 2.1. Create a Module

To create a module just save the code you want in a file with the file extension ```.py```.

**Example:** Save this code in a file named ```mymodule.py```

```python
def greeting(name):
    print("Hello, " + name)
```

#### 2.2. Use a module

Now we can use the module we just created, by using the ```import``` statement.

**Example:** Import the module named mymodule, and call the greeting function:

```python
import mymodule
mymodule.greeting("Vu Duc Anh")
```

#### 2.3. Variables in Module

The module can contain functions, as already described, but also variables of all types (arrays, dictionaries, objects, etc):

**Example:** Save this code in the file ```mymodule.py```

```python
person = {
  "name": "Lucaz",
  "age": 25,
  "country": "Vietnam"
}
```

Import the module named mymodule, and access the ```person``` dictionary:

```python
import mymodule

a = mymodule.person["age"]
print(a)
```

#### 2.4. Naming a Module

You can name the module file whatever you like, but it must have the file extension ```.py```.

You can create an alias when you import a module, by using the as keyword:

**Example:** Create an alias for ```mymodule``` called ```md```:

```python
import mymodule as md

a = md.person["age"]
print(a)
```

#### 2.5. Import From Module

You can choose to import only parts from a module, by using the ```from``` keyword.

**Example:** The module named ```mymodule``` has one function and one dictionary:

```python
def greeting(name):
  print("Hello, " + name)

person = {
  "name": "Lucaz",
  "age": 25,
  "country": "Vietnam"
}
```

Import only the ```person``` dictionary from the module:

```python
from mymodule import person

print(person["age"])
```
