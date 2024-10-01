### Lab 10: Sequential and Recursive Algorithms

#### Objectives:
- Understand the difference between **sequential** (iterative) and **recursive** algorithms.
- Learn how to implement both types of algorithms in Python.
- Practice solving common problems using both iterative and recursive approaches.
- Explore the concept of recursion, including base cases and recursive cases.

---

### Section 1: Sequential (Iterative) Algorithms

#### 1.1 What is a Sequential Algorithm?
A **sequential algorithm** uses a series of steps that execute in a loop or sequence to solve a problem. These are often referred to as iterative approaches.

#### 1.2 Example: Factorial (Iterative)
The factorial of a number `n` (denoted as `n!`) is the product of all positive integers from 1 to `n`.

**Iterative Approach:**

```python
# Factorial using iteration
def factorial_iterative(n):
    result = 1
    for i in range(1, n+1):
        result *= i
    return result

n = 5
print(f"Factorial of {n} (iterative):", factorial_iterative(n))
```

---

### Section 2: Recursive Algorithms

#### 2.1 What is Recursion?
**Recursion** occurs when a function calls itself to solve smaller instances of the same problem. A recursive algorithm typically has two main parts:
1. **Base case**: The condition that stops the recursion.
2. **Recursive case**: The part of the function that reduces the problem towards the base case.

#### 2.2 Example: Factorial (Recursive)
The same factorial problem can be solved using recursion.

**Recursive Approach:**

```python
# Factorial using recursion
def factorial_recursive(n):
    if n == 0 or n == 1:  # Base case
        return 1
    else:  # Recursive case
        return n * factorial_recursive(n-1)

n = 5
print(f"Factorial of {n} (recursive):", factorial_recursive(n))
```

#### 2.3 Key Points about Recursion:
- **Base case**: It is essential to define a base case to avoid infinite recursion.
- **Recursive calls**: Each recursive call reduces the size of the problem.

---

### Section 3: Comparison of Iterative and Recursive Solutions

#### 3.1 Fibonacci Series (Iterative vs Recursive)
The **Fibonacci series** is a sequence of numbers where each number is the sum of the two preceding ones. The series starts with 0 and 1.

**Iterative Approach:**

```python
# Fibonacci using iteration
def fibonacci_iterative(n):
    a, b = 0, 1
    for _ in range(n):
        a, b = b, a + b
    return a

n = 6
print(f"Fibonacci({n}) (iterative):", fibonacci_iterative(n))
```

**Recursive Approach:**

```python
# Fibonacci using recursion
def fibonacci_recursive(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)

n = 6
print(f"Fibonacci({n}) (recursive):", fibonacci_recursive(n))
```

#### 3.2 Pros and Cons
- **Iterative algorithms** are usually faster because they don’t involve repeated function calls, which can add overhead.
- **Recursive algorithms** can be more intuitive and easier to write for problems like the Fibonacci series, but they may be less efficient in terms of time and space (due to function call stack growth).

---

### Section 4: Common Recursive Algorithms

#### 4.1 Tower of Hanoi
The **Tower of Hanoi** is a classic problem in which you must move `n` disks from one peg to another, with the restriction that no disk may be placed on top of a smaller disk.

```python
# Tower of Hanoi
def hanoi(n, source, target, auxiliary):
    if n == 1:
        print(f"Move disk 1 from {source} to {target}")
    else:
        hanoi(n-1, source, auxiliary, target)
        print(f"Move disk {n} from {source} to {target}")
        hanoi(n-1, auxiliary, target, source)

n = 3
hanoi(n, 'A', 'C', 'B')
```

#### 4.2 Sum of Digits
A recursive function to calculate the sum of digits of a number.

```python
# Sum of digits using recursion
def sum_of_digits(n):
    if n == 0:
        return 0
    else:
        return n % 10 + sum_of_digits(n // 10)

n = 12345
print(f"Sum of digits of {n}:", sum_of_digits(n))
```

---

### Section 5: Lab Exercises

#### Exercise 1: Factorial Calculation
1. Write a function to calculate the factorial of a number using both an iterative and a recursive approach.
2. Compare the two solutions for the factorial of `10`.

```python
# Solution to Exercise 1
def factorial_iterative(n):
    result = 1
    for i in range(1, n+1):
        result *= i
    return result

def factorial_recursive(n):
    if n == 0 or n == 1:
        return 1
    else:
        return n * factorial_recursive(n-1)

n = 10
print("Factorial (iterative):", factorial_iterative(n))
print("Factorial (recursive):", factorial_recursive(n))
```

#### Exercise 2: Fibonacci Series
1. Write a function to calculate the nth Fibonacci number using both an iterative and a recursive approach.
2. Compare the two solutions for the Fibonacci number at position `10`.

```python
# Solution to Exercise 2
def fibonacci_iterative(n):
    a, b = 0, 1
    for _ in range(n):
        a, b = b, a + b
    return a

def fibonacci_recursive(n):
    if n == 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)

n = 10
print("Fibonacci (iterative):", fibonacci_iterative(n))
print("Fibonacci (recursive):", fibonacci_recursive(n))
```

#### Exercise 3: Sum of Digits
1. Write a recursive function to find the sum of the digits of a given number.
2. Test the function with the number `54321`.

```python
# Solution to Exercise 3
def sum_of_digits(n):
    if n == 0:
        return 0
    else:
        return n % 10 + sum_of_digits(n // 10)

n = 54321
print("Sum of digits:", sum_of_digits(n))
```

#### Exercise 4: Tower of Hanoi
1. Write a function to solve the Tower of Hanoi problem for `3` disks.
2. Print the steps required to solve the problem.

```python
# Solution to Exercise 4
def hanoi(n, source, target, auxiliary):
    if n == 1:
        print(f"Move disk 1 from {source} to {target}")
    else:
        hanoi(n-1, source, auxiliary, target)
        print(f"Move disk {n} from {source} to {target}")
        hanoi(n-1, auxiliary, target, source)

n = 3
hanoi(n, 'A', 'C', 'B')
```