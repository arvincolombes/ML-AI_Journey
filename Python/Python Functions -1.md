 # python Functions

### Function is a group of related statements that perform a specific task.
### Functions help break our program into smaller and modular chunks. As our program grows larger and larger, functions make it more organized and manageable.

### It avoids repetition and makes code reusable.

# Syntax:
 def function_name(parameters)
  """
  Doc strings

  """
   statment(s)
  


1. keyword "def" marks the start of function header

2. Parameters (arguments) through which we pass values to a function. These are optional

3. A colon(:) to mark the end of funciton header

4. Doc string describe what the function does. This is optional

5. "return" statement to return a value from the function. This is optional


```python
def print_name(name):
    """
    this function print the name
    """
    print("hello" + str(name))
```

# Function Call
### Once we have defined a function, we can call it from anywhere


```python
print_name("arvin")
```

    helloarvin
    

# Doc String

### The first string after the function header is called the docstring and is short for documentation string.
### Although optional, documentation is a good programming practice, always document your code    
### Doc string will be written in triple quotes so that docstring can extend up to multiple lines


```python
print(print_name.__doc__) # print doc string of the function
```

    
    this function print the name
    
    

##  return Statement

### The return statement is used to exit a function and go back to the place from where it was called.

## Syntax:
###     return [expression]

-> return statement can contain an expression which gets evaluated and the value is returned.

-> if there is no expression in the statement or the return statement itself is not present inside a function, then the function will return None Object

def get_sum(lst):
    """
    This function returns the sum of all the elements in a list
    """
    sum = 0
    for num in lst:
            sum += num
    return sum


```python
s = get_sum([1,2,34,5])
print(s)
```

    42
    


```python
# print doc string
print(get_sum.__doc__)
```

    
    This function returns the sum of all the elements in a list
    
    

## Scope and Life Time of Variables

### -> Scope of a variable is the portion of a program where the variable is recognized
### -> variables defined inside a function is not visible from outside. Hence, they have a local scope.
### -> Lifetime of a variable is the period throughout which the variable exits in the memory. 
### -> The lifetime of variables inside a function is as long as the function executes.
### -> Variables are destroyed once we return from the function. 


```python
 global_var = "This is global variable"
 def test_life_time():
     """
     This function test the life time of a variables
     """
     local_var = "This is local variable"
     print(local_var)       #print local variable local_var
     print(global_var)      #print global variable global_var


```


```python
#calling function
test_life_time()
```

    This is local variable
    This is global variable
    


```python
#print global variable global_var
print(global_var)
```

    This is global variable
    


```python
#print local variable local_var
print(local_var)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[46], line 2
          1 #print local variable local_var
    ----> 2 print(local_var)
    

    NameError: name 'local_var' is not defined


### Python program to print Highest Common Factor (HCF) of two numbers


```python
def computeHCF(a, b):
    """
    Computing HCF of two numbers
    """
    smaller = b if a > b else a  #consice way of writing if else statement
    
    hcf = 1
    for i in range(1, smaller+1):
        if (a % i == 0) and (b % i == 0):
            hcf = i
    return hcf

num1 = 6
num2 = 36

print("H.C.F of {0} and {1} is: {2}".format(num1, num2, computeHCF(num1, num2)))
```

    H.C.F of 6 and 36 is: 6
    

# Types Of Functions

1. Built-in Functions

2. User-defined Functions


```python

```

### Built-in Functions

### 1. abs()


```python
# find the absolute value

num = -100
print(abs(num))
```

    100
    

### 1. all()

## return value of all() function

## True: if all elements in an iterable are true

## False: if any element in an iterable is false


```python
lst = [1, 2, 3, 4]
lst2 = [0,1, 3, 5, 6]

print(all(lst))
print(all(lst2))
```

    True
    False
    


```python
lst = []
print(all(lst))
```

    True
    


```python
lst = [False, 1, 3, 4]
all(lst)
```




    False



### dir()

The dir() tries to return a list of valid attributes of the object.

If the object has __dir__() method, the method will be called and must return the list of attributes.

If the object doesn't have __dir()__ method, this method tries to find information from the __dict__ attribute (if defined), and from type object. In this case, the list returned from dir() may not be complete.


```python
num = [1,2,3,4,5]

print(dir(num))
```

    ['__add__', '__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getstate__', '__gt__', '__hash__', '__iadd__', '__imul__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__rmul__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'append', 'clear', 'copy', 'count', 'extend', 'index', 'insert', 'pop', 'remove', 'reverse', 'sort']
    

## divmod()

### The divmod() method takes two numbers and returns a pair of numbers (a tuple) consisting of their quotient and remainder.


```python
print(divmod(9, 2))
print(divmod(10,4))
```

    (4, 1)
    (2, 2)
    

## enumerate()
### The enumerate() method adds counter to an iterable and returns it 
### syntax: enumerate(iterable, start=0)
In Python, the enumerate() function is a built-in tool that adds a counter to an iterable (like a list, tuple, or string) and returns it as an enumerate object. This is the "Pythonic" way to loop through a collection when you need both the index and the value of each item.


```python
numbers = [10,20,30,40]

for index, num in enumerate(numbers, 10):
        print(f"index {index} has value {num}")
```

    index 10 has value 10
    index 11 has value 20
    index 12 has value 30
    index 13 has value 40
    

## filter()
### The filter() method constructs an iterator from elements of an iterable for which a function returns true
### In Python, the filter() function is a built-in tool used to extract elements from an iterable (like a list, tuple, or set) that satisfy a specific condition. It works by applying a "filtering function" to each item and only keeping those for which the function returns True


```python
def find_postive_number(num):
    """
    this function return values
    """
    if num > 0:
        return num

```


```python
number_list = range(-10, 10)
print(list(number_list))

postive_number =  list(filter(find_postive_number, number_list))
print(postive_number)
```

    [-10, -9, -8, -7, -6, -5, -4, -3, -2, -1, 0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    [1, 2, 3, 4, 5, 6, 7, 8, 9]
    


```python
# fiter the even numbers
kill = [ 1, 2, 3, 4, 5, 6, 7, 8, 9]
def even(num):
    if num % 2 == 0: 
      return True


even_number = tuple(filter( even, kill))

print(even_number)

```

    (2, 4, 6, 8)
    


```python
 def odd(num):
     if num % 2 != 0:
         return True
 odd_number = tuple(filter( odd, kill))
 print(odd_number)                   
             
```

    (1, 3, 5, 7, 9)
    



## isinstance()
### The isinstance() function checks if the object (first argument) is an instance or subclass of classinfo class (second argument).
### syntax: isinstance(object, classinfo)


```python
lst = (1, 2, 3, 4, 5)
print(isinstance(lst, tuple))

```

    False
    


```python
t = (1, 2, 3, 4, 5)
print(isinstance(t, set))
```

    False
    


```python

```
