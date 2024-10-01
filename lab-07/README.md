### Lab 07: Lists, Iteration, and Loops

#### Objectives:
- Understand how to use loops (for and while) to iterate through lists.
- Practice different ways of iterating over lists in Python.
- Learn how to apply loops for various operations on lists, such as searching, counting, and modifying list elements.

---

### Section 1: Lists and `for` Loops

#### 1.1 Introduction to `for` Loops with Lists
A `for` loop in Python allows you to iterate over all elements of a list easily.

```python
# A simple for loop that prints each element in a list
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    print(num)
```

Here, the `for` loop goes through each element of the `numbers` list and prints it.

#### 1.2 Using `range()` with `for` Loops
You can also use the `range()` function to loop through a sequence of numbers, which can be useful when you want to use the index of a list.

```python
# Using range() to loop through indices of the list
for i in range(len(numbers)):
    print(f"Index {i}: {numbers[i]}")
```

The `range(len(numbers))` gives us a sequence of indices, and we can use it to access list elements.

#### 1.3 Modifying a List with `for` Loops
We can use a `for` loop to modify elements in a list.

```python
# Doubling each number in the list
for i in range(len(numbers)):
    numbers[i] = numbers[i] * 2
print("List after doubling:", numbers)
```

Note: Be cautious when modifying a list while iterating through it.

---

### Section 2: Lists and `while` Loops

#### 2.1 Introduction to `while` Loops with Lists
A `while` loop continues until a condition becomes false. You can use it to iterate over a list based on a condition.

```python
# Using a while loop to print all elements in the list
index = 0
while index < len(numbers):
    print(numbers[index])
    index += 1  # Move to the next element
```

Here, the `while` loop goes through each element of the list based on the `index`.

#### 2.2 `while` Loop for Searching in a List
A common use of a `while` loop is to search for a specific element in a list.

```python
# Searching for a number in the list using a while loop
target = 8
index = 0
found = False

while index < len(numbers) and not found:
    if numbers[index] == target:
        found = True
        print(f"Found {target} at index {index}")
    index += 1

if not found:
    print(f"{target} not found in the list")
```

---

### Section 3: Nested Loops with Lists

#### 3.1 Nested `for` Loops
A **nested loop** is when a loop runs inside another loop. You can use this to work with 2D lists or perform operations involving multiple lists.

```python
# Example of a nested loop: Multiplication table
for i in range(1, 4):  # Outer loop
    for j in range(1, 4):  # Inner loop
        print(f"{i} x {j} = {i * j}")
    print()  # Blank line after each row
```

Nested loops allow you to combine elements or perform operations like matrix multiplication.

---

### Section 4: Practical Examples of List Operations with Loops

#### 4.1 Counting Elements in a List
You can use a `for` loop to count how many times a certain element appears in a list.

```python
# Counting the occurrences of the number 8 in the list
numbers = [2, 4, 8, 8, 10, 12, 8]
count = 0

for num in numbers:
    if num == 8:
        count += 1

print(f"Number 8 appears {count} times in the list")
```

#### 4.2 Finding the Maximum Value in a List
Use a `for` loop to find the maximum value in a list.

```python
# Finding the maximum value in a list
numbers = [2, 4, 8, 10, 12, 3]
max_num = numbers[0]

for num in numbers:
    if num > max_num:
        max_num = num

print(f"The maximum value in the list is: {max_num}")
```

#### 4.3 Summing the Elements of a List
You can sum all the numbers in a list using a `for` loop.

```python
# Summing all numbers in the list
total = 0

for num in numbers:
    total += num

print(f"The sum of the numbers in the list is: {total}")
```

#### 4.4 Using List Comprehensions
List comprehensions offer a concise way to create lists. You can also use them to apply transformations to list elements.

```python
# Doubling all numbers in a list using list comprehension
doubled_numbers = [num * 2 for num in numbers]
print("Doubled numbers:", doubled_numbers)
```

---

### Section 5: Lab Exercises

#### Exercise 1: Sum and Average of List Elements
1. Create a list of integers from 1 to 20.
2. Write a loop to calculate the sum of all elements in the list.
3. Calculate and print the average of the list.

```python
# Solution to Exercise 1
numbers = list(range(1, 21))
total = 0

# Calculating the sum
for num in numbers:
    total += num

average = total / len(numbers)
print(f"Sum: {total}, Average: {average}")
```

#### Exercise 2: Find the Minimum Value in a List
1. Create a list of random integers.
2. Write a loop to find the minimum value in the list.

```python
# Solution to Exercise 2
numbers = [15, 22, 3, 45, 67, 12, 4]
min_num = numbers[0]

# Finding the minimum value
for num in numbers:
    if num < min_num:
        min_num = num

print(f"The minimum value in the list is: {min_num}")
```

#### Exercise 3: Filter Even Numbers Using a Loop
1. Create a list of numbers from 1 to 30.
2. Write a loop that adds only the even numbers to a new list.
3. Print the new list of even numbers.

```python
# Solution to Exercise 3
numbers = list(range(1, 31))
even_numbers = []

# Filtering even numbers
for num in numbers:
    if num % 2 == 0:
        even_numbers.append(num)

print("Even numbers:", even_numbers)
```

#### Exercise 4: Multiplication Table Using Nested Loops
1. Create a multiplication table (from 1 to 10) using nested loops.
2. Print the table neatly in rows and columns.

```python
# Solution to Exercise 4: Multiplication table
for i in range(1, 11):  # Outer loop
    for j in range(1, 11):  # Inner loop
        print(f"{i * j:3}", end=" ")  # Formatting with spaces for alignment
    print()  # New line after each row
```
