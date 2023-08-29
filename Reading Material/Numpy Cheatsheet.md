
# Numpy Cheat Sheet 📚

Made with :heart: by **Fardeen Ahmad Khan**

Welcome to the Numpy Cheat Sheet! 🌟 Numpy is a fundamental package for numerical computations in Python. This cheat sheet provides a quick reference for some commonly used functions and concepts in Numpy.

## Importing Numpy
```python
import numpy as np
```

## Creating Arrays 📊
Create arrays using various methods.

- 📝 **1D Array**:
```python
arr = np.array([1, 2, 3])
```

- 📝 **2D Array (Matrix)**:
```python
matrix = np.array([[1, 2, 3], [4, 5, 6]])
```

- 📝 **Zeros Array**:
```python
zeros = np.zeros((2, 3))
```

- 📝 **Ones Array**:
```python
ones = np.ones((3, 2))
```

- 📝 **Random Array**:
```python
random = np.random.rand(2, 2)
```

## Basic Operations ✨
Perform basic arithmetic operations on arrays.

- 🧮 **Addition**:
```python
result = arr1 + arr2
```

- 🧮 **Subtraction**:
```python
result = arr1 - arr2
```

- 🧮 **Multiplication**:
```python
result = arr1 * arr2
```

- 🧮 **Division**:
```python
result = arr1 / arr2
```

## Indexing and Slicing 🪒
Access and manipulate array elements.

- 🔍 **Indexing**:
```python
element = arr[2]
```

- 🔍 **Slicing**:
```python
sub_array = arr[1:4]
```

## Array Manipulation 🔄
Manipulate the shape and contents of arrays.

- 🔄 **Reshape Array**:
```python
reshaped = arr.reshape((2, 2))
```

- 🔄 **Transposed Array**:
```python
transposed = arr.T
```

- 🔄 **Flatten Array**:
```python
flattened = matrix.flatten()
```

## Broadcasting 📡
Perform element-wise operations on arrays of different shapes.

- 📡 **Broadcasting Example**:
```python
result = arr + 5
```

## Aggregation Functions 📊
Compute statistics and aggregates on arrays.

- 📊 **Mean**:
```python
mean_value = np.mean(arr)
```

- 📊 **Median**:
```python
median_value = np.median(arr)
```

- 📊 **Sum**:
```python
sum_value = np.sum(arr)
```

## Linear Algebra 🔗
Perform linear algebra operations with arrays.

- 🔗 **Matrix Multiplication**:
```python
result = np.dot(matrix1, matrix2)
```

- 🔗 **Determinant**:
```python
determinant = np.linalg.det(matrix)
```

- 🔗 **Inverse**:
```python
inverse = np.linalg.inv(matrix)
```

Remember to install Numpy using `pip install numpy` if you haven't already. Feel free to refer to this cheat sheet whenever you're working with Numpy arrays. Happy coding! 🚀

Made with :heart: by **Fardeen Ahmad Khan**
