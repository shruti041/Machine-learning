# NumPy
## What is NumPy?
- NumPy is a Python library used for working with arrays.
- It also has function for working in domain of linear algebra, fourier transform, and matrices.
- NumPy was created in **2005** by **<ins>Travis Oliphant</ins>**. It is an open source project and you can use it freely.
- NumPy stands for **Numerical Python**. \
![NumPy](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTXqI8dRgAbdkj7q3UkNJKi7iTNTbSNTIoz03J8UCfKO0123jddXVz9QgylEmXw4n2pMQ4&usqp=CAU)
> [Intro](https://www.w3schools.com/python/numpy/numpy_intro.asp)\
> import numpy as np
## DataTypes and Attributes
- NumPy's main DataType is **ndarray**.
> al = np.array([1,2,3])
- [NumPy Array Shape](https://www.w3schools.com/python/numpy/numpy_array_shape.asp)
> a1.shape
- [NumPy Array shape and size](https://numpy.org/doc/2.2/reference/generated/numpy.size.html)
- **ndarray.size** --> number of elements in array
> a1.size
## Creating arrays
- [NumPy Creating Arrays](https://www.w3schools.com/python/numpy/numpy_creating_arrays.asp)
- **np.ones()** --> This function is used to create a new NumPy array of a specified shape and data type, where all elements are initialized to the value 1.
> ones = np.ones((2,3))\
> [numpy.ones()](https://numpy.org/devdocs/reference/generated/numpy.ones.html)
- **np.zeros()** --> It is a function in Python's NumPy library which creates a new array of a given shape and data type, filled entirely with zeros.
> zeros = np.zeros((2,3))\
> [numpy.zeros()](https://numpy.org/devdocs/reference/generated/numpy.zeros.html)
- **np.arange()** --> It is a function in Python's NumPy library that creates arrays with evenly spaced values within a specified interval. It is analogous to Python's built-in **[range()](https://www.w3schools.com/python/ref_func_range.asp)** function but returns a NumPy array instead of a list.
> range_array = np.arange(0,10,2)\
> [numpy.arange()](https://numpy.org/devdocs/reference/generated/numpy.arange.html)
- **np.random.randint()** --> It is a function in Python's NumPy library which is used to generate random integers within a specified range.
> random_array = np.random.randint(0, 10, size = (3,5))\
> [numpy.random.randint()](https://numpy.org/devdocs/reference/random/generated/numpy.random.randint.html)
- **np.random.random()** --> It is a function within the NumPy library in Python used to generate pseudo-random floating-point numbers. It produces samples from a uniform distribution over the half-open interval [0.0, 1.0), meaning the generated numbers are greater than or equal to 0 and strictly less than 1.
> random_array2 = np.random.random((5,3))\
> [numpy.random.random()](https://numpy.org/doc/2.2/reference/random/generated/numpy.random.random.html)
- **np.random.rand()** --> It is a function within the NumPy library in Python used to generate arrays of random floating-point numbers. These numbers are drawn from a uniform distribution over the interval [0,1), meaning every value between 0 (inclusive) and 1 (exclusive) has an equal probability of being selected.
> random_array3 = np.random.rand(5,3)\
> [numpy.random.rand()](https://numpy.org/doc/2.2/reference/random/generated/numpy.random.rand.html)
- **np.random.seed()** --> It is a function in NumPy which is used to initialize the pseudo-random number generator. This function takes an integer as an argument, which serves as the "seed" for the generator.
  - The primary purpose of using np.random.seed() is to ensure that random number generation is reproducible. When you set a specific seed, the sequence of "random" numbers generated subsequent to that seed will always be the same, regardless of how many times you run the code. This is crucial for **debugging**, **testing**, and **sharing research**, as it allows others to replicate your results exactly.
> np.random.seed(seed = 0)\
> random_array4 = np.random.randint(10, size = (5,3))\
> random_array4\
> [numpy.random.seed()](https://numpy.org/doc/2.3/reference/random/generated/numpy.random.seed.html)
## Viewing Arrays and Matrices
- **np.unique()** --> It is a function within the NumPy library in Python used to find the unique elements of an array. It returns a sorted array containing only the distinct values from the input array.
> np.unique(random_array4)\
> [numpy.unique()](https://numpy.org/doc/stable/reference/generated/numpy.unique.html)
## Manipulating and Comparing arrays
>[Broadcasting](https://numpy.org/doc/stable/user/basics.broadcasting.html)
- [Simple Arithmetic](https://www.w3schools.com/python/numpy/numpy_ufunc_simple_arithmetic.asp)
- [NumPy Logs](https://www.w3schools.com/python/numpy/numpy_ufunc_logs.asp)
- [Standard Deviation and Variance](https://www.mathsisfun.com/data/standard-deviation.html)
> a2 = np.array([[1,2.3,3.5],
                [4.7,5.6,6.3]])
- np.std(a2) -->  **. std()** function calculates the NumPy standard deviation of given data along a specified axis.
- np.var(a2) --> The numpy **.var()** function in Python's NumPy library calculates the variance of elements within an array.
## Reshaping and Transposing
- [NumPy Array Reshaping](https://www.w3schools.com/python/numpy/numpy_array_reshape.asp)
- [NumPy Array Transpose](https://numpy.org/devdocs/reference/generated/numpy.ndarray.T.html)
> a2.T\
> array([[1. , 4.7],
       [2.3, 5.6],
       [3.5, 6.3]])
## Dot product
>[How to Multiply Matrices](https://www.mathsisfun.com/algebra/matrix-multiplying.html)
- [numpy.dot()](https://numpy.org/devdocs/reference/generated/numpy.dot.html)
## Comparison Operators
- [Logic functions](https://numpy.org/doc/2.3/reference/routines.logic.html) 
## Sorting arrays
- [Methods](https://www.tutorialspoint.com/find-the-maximum-and-minimum-element-in-a-numpy-array)
- [numpy.argsort()](https://numpy.org/devdocs/reference/generated/numpy.argsort.html)
