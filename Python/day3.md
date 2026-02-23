# Memoery References and ID
### When variables hold the same value, Python may use the same memory location (internal caching).



```python
a = 10
b = 20
print(id(a))
print(id(b))
```

    140725762045128
    140725762045448
    


```python
c=a
print(id(c))
```

    140725762045128
    


```python
d=e=f = 20
print((d))
print((e))
print((f))
print(id(d))
print(id(e))
print(id(f))
```

    20
    20
    20
    140725762045448
    140725762045448
    140725762045448
    

### Observation
*	If values are identical, Python reuses memory.
*	Variables become aliases of the same object.
Important Concept:
*	Value remains at memory location.
*	Variable names (aliases) may change.
*	Memory location of value does not change


# Data Types in Python


```python
a = 1    # integer 
b = 2.5  # floate
c = 'LM'   # String
d = True # boolen
e = (6+2j) # complex 
```


```python
print ( 'value of a : ', a , type(a)) 
print(' value of b : ',b , type(b))
print( 'Value of c : ', c  , type(c))
print('Value of d :  ', d , type(d))
print('Value of e : ', e , type(e))
```

    value of a :  1 <class 'int'>
     value of b :  2.5 <class 'float'>
    Value of c :  LM <class 'str'>
    Value of d :   True <class 'bool'>
    Value of e :  (6+2j) <class 'complex'>
    

type(a)
### Common Data Types:
*	int
*	float
*	complex
*	str
*	bool


## Type Casting
### Type casting converts one data type into another

print (int(5.4)) 
print(float(6))
print(str(10))

### Boolean conversion



```python
print (int(True)) 
print (int(False))
print (bool(1))
print (bool(0)) 
```

    1
    0
    True
    False
    

### Key Note:
*	True → 1
*	False → 0


## Strings and Indexing
### Strings are indexed starting from 0


```python
s = "This is Online AI Course" 
print(s[0])
print(s[5])
print(s[0:6])
print(s[1:15:2])
print(s[-2])
print(s[-6])
print(s[0:])
print(s[::-1])
```

    T
    i
    This i
    hsi nie
    s
    C
    This is Online AI Course
    esruoC IA enilnO si sihT
    

## Formatted Strings (f-strings)


```python
name = "Manoj"
line = 100
d = "Arvin"
c = "kumar"
e = 100
f = "good"

print(f"Congralution {name} , you worte {line} lines of code")
print(f"{d} full name is {c} and got {e} marks")
print(f"{name} and {d}{c} are {f} friends")  
```

    Congralution Manoj , you worte 100 lines of code
    Arvin full name is kumar and got 100 marks
    Manoj and Arvinkumar are good friends
    

### Why use f-strings?
*	Avoid manual type casting
*	Cleaner syntax
*	Supports expressions inside {}


## Input in Python


```python
num = input("Enter the number : ")
print(num , type(num))

```

    Enter the number :  Arvinkumar
    

    Arvinkumar <class 'str'>
    

num = input("Enter the number : ")
print(num , type(num))

## Important:
*	Input is always string.



```python
# take the input int and float ue below 
num = int(input("Enter the number :"))
print(num , 'is a ', type(num))

```

    Enter the number : 5
    

    5 is a  <class 'int'>
    


```python
num = float(input("Enter the float number : "))
print (num , 'is a' , type(num))

```

    Enter the float number :  5.4
    

    5.4 is a <class 'float'>
    

## Arithmetic Operators

*  (+) Addition
*  (-) Subtraction
*  (*) Multiplication
*  (/) Division
*  (//) Floor division
*  (%) Modulus
*  (**) Exponent



```python
print ( 5 + 5)
print ( 10 -5)
print (5 * 6)
print (10 /2 )
print ( 10//3)
print ( 100%30)
print (2 ** 2)
```

    10
    5
    30
    5.0
    3
    10
    4
    

## Comparison Operators

* (==) Equal to
* (!=) Not equal to
* (>) Greater than
* (<) Less than
* (>=) Greater than or equal to
* (<=) Less than or equal to


```python
# Equal to
print ( 5 == 5)
print( 10 != 5)
print( 10 > 5 )
print ( 10 < 5)
print ( 10 >= 10)
print ( 10 <= 5)
```

    True
    True
    True
    False
    True
    False
    

## Logical Operators

* and
* or
* not
### True and False  
### True or False
### not true    

## Bitwise Operators
### Operate on binary representations


```python
print ( 10 & 4)
print ( 10 | 4)
print ( 10 ^ 4)
print ( 10 >> 4 )
print ( 10 << 4)
```

    0
    14
    14
    0
    160
    

### Concept:
*	Right shift → divide by 2
*	Left shift → multiply by 2




```python
# If-Else Statements
```
