```python
## map()
```

    1 "heeelo" 3
    ('1', ' ', '"', 'h', 'e', 'e', 'e', 'l', 'o', '"', ' ', '3')
    

## map()
### Map applies a function to all the items in an input_list.
### syntax: map(function_to_apply, list_of_inputs)


```python
numbers = [1, 2, 3, 4]
#normal method of computing num^2 for each element in the list.
sqare=[]
for i in numbers:
    sqare.append(i**2)
print(sqare) 
```

    [1, 4, 9, 16]
    


```python
numbers = [1, 2, 3, 4]

def poweroftwo(num):
    return num **2
s1=list(map(poweroftwo, numbers))    
print(s1)
```

    [1, 4, 9, 16]
    


```python
numbers = [ 1,2,3,4,5,6]

def evnodd(num):
    if num % 2 == 0:
        return num ** 2
    else:
        return num ** 3

r2 = list(map(evnodd, numbers))
print(str(r2))    
```

    [1, 4, 27, 16, 125, 36]
    


```python
input = list(map(int,input()))
print(input)
```

    []
    


```python

```


```python
#input2 = tuple(map(int,input()))
#print(input2)
# input2_1 = tuple(map(float,input()))
# print(input2_1)
input2_2 = tuple(map(str,input()))
print(input2_2)
```


```python
# input3= list(map(int,input()))
# print(input3)
input3_1= list(map(float,input()))
print(input3_1)
```

    12345
    [1.0, 2.0, 3.0, 4.0, 5.0]
    


```python
input4= set(map(int,input()))
print(input4)
```

    123456
    {1, 2, 3, 4, 5, 6}
    


```python
def find_positive_number(num):
    """
    This function returns the positive number if num is positive
    """
    if num > 0:
        return num
```

## reduce()

## reduse()
### reduce() function is for performing some computation on a list and  returning the result.
### It applies a rolling computation to sequential pairs of values in a list.


```python
#product of elemnts in a list
number = [1,2,3,4]
product=1
# traditional program without reduce()
for i in number:
  product *=i
print(product)



;
```

    24
    




    ''




```python
# with reduse()
number = [1,2,3,4]
from functools import reduce
def mult(x,y):
  return x*y
multipule = reduce(mult, number)

print(multipule)


```

    24
    

### 2. User-defined Functions
Functions that we define ourselves to do certain specific task are referred as user-defined functions
If we use functions written by others in the form of library, it can be termed as library functions.
### Advantages
1. User-defined functions help to decompose a large program into small segments which makes program easy to understand, maintain and debug.

2. If repeated code occurs in a program. Function can be used to include those codes and execute when needed by calling that function.

3. Programmars working on large project can divide the workload by making different functions.




```python
def product_numbers(a,b):
    product = a*b
    return product
num1 = 2
num2 = 3

print(f"product of {num1} and {num2} is {product_numbers(num1,num2)}")


```

    product of 2 and 3 is 6
    

### Python program to make a simple calculator that can add, subtract, multiply and division


```python
def add(a,b):
  return a+b

def subtract(a,b):
  return a-b

def multiply(a,b):
  return a*b

def devision(a,b):
  return a/b

print( "select any operation")

print(1,"addtion two values" )
print(2,"subract two values" )
print(3, "multiply two values" )
print(4, "devision two values")

choice = int(input("enter the choice 1/2/3/4 "))

num1 = int(input("Ente the first number :"))
num2 = int(input("Enter the 2nd number :"))

if choice == 1:
  print(f"addtion of {num1} and {num2} is {add(num1,num2)}")
elif choice == 2:
  print(f"subraction of {num1} and {num2} is {subtract(num1,num2)}")
elif choice == 3:
  print(f"multiply of {num1} and {num2} is {multiply(num1,num2)}" )
elif choice == 4:
  print(f"devision of {num1} and {num2} is {multiply(num1,num2)}")
else:
  print("invalit numbers ")

```

    select any operation
    1 addtion two values
    2 subract two values
    3 multiply two values
    4 devision two values
    
