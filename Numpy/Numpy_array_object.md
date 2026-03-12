# The Numpy array object

# NumPy Arrays

**python objects:** 

1. high-level number objects: integers, floating point
2. containers: lists (costless insertion and append), dictionaries (fast lookup)

**Numpy provides:**
1. extension package to Python for multi-dimensional arrays
2. closer to hardware (efficiency)
3. designed for scientific computation (convenience)
4. Also known as array oriented computing


```python
import numpy as np
a=np.array([1,2,3,4,5])
print(a)
print(np.arange(10))
```

    [1 2 3 4 5]
    [0 1 2 3 4 5 6 7 8 9]
    

**Why it is useful:** Memory-efficient container that provides fast numerical operations.


```python
#python list
L = range(1000)
%timeit [i**2 for i in L]
#print(m)
```

    143 μs ± 18.3 μs per loop (mean ± std. dev. of 7 runs, 10,000 loops each)
    


```python
a = np.arange(1000)
%timeit (a**2)
```

    1.65 μs ± 231 ns per loop (mean ± std. dev. of 7 runs, 1,000,000 loops each)
    

# 1. Creating arrays

** 1.1.  Manual Construction of arrays**


```python
#1-D
a = np.array([1,2,3,4,5])
a
```




    array([1, 2, 3, 4, 5])




```python
#print dimensions
a.ndim
```




    1




```python
# shape
a.shape
```




    (5,)




```python
len(a)
```




    5




```python
# 2-D , 3 -D
b = np.array([[1,2,3], [4,5,6]])
b
```




    array([[1, 2, 3],
           [4, 5, 6]])




```python
b.ndim
```




    2




```python
b.shape
```




    (2, 3)




```python
len(b)
```




    2




```python
c = np.array([[[1,2,3], [4,5,6]], [[7,8,9],[10,11,12]]])
c
```




    array([[[ 1,  2,  3],
            [ 4,  5,  6]],
    
           [[ 7,  8,  9],
            [10, 11, 12]]])




```python
c.ndim
```




    3




```python
c.shape
```




    (2, 2, 3)




```python
len(c)
```




    2



** 1.2  Functions for creating arrays**


```python
#using arrange function

# arange is an array-valued version of the built-in Python range function

a = np.arange(10)
print(a)
```

    [0 1 2 3 4 5 6 7 8 9]
    


```python
b = np.arange(0, 10, 2)
b
```




    array([0, 2, 4, 6, 8])




```python
c= np.linspace(0, 1, 6)
c
```




    array([0. , 0.2, 0.4, 0.6, 0.8, 1. ])




```python
# common array

a = np.ones((3,3))
print(a)
a_1 = np.ones((2,2))
print(a_1)
```

    [[1. 1. 1.]
     [1. 1. 1.]
     [1. 1. 1.]]
    [[1. 1.]
     [1. 1.]]
    


```python
b= np.zeros((3,3))
b
```




    array([[0., 0., 0.],
           [0., 0., 0.],
           [0., 0., 0.]])




```python
c = np.eye(3) #Return a 2-D array with ones on the diagonal and zeros elsewhere.
c
```




    array([[1., 0., 0.],
           [0., 1., 0.],
           [0., 0., 1.]])




```python
d = np.eye(2)
d
```




    array([[1., 0.],
           [0., 1.]])




```python
d = np.eye(3,2) #3 is number of rows, 2 is number of columns, index of diagonal start with 0
d
```




    array([[1., 0.],
           [0., 1.],
           [0., 0.]])




```python
#create array using diag function
a = np.diag([1,2,3,4,5]) #construct a diagonal array.
a
```




    array([[1, 0, 0, 0, 0],
           [0, 2, 0, 0, 0],
           [0, 0, 3, 0, 0],
           [0, 0, 0, 4, 0],
           [0, 0, 0, 0, 5]])




```python
np.diag(a)
```




    array([1, 2, 3, 4, 5])




```python
#create array using random
#Create an array of the given shape and populate it with random samples from a uniform distribution over [0, 1).

a = np.random.rand(5)
a

```




    array([0.42869839, 0.03394714, 0.37966282, 0.01592543, 0.95892886])




```python
a = np.random.randn(4) #Return a sample (or samples) from the “standard normal” distribution.  ***Gausian***
a
```




    array([-1.59058872,  2.39486383, -0.98100846, -1.42320742])



**Note:**
    
For random samples from N(\mu, \sigma^2), use:

sigma * np.random.randn(...) + mu

### np.random.rand: Best when you need values within a strictly defined range where every value is equally likely, such as probability simulations or dropout masks in neural networks.
### np.random.randn: The standard choice for weight initialization in machine learning. Because most values cluster around zero, it helps avoid "exploding" or "vanishing" gradients that can happen if initial weights are too large or too far from zero. 


# 2. Basic DataTypes

You may have noticed that, in some instances, array elements are displayed with a **trailing dot (e.g. 2. vs 2)**. This is due to a difference in the **data-type** used:


```python
a = np.arange(10)
print(a)
a.dtype
```

    [0 1 2 3 4 5 6 7 8 9]
    




    dtype('int64')




```python
#You can explicitly specify which data-type you want:

b =  np.arange(10, dtype='float64')
b
```




    array([0., 1., 2., 3., 4., 5., 6., 7., 8., 9.])




```python
#The default data type is float for zeros and ones function
a = np.zeros((3,3))
print(a)
a.dtype
```

    [[0. 0. 0.]
     [0. 0. 0.]
     [0. 0. 0.]]
    




    dtype('float64')



**other datatypes**


```python
# d = np.array([2+1j, 4+6j])
d = np.array([2+1j, 4+6j])
print(d)
d.dtype

```

    [2.+1.j 4.+6.j]
    




    dtype('complex128')




```python
c = np.array([True, False, True, False])
print(c)
c.dtype

```

    [ True False  True False]
    




    dtype('bool')




```python
e = np.array(['raj','ram','arvin','bhavani'])
print(e)
e.dtype
```

    ['raj' 'ram' 'arvin' 'bhavani']
    




    dtype('<U7')




```python
s = np.array(['Ram', 'Robert', 'Rahim'])

s.dtype
```




    dtype('<U6')



**Each built-in data type has a character code that uniquely identifies it.**

'b' − boolean

'i' − (signed) integer

'u' − unsigned integer

'f' − floating-point

'c' − complex-floating point

'm' − timedelta

'M' − datetime

'O' − (Python) objects

'S', 'a' − (byte-)string

'U' − Unicode

'V' − raw data (void)

**For more details**
**https://docs.scipy.org/doc/numpy-1.10.1/user/basics.types.html**


# 3. Indexing and Slicing

**3.1 Indexing**

The items of an array can be accessed and assigned to the same way as other **Python sequences (e.g. lists)**:


```python
a = np.arange(10)
a
```




    array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
print(a[-1]) #indices begin at 0, like other Python sequences (and C/C++)
print(a[3])
```

    9
    3
    


```python
# For multidimensional arrays, indexes are tuples of integers:
b= np.diag([1, 2, 4])
print(b)
print(b[0,0])
print(b[0,1])
print(b[2,2])
print(b[2,1])
```

    [[1 0 0]
     [0 2 0]
     [0 0 4]]
    1
    0
    4
    0
    

**3.2 Slicing**


```python
a = np.arange(10)
a
```




    array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
a[1:8:2]
```




    array([1, 3, 5, 7])




```python
# Assign values
a[4] = 0
a
```




    array([0, 1, 2, 3, 0, 5, 6, 7, 8, 9])




```python
#we can also combine assignment and slicing:
a[6:] = 44
a
```




    array([ 0,  1,  2,  3,  0,  5, 44, 44, 44, 44])




```python
#assigning
print(a)
a[2] = a[-2]
a
```

    [ 0  1  2  3  0  5 44 44 44 44]
    




    array([ 0,  1, 44,  3,  0,  5, 44, 44, 44, 44])



# 4. Copies and Views

## A slicing operation creates a view on the original array, which is just a way of accessing array data. Thus the original array is not copied in memory. You can use **np.may_share_memory()** to check if two arrays share the same memory block. 

**When modifying the view, the original array is modified as well:**


```python
a = np.arange(10)
a
```




    array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
b = a[::2]
b
```




    array([0, 2, 4, 6, 8])




```python
np.shares_memory(a,b)
```




    True




```python
b[0] = 10
b
```




    array([10,  2,  4,  6,  8])




```python
a
```




    array([10,  1,  2,  3,  4,  5,  6,  7,  8,  9])




```python
a = np.arange(10)
print(a)

c = a[::2].copy() #force a copy
print(c)
```

    [0 1 2 3 4 5 6 7 8 9]
    [0 2 4 6 8]
    


```python
np.shares_memory(a,c)
```




    False




```python
c[0] = 11
print(c)
print(a)
```

    [11  2  4  6  8]
    [0 1 2 3 4 5 6 7 8 9]
    

# 5. Fancy Indexing

## NumPy arrays can be indexed with slices, but also with boolean or integer arrays **(masks)**. This method is called **fancy indexing**. It creates copies not views.

**Using Boolean Mask**


```python
a = np.random.randint(0, 20, 15)
a
```




    array([18,  9, 12,  7, 18, 17, 15, 18, 11, 12, 14, 13,  2,  3, 16],
          dtype=int32)




```python
mask = (a % 2 ==0)
mask
```




    array([ True, False,  True, False,  True, False, False,  True, False,
            True,  True, False,  True, False,  True])




```python
exract_mask_a = a[mask]
exract_mask_a
```




    array([18, 12, 18, 18, 12, 14,  2, 16], dtype=int32)



**Indexing with a mask can be very useful to assign a new value to a sub-array:**


```python
a[mask] = -1
a
```




    array([-1,  9, -1,  7, -1, 17, 15, -1, 11, -1, -1, 13, -1,  3, -1],
          dtype=int32)



**Indexing with an array of integers**


```python
a = np.arange(0, 100, 10)
a

```




    array([ 0, 10, 20, 30, 40, 50, 60, 70, 80, 90])




```python
#Indexing can be done with an array of integers, where the same index is repeated several time:
a[[2,4,6,7,8]]

```




    array([20, 40, 60, 70, 80])




```python
# New values can be assigned 
a[[2,7]] = -200
a
```




    array([   0,   10, -200,   30,   40,   50,   60, -200,   80,   90])




```python

```
