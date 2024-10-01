### Lab 09: Sorting

#### Objectives:
- Understand the concept of sorting and why it is useful in programming.
- Learn how to use Python’s built-in sorting methods: `sorted()` and `.sort()`.
- Explore different ways to customize sorting using key functions and lambda expressions.
- Practice implementing simple sorting algorithms (e.g., selection sort, bubble sort).

---

### Section 1: Introduction to Sorting

#### 1.1 What is Sorting?
Sorting is the process of arranging data in a particular order. This is commonly ascending or descending order. Sorting is useful in searching, organizing data, and optimizing certain algorithms.

---

### Section 2: Built-in Sorting Functions

#### 2.1 Using `sorted()`
The `sorted()` function returns a new sorted list from any iterable (e.g., list, tuple).

```python
# Using sorted() to sort a list of numbers
numbers = [5, 3, 8, 6, 2, 7]
sorted_numbers = sorted(numbers)
print("Original list:", numbers)
print("Sorted list:", sorted_numbers)
```

- **Note:** The `sorted()` function does not modify the original list. It returns a new list.

#### 2.2 Using `.sort()`
The `.sort()` method sorts a list in place, meaning it modifies the original list.

```python
# Using sort() to sort the original list
numbers.sort()
print("List after sort():", numbers)
```

#### 2.3 Sorting in Descending Order
You can sort in descending order by passing the `reverse=True` argument.

```python
# Sorting in descending order
sorted_numbers_desc = sorted(numbers, reverse=True)
print("Sorted in descending order:", sorted_numbers_desc)
```

---

### Section 3: Custom Sorting with `key`

#### 3.1 Sorting by String Length
You can customize the sorting behavior by using the `key` parameter. The `key` parameter expects a function that will be applied to each element before sorting.

```python
# Sorting strings by their length
words = ["apple", "banana", "cherry", "date"]
sorted_by_length = sorted(words, key=len)
print("Sorted by length:", sorted_by_length)
```

#### 3.2 Sorting with `lambda` Functions
You can pass a custom function or use a **lambda function** to sort based on more complex criteria.

```python
# Sorting tuples by the second element
tuples = [(1, 3), (2, 2), (4, 1)]
sorted_tuples = sorted(tuples, key=lambda x: x[1])
print("Sorted by second element:", sorted_tuples)
```

---

### Section 4: Implementing Sorting Algorithms

#### 4.1 Selection Sort
In **selection sort**, the algorithm repeatedly selects the smallest element from the unsorted portion of the list and swaps it with the first unsorted element.

```python
# Selection Sort implementation
def selection_sort(arr):
    for i in range(len(arr)):
        min_idx = i
        for j in range(i+1, len(arr)):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]

numbers = [64, 25, 12, 22, 11]
selection_sort(numbers)
print("Selection sorted list:", numbers)
```

#### 4.2 Bubble Sort
In **bubble sort**, adjacent elements are repeatedly swapped if they are in the wrong order. This process continues until the list is sorted.

```python
# Bubble Sort implementation
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

numbers = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(numbers)
print("Bubble sorted list:", numbers)
```

#### 4.3 Efficiency of Sorting Algorithms
Both selection sort and bubble sort have time complexity of O(n²), which makes them inefficient for large datasets. However, Python's built-in sorting functions use **Timsort**, which is much more efficient (O(n log n)).

---

### Section 5: Lab Exercises

#### Exercise 1: Sorting Numbers
1. Create a list of random integers.
2. Use `sorted()` to sort the list in both ascending and descending order.
3. Print the original and sorted lists.

```python
# Solution to Exercise 1
import random

numbers = random.sample(range(1, 100), 10)
print("Original list:", numbers)

sorted_numbers = sorted(numbers)
print("Sorted list (ascending):", sorted_numbers)

sorted_numbers_desc = sorted(numbers, reverse=True)
print("Sorted list (descending):", sorted_numbers_desc)
```

#### Exercise 2: Sorting by Custom Key
1. Create a list of tuples where each tuple contains a student’s name and grade.
2. Sort the list by grade using `sorted()` and a `lambda` function.

```python
# Solution to Exercise 2
students = [("Alice", 85), ("Bob", 90), ("Charlie", 82), ("David", 88)]
sorted_by_grade = sorted(students, key=lambda x: x[1])
print("Sorted by grade:", sorted_by_grade)
```

#### Exercise 3: Implement Selection Sort
1. Write a function to implement the selection sort algorithm.
2. Test it on a list of integers.

```python
# Solution to Exercise 3
def selection_sort(arr):
    for i in range(len(arr)):
        min_idx = i
        for j in range(i+1, len(arr)):
            if arr[j] < arr[min_idx]:
                min_idx = j
        arr[i], arr[min_idx] = arr[min_idx], arr[i]

numbers = [29, 10, 14, 37, 14]
selection_sort(numbers)
print("Selection sorted list:", numbers)
```

#### Exercise 4: Implement Bubble Sort
1. Write a function to implement the bubble sort algorithm.
2. Test it on a list of integers.

```python
# Solution to Exercise 4
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]

numbers = [64, 34, 25, 12, 22, 11, 90]
bubble_sort(numbers)
print("Bubble sorted list:", numbers)
```