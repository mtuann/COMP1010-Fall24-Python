### Lab 13: Python Tools for Machine Learning

#### Objectives:
- Introduce Python libraries commonly used for machine learning.
- Explore basic functionality of tools such as NumPy, pandas, and Matplotlib.
- Implement a simple machine learning model using scikit-learn.

---

### Section 1: Introduction to Machine Learning in Python

Python provides several powerful libraries for data analysis and machine learning. In this lab, we'll focus on key tools:
- **NumPy**: For numerical computations.
- **pandas**: For data manipulation and analysis.
- **Matplotlib**: For data visualization.
- **scikit-learn**: For machine learning algorithms and models.

#### 1.1 What is Machine Learning?
Machine learning (ML) is the process of teaching computers to make decisions or predictions based on data. There are various types of ML tasks, such as classification, regression, and clustering.

---

### Section 2: Working with NumPy

#### 2.1 NumPy Basics
NumPy is the core library for numerical operations in Python. It provides support for arrays, matrices, and mathematical functions.

```python
import numpy as np

# Creating a NumPy array
arr = np.array([1, 2, 3, 4, 5])

# Performing basic operations
print("Array:", arr)
print("Sum:", np.sum(arr))
print("Mean:", np.mean(arr))
print("Square of each element:", np.square(arr))
```

#### 2.2 Multi-dimensional Arrays
NumPy supports multi-dimensional arrays, which are useful for handling matrices and large datasets.

```python
# Creating a 2D array
matrix = np.array([[1, 2, 3], [4, 5, 6], [7, 8, 9]])

# Accessing elements
print("Matrix:\n", matrix)
print("Element at position (0, 1):", matrix[0, 1])

# Transposing the matrix
print("Transposed Matrix:\n", np.transpose(matrix))
```

---

### Section 3: Data Manipulation with pandas

#### 3.1 pandas DataFrames
pandas is a library for data manipulation and analysis. It provides two main data structures: `Series` and `DataFrame`.

```python
import pandas as pd

# Creating a DataFrame
data = {'Name': ['Alice', 'Bob', 'Charlie', 'David'],
        'Age': [25, 30, 35, 40],
        'Salary': [50000, 60000, 70000, 80000]}
df = pd.DataFrame(data)

# Displaying the DataFrame
print("DataFrame:\n", df)

# Accessing columns
print("Names:", df['Name'])

# Filtering rows
print("Employees with Salary > 60000:\n", df[df['Salary'] > 60000])
```

#### 3.2 Loading Data from CSV Files
pandas can be used to load and manipulate data from CSV files.

```python
# Loading a CSV file
df = pd.read_csv('data.csv')

# Displaying the first few rows of the dataset
print(df.head())
```

---

### Section 4: Visualizing Data with Matplotlib

#### 4.1 Plotting Graphs
Matplotlib is a plotting library for creating visualizations in Python.

```python
import matplotlib.pyplot as plt

# Creating a simple plot
x = np.linspace(0, 10, 100)
y = np.sin(x)

plt.plot(x, y)
plt.title("Sine Wave")
plt.xlabel("X-axis")
plt.ylabel("Y-axis")
plt.show()
```

#### 4.2 Bar Charts and Histograms
Matplotlib also supports other types of plots like bar charts and histograms.

```python
# Bar chart
categories = ['A', 'B', 'C', 'D']
values = [3, 7, 5, 2]

plt.bar(categories, values)
plt.title("Bar Chart Example")
plt.show()

# Histogram
data = np.random.randn(1000)
plt.hist(data, bins=30)
plt.title("Histogram Example")
plt.show()
```

---

### Section 5: Building a Simple Machine Learning Model with scikit-learn

#### 5.1 scikit-learn Overview
scikit-learn is a powerful library for machine learning in Python. It supports tasks like classification, regression, and clustering.

#### 5.2 Example: Linear Regression
We will use scikit-learn to create a simple linear regression model.

```python
from sklearn.linear_model import LinearRegression
import numpy as np

# Sample data (Hours studied vs Scores obtained)
X = np.array([[1], [2], [3], [4], [5]])  # Hours studied
y = np.array([50, 55, 65, 70, 80])  # Scores obtained

# Creating a linear regression model
model = LinearRegression()

# Fitting the model
model.fit(X, y)

# Making a prediction (score for 6 hours of study)
predicted_score = model.predict([[6]])
print("Predicted score for 6 hours of study:", predicted_score)
```

#### 5.3 Evaluating the Model
We can evaluate the performance of the model using metrics like Mean Squared Error (MSE) and R-squared.

```python
from sklearn.metrics import mean_squared_error, r2_score

# Predicting for the input data
y_pred = model.predict(X)

# Calculating MSE and R-squared
mse = mean_squared_error(y, y_pred)
r2 = r2_score(y, y_pred)

print("Mean Squared Error:", mse)
print("R-squared:", r2)
```

---

### Section 6: Lab Exercises

#### Exercise 1: Linear Regression on Housing Data
1. Load a dataset containing information about house prices (e.g., square footage, number of bedrooms, and price).
2. Use scikit-learn to build a linear regression model that predicts the house price based on square footage.

```python
# Loading data and applying linear regression
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression

# Load dataset (assumed as a CSV file)
data = pd.read_csv('housing.csv')

# Select features and target
X = data[['SquareFootage']]  # Feature
y = data['Price']  # Target

# Split the data into training and testing sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create and train the model
model = LinearRegression()
model.fit(X_train, y_train)

# Test the model and evaluate its performance
y_pred = model.predict(X_test)
print("Predictions on test set:\n", y_pred)
```

#### Exercise 2: Classification with k-Nearest Neighbors (k-NN)
1. Use scikit-learn’s `KNeighborsClassifier` to classify a dataset (e.g., the Iris dataset).
2. Train the model and make predictions on the test set.

```python
from sklearn.datasets import load_iris
from sklearn.model_selection import train_test_split
from sklearn.neighbors import KNeighborsClassifier

# Load the Iris dataset
iris = load_iris()
X = iris.data
y = iris.target

# Split into training and test sets
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)

# Create and train the k-NN model
knn = KNeighborsClassifier(n_neighbors=3)
knn.fit(X_train, y_train)

# Predict on the test set
y_pred = knn.predict(X_test)
print("Predicted classes:", y_pred)
```