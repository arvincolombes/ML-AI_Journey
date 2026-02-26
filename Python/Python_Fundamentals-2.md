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



## If-Else Statements

### Dession making strcture 


```python
num = int(input('Enter the number: '))
if num > 0:
    print('postive number')
else:
    print('negative number')      
          

```

    Enter the number:  0
    

    negative number
    


```python
nom = int(input('Enter the number: '))
if nom > 15:
    print ( nom , "gregater than 15")
    
print (nom , 'less than 15')     

```

    Enter the number:  20
    

    20 gregater than 15
    20 less than 15
    

### Simple if-else


```python
num = int(input('enter the number: '))
if num > 20:
  print ( num , 'greater than 20')
else:
  print ( num,  'less than 20')      
          
          
          
```

    enter the number:  25
    

    25 greater than 20
    

### Logical Operators with If..Else
We can combine multiple conditions using logical operators such as and, or, and not.


```python
age = int(input('Enter tha Number: '))
exp = int(input('Enter the Number: '))
# Using '>' operator & 'and' with if-else
if age > 23 and exp > 8:
    print("Eligible.")
else:  
    print("not Eligib;e")          
          

```

    Enter tha Number:  9
    Enter the Number:  5
    

    not Eligib;e
    

### If Else in One-line
If we need to execute a single statement inside the if or else block then one-line shorthand can be used.


```python
a = -2
res = "Positive" if a >= 0 else "negative"
print(res)
```

    negative
    

### Nested If Else Statement
Nested if...else statement occurs when if...else structure is placed inside another if or else block. Nested If..else allows the execution of specific code blocks based on a series of conditional checks


```python
i = int(input("Enter the number: "))
if i == 10:   
    #  First if statement
  if i < 15:
    print("i is smaller than 15") 
      # Nested - if statement
      # Will only be executed if statement above
      # it is true
  if i < 12:
    print("i is smaller than 12 too")
  else:
    print("i is greater than 15")
else:
  print("i is not equal to 10")

```

    Enter the number:  10
    

    i is smaller than 15
    i is smaller than 12 too
    

### if…elif…else Statement
if-elif-else statement in Python is used for multi-way decision-making. This allows us to check multiple conditions sequentially and execute a specific block of code when a condition is True. If none of the conditions are true, the else block is executed


```python
i = int(input('Enther the number : '))
    # Checking if i is equal to 10
if i == 10:
        print("i is 10")
    # Checking if i is equal to 15
elif i == 15:
        print("i is 15")
    # Checking if i is equal to 20
elif i == 20:
        print("i is 20")
    # If none of the above conditions are true
else:
        print('i is not present')
    
```

    Enther the number :  20
    

    i is 20
    

## While Loop

### Executes until condition becomes False.


```python
i = int(input('Enter the number: '))
while i < 10:
  print(i)
  i +=1

```

    Enter the number:  0
    

    0
    1
    2
    3
    4
    5
    6
    7
    8
    9
    

### Print Numbers from 10 to 15
### Write a program to print numbers from 10 to 15 using a while loop.
Expected Output: 10 11 12 13 14 15


```python
x = 10
while x <= 15:
    print( x , end=" ")
    x +=1
    

```

    10 11 12 13 14 15 

### Write a program to print the cubes of numbers from 1 to 5.



```python
y = 1
while y <= 5:
    print(y ** 3, end=" ")
    y +=1


```

    1 8 27 64 125 

### write a program to print odd number form 1 to 10


```python
y = 1
while y <= 10:
    if y % 2 !=0:
      print(y , end=' ')
    y +=1
```

    1 3 5 7 9 

### Write a program to calulate the product of numbers from 1 to 5


```python
product = 1
number = 1
while number <=5:
    product *=number
    number +=1
print( product)
```

    120
    

### Write a program to reverse each word in the sentence "Hello World" useing while loop


```python
setance = input("Enter a Sentence = ")
words = setance.split()
for word in words:
    i = len(word) -1
    while i>=0:
        print(word[i], end=" ")
        i -= 1
   # print(end= " ")


```

    Enter a Sentence =  Arvin kumar
    

    n i v r A r a m u k 


```python
word = input('Enter a word to check= ')
vowels = "aeiou"
count = 0
index = 0
while index < len(word):
    if word[index].lower() not in vowels and word[index].isalpha():
        count += 1
    index += 1
print(f"Number of consinants: {count}")    
    
    
```

    Enter a word to check=  arvin
    

    Number of consinants: 3
    

### Write a program to print the first 5 multiples of 3




```python
multiple = 3
count = 1
while count <= 5:
    print(multiple , end=' ')
    multiple += 3
    count += 1

```

    3 6 9 12 15 

### write a program to caculate 3 to the power of 4


```python
count =1
while count <=1 :
    print( 3 ** 4 )
    count +=1
     

```

    81
    

### Write a program to check if given number perfact squre or not 


```python
num = int(input("Enter the to check ="))
i = 1
is_perfact = False

while i * i <= num:
  if i * i == num:
      is_perfact = True
      break
  i +=1
if is_perfact:
        print(f"give {num} is perfact square")
else:
         print(f"give {num} is not a perfact square")   
```

    Enter the to check = 9
    

    give 9 is perfact square
    

## For Loop
### Used for traversal over sequences


```python
for iteam in [10, 20, 30]:
        print(iteam)
```

    10
    20
    30
    


```python
for iteam in range(5):
        print(iteam, end=" ")
```

    0 1 2 3 4 


```python
for iteam in range(2,10):
        print(iteam, end=" ")
```

    2 3 4 5 6 7 8 9 


```python
for iteam in range(2, 20, 5):
         print(iteam, end=" ")    
```

    2 7 12 17 


```python
for iteam in range( 20 , 0, -5):
        print(iteam, end=' ')
```

    20 15 10 5 

### Write program to print square of numbers  


```python
for i in range(1,10):
        print(i ** 2 ,end=' ')
```

    1 4 9 16 25 36 49 64 81 

### write a program to print even numbers 1 to 10


```python
for i in range (1,10):
    if i % 2 == 0 :
      print( i , end=' ')
```

    2 4 6 8 

### write the program to calculate the sum of the numbers from 1 to 10


```python
sum = 0
for i in range (1,11):
    sum += i        
print(sum)
```

    55
    

### Wrtie program to revers given string 




```python
name = str(input("Enter the string :"))
for i in range(len(name) -1 ,-1, -1):
        print(i)     
        #print( name[i] , end=' ')
```

    Enter the string : arvin
    

    4
    3
    2
    1
    0
    

### write a program to count the numbers of vowels from input strings


```python
word = str(input("Enther the string : "))
vol = 'aeiou'
count = 0 
for char in word:
    if char in vol:
        count +=1
print(f"Total vowels in {word} is {count}")        
              
```

    Enther the string :  python
    

    Total vowels in python is 1
    

### write a program to caculate the factorial of a given.
     


```python
n =5
factorial = 1
for i in range(1, n+1):
        factorial*= i
print(f"Factorial of {n} is {factorial}")   

```

    Factorial of 5 is 120
    

### write a program to check if a given number is prime or not


```python
num = int(input('Enter the number :'))
is_prime = True
for i in range(2, int(num **0.5) +1):
    if num % i == 0:
        is_prime = False
        break
if is_prime and num > 1:
    print(num, "is a prime member")
else:
    print(num, "is not a prime member")
    
```

    Enter the number : 7
    

    7 is a prime member
    

### count Occurrences of Each Character in a string


```python
num = input('enter the string')
char_count = {}
for char in num:
    if char in char_count:
        char_count[char] += 1
    else:
        char_count[char] = 1
print(char_count)        
        

```

    enter the string arvina
    

    {'a': 2, 'r': 1, 'v': 1, 'i': 1, 'n': 1}
    


```python

```
