## String

In Python, a string is a sequence of characters written inside quotes. It can include letters, numbers, symbols, and spaces.

* Python does not have a separate character type.
* A single character is treated as a string of length one.
* Strings are commonly used for text handling and manipulation.


```python
a = "arvin"
b = 'kumat'
print(a)
print(b)
```

    arvin
    kumat
    

### Multi-line Strings
Use triple quotes ('''...''' ) or ( """...""") for strings that span multiple lines. Newlines are preserved.


```python
a = """Arvin kumar 
learning  ML for
job chnages"""
print(a)
b = ''' bhavani is 
studing the MA pyschologies
in JAIN'''
print(b)
```

    Arvin kumar 
    learning  ML for
    job chnages
     bhavani is 
    studing the MA pyschologies
    in JAIN
    

### String Slicing
Strings are indexed sequences. Positive indices start at 0 from the left; negative indices start at -1 from the right 


```python
s = "arvinkumar is good guy"
print(s[0])    # first character
print(s[5])   # sixth character
print(s[-10]) # 11th  character
print(s[-5])  # 16th charatecter
print(s[1:4]) # characters from index 1 to 3
print(s[:3])  # from start to index 2 
print(s[3:]) # from index 3 to end
print(s[::-1]) # reverse the string
```

    a
    k
    s
    d
    rvi
    arv
    inkumar is good guy
    yug doog si ramuknivra
    

### String Iteration


```python
s = 'python'
for i in s:
    print(i)

```

    p
    y
    t
    h
    o
    n
    

### String Immutability
Strings are immutable, which means that they cannot be changed after they are created. If we need to manipulate strings then we can use methods like concatenation, slicing or formatting to create new strings based on original


```python
s = "arvinkumar"
s[0] = f
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[24], line 2
          1 s = "arvinkumar"
    ----> 2 s[0] = f
    

    NameError: name 'f' is not defined



```python
# In this example we are changing first character by building a new string.
s = 'A' + s[1:]
print(s)
```

    Arvinkumar
    

 ### Deleting string


```python
s = 'arvin'
del s

```

### Updating a String


```python
s = "hello Arvin"
s = 'g' + s[1:] 
print(s)
#print(b)
```

    gello Arvin
    


```python
print(b)
```

     bhavani is 
    studing the MA pyschologies
    in JAIN
    


```python
s = "hello Arvin"
s2 = s.replace("hello", "bhavani")
print(s2)
print(len(s2))
```

    bhavani Arvin
    13
    

### upper and Lower



```python
s = "Hello Arvin"
print(s.lower())
print(s.upper())
```

    hello arvin
    HELLO ARVIN
    

### strip and replace: strip removes leading and trailing whitespace from the string and replace() replaces all occurrences of a specified substring with another.


```python
s = "   Gfg   "
a = "Hello Arvin"
print(s.strip())
print (a.replace("Hello", "chnarani"))
```

    Gfg
    chnarani Arvin
    

### Concatenating and Repeating Strings


```python
a1 = "hello"
a2 = "charani"
print(a1 + " " +a2)
```

    hello charani
    


```python
a = "hello"
print( a  *  3)
```

    hellohellohello
    

### Using format()


```python
s = "My name is {} and my age is {}.".format("Arvin", 22)
print(s)
```

    My name is Arvin and my age is 22.
    

### String Membership Testing


```python
a = "i love my self"
print("i" in a)
print("love" in a)
print("a" in a)

```

    True
    True
    False
    

### String Comparison in Python


```python
s1 ="apple"
s2 = "banna"
print(s1 == s2)
print(s1 != s2)
# "apple" comes before "banana" lexicographically, therefore it is Tru
print( s1 < s2)
```

    False
    True
    True
    

### Using startswith() and endswith() Methods


```python
a = "arvin kumar"
print(a.startswith("arvin"))
print(a.endswith("kumar"))
```

    True
    True
    

### Convert integer to string in Python


```python
n = 12
s= str(n)
print ( s ," ", type(s))

```

    12   <class 'str'>
    

#### Using f-strings


```python
n= 14
m = f"{n}"
print( m , " ", type(m))
```

    14   <class 'str'>
    

## Lists

### In Python, a list is a built-in data structure that can hold an ordered collection of items. Unlike arrays in some languages, Python lists are very flexible:
* Can contain duplicate items
* Mutable: items can be modified, replaced, or removed
* Ordered: maintains the order in which items are added
* Index-based: items are accessed using their position (starting from 0)
* Can store mixed data types (integers, strings, booleans, even other lists)

### Using Square Brackets


```python
a = [1,2,3,4,5,]  # list of ingers
b = ['apple','banana','cherry'] # List of stringes
c = [1,'hello',3.4, True] # mixted data types

print (c)
print (a)
print (b)

```

    [1, 'hello', 3.4, True]
    [1, 2, 3, 4, 5]
    ['apple', 'banana', 'cherry']
    

#### Using list() Constructor


```python
a = list((1,2,3,'apple',4.5))
print(a)
b = list("CFG")
print(b)
```

    [1, 2, 3, 'apple', 4.5]
    ['C', 'F', 'G']
    


```python
a = [2] * 5
b = [3] * 6
print(a)
print(b)
```

    [2, 2, 2, 2, 2]
    [3, 3, 3, 3, 3, 3]
    

### Accessing List Elements


```python
a = [ 10, 20, 30, 40, 50]
print(a[0])
print(a[-1])
print(a[1:4])
print(a[::-1])   
```

    10
    50
    [20, 30, 40]
    [50, 40, 30, 20, 10]
    

### Adding Elements into List
#### * append(): Adds an element at the end of the list.
#### * extend(): Adds multiple elements to the end of the list.
#### * insert(): Adds an element at a specific position.
#### * clear(): removes all items.


```python
a = [ 10, 20, 30, 40, 50]
a.append(5)
print(a)
```

    [10, 20, 30, 40, 50, 5]
    


```python
a.insert(7, 8)

```


```python
print(a)
```

    [10, 20, 30, 40, 50, 5, 8]
    


```python
a.extend([60,70,80])
print(a)
```

    [10, 20, 30, 40, 50, 5, 8, 60, 70, 80]
    


```python
a.clear()
print(a)
```

    []
    


```python
lst = ['one','two','three']
lst.insert(1, 'three')
print(lst)
```

    ['one', 'three', 'two', 'three']
    


```python
# append
lst = [1,2,3,4] 
lst2=[5,4]
lst.append(lst2)
print(lst)
lst = [1,2,3,4]
lst2=[5,4]
lst.extend(lst2)
print(lst)
```

    [1, 2, 3, 4, [5, 4]]
    [1, 2, 3, 4, 5, 4]
    


```python
lst = ['one','two','three','four']
del lst[1]
print(lst)
```

    ['one', 'three', 'four']
    


```python
lst.pop(1)
print(lst)
```

    ['one', 'four']
    


```python
lst.extend('six','seven')
print(lst)

```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[14], line 1
    ----> 1 lst.extend('six','seven')
          2 print(lst)
    

    TypeError: list.extend() takes exactly one argument (2 given)



```python

```

### Removing Elements from List
* remove(): Removes the first occurrence of an element.
* pop(): Removes the element at a specific index or the last element if no index is specified.
* del statement: Deletes an element at a specified index.


```python

```


```python
b= [1,2,3,5,6,8]
b.remove(2)
print(b)
b.pop(1)
print(b)
del b[0]
print(b)
```

    [1, 3, 5, 6, 8]
    [1, 5, 6, 8]
    [5, 6, 8]
    


```python

```


```python
a = ['apple','banana','mango']
for i in a:
    print(i)
```

    apple
    banana
    mango
    

### List lenth 


```python
l = ['one','two','3','four']
len(l)
```




    4




```python
l.insert
```

### Sring split to create a  list


```python
s = "one,two,three,foue,five,"
slit = s.split(',')
print(slit)
```

    ['one', 'two', 'three', 'foue', 'five', '']
    


```python
s= "this aplied to AI training"
s1 = s.split() #default split is white-character: space or tab
print(s1)
```

    ['this', 'aplied', 'to', 'AI', 'training']
    

### List Count


```python
numbers = [1,2,1,4,5,2,7]
print(numbers.count(1))
print(numbers.count(2))
```

    2
    2
    

### list looping 


```python
lst = ['one','two',3,3.4,'five']

for i in lst:
    print(i)
```

    one
    two
    3
    3.4
    five
    

### List Comprehensions
*  List comprehensions provide a concise way to create lists.

* Common applications are to make new lists where each element is the result of some operations applied to each member of another sequence 
or iterable, or to create a subsequence of those elements that satisfy a certain condition.


```python
# without list comprehension
square = []
for i in range(10):
        square.append(i**2)
print(square)
```

    [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
    


```python
# example 

lst = [10,20,-30,-40,50,60]
new_lst = [i*2 for i in lst]
print(new_lst)

new_lst1 = [ i for i in lst if i >=0 ]
print(new_lst1)

new_lst2 = [(i, i**2) for i in range (10)]
print(new_lst2)
```

    [20, 40, -60, -80, 100, 120]
    [10, 20, 50, 60]
    [(0, 0), (1, 1), (2, 4), (3, 9), (4, 16), (5, 25), (6, 36), (7, 49), (8, 64), (9, 81)]
    

### Nested List Comprehensions


```python
matrix = [
    [1, 2, 3, 4],
    [6, 6, 7, 8],
    [9, 10, 11, 12]
]

t = []
for i in range(4):
    lst = []
    for row in matrix:
        lst.append(row[i])
        t.append(lst)
print(t)     

#print(matrix)
```

    [[1, 6, 9], [1, 6, 9], [1, 6, 9], [2, 6, 10], [2, 6, 10], [2, 6, 10], [3, 7, 11], [3, 7, 11], [3, 7, 11], [4, 8, 12], [4, 8, 12], [4, 8, 12]]
    


```python
transposed = [[row[i] for row in matrix] for i in range(4)]
print(transposed)
```

    [[1, 6, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]
    

## TUPLES

* A tuple is similar to list

* The diffence between the two is that we can't change the elements of tuple once it is assigned whereas in the list, elements can be changed


```python
# empty
t = ()
print(t)

tp = (1,2,3,4,6)
print(tp)
#mixed values
tup = ('raju', 2.5, 4, 'ramu', 5, 6 )
print(tup)
```

    ()
    (1, 2, 3, 4, 6)
    ('raju', 2.5, 4, 'ramu', 5, 6)
    


```python
# only parenthes not enought
t = ('arvin')
type(t)
```




    str




```python
# need coma at the end
t = ('arvin',)
type(t)
```




    tuple




```python
# parenthes are oprtinal
t = "rame",
print(type(t))
```

    <class 'tuple'>
    

### Accessing Elements in Tuple


```python
t = ("raju", "ramu", "rani", "arin")
print(t[0])
print(t[-1])
print(t[0:2])
print(t[::-1])
```

    raju
    arin
    ('raju', 'ramu')
    ('arin', 'rani', 'ramu', 'raju')
    


```python
t = ( "sri", ("chandra", "kavit" , "bhavani", "sharada"))
print(t)
```

    ('sri', ('chandra', 'kavit', 'bhavani', 'sharada'))
    


```python
print(t[1][1])
print(t[1][-1])
print(t[1][::-1])
```

    kavit
    sharada
    ('sharada', 'bhavani', 'kavit', 'chandra')
    


```python
# slicing
t = (1,2,3,4,6,7)
print(t[1:4])
print(t[:-2])
print(t[:])
print(t[::-1])
```

    (2, 3, 4)
    (1, 2, 3, 4)
    (1, 2, 3, 4, 6, 7)
    (7, 6, 4, 3, 2, 1)
    

### Changing a Tuple
* unlike lists, tuples are immutable
* This means that elements of a tuple cannot be changed once it has been assigned. But, if the element is itself a mutable
  datatype like list, its nested items can be changed.


```python
##creating tuple
t = (1,2,3,4,[5,6,7])
print (t)
t[2] = x #will get TypeError
```

    (1, 2, 3, 4, [5, 6, 7])
    


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[33], line 4
          2 t = (1,2,3,4,[5,6,7])
          3 print (t)
    ----> 4 t[2] = x
    

    NameError: name 'x' is not defined



```python
t[4][1] = 'arvin'
print(t)
```

    (1, 2, 3, 4, [5, 'arvin', 7])
    


```python
#concatinating tuples
t = (1, 2, 3) + (4, 5, 6)
print(t)
```

    (1, 2, 3, 4, 5, 6)
    


```python
t = (("arvin",) * 4)
print(t)
```

    ('arvin', 'arvin', 'arvin', 'arvin')
    

### Tuple Deletion


```python
# we cannot change the elements in a tuple. 
# That also means we cannot delete or remove items from a tuple.
t = (1,2,3,4,5,6)
del t
print(t)
```


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[44], line 5
          3 t = (1,2,3,4,5,6)
          4 del t
    ----> 5 print(t)
    

    NameError: name 't' is not defined


### tuple count 


```python
t = (1,2,3,5,5,6,6)
print(len(t))
print(t.count(5))
```

    7
    2
    

### Tuple index


```python

t = (1,2,3,5,5,6,6)
print(t.index(3))
```

    2
    

### Tuple Memebership 


```python
#test if an item exists in a tuple or not, using the keyword in.
t = (1,2,3,4,5,6)
print( 1 in t)
print( 0 not in t)
print( 7 in t)
```

    True
    True
    False
    

### Built in Functions

### Tuple Length


```python
t = (1,2,3,4,6,7)
print(len(t))
```

    6
    

### tuple sort 


```python
t = (1,3,2,7,5)
new_t = sorted(t)
print(new_t)
#Take elements in the tuple and return a new sorted list 
#(does not sort the tuple itself).
```

    [1, 2, 3, 5, 7]
    


```python
#get the largest element in a tuple
t = (1,3,2,7,5)
print(max(t))
print(min(t))
print(sum(t))

```

    7
    1
    18
    

# SETS

-> A set is an unordered collection of items. Every element is unique (no duplicates).

-> The set itself is mutable. We can add or remove items from it.

-> Sets can be used to perform mathematical set operations like union, intersection, symmetric difference etc.


```python
# set of integers 
s = {1, 2, 3}
print(s)
print(type(s))
```

    {1, 2, 3}
    <class 'set'>
    


```python
#set doesn't allow duplicates. They store only one instance.
s = { 1, 1, 2, 3, 3, 4, 5, 6 }
print(s)
```

    {1, 2, 3, 4, 5, 6}
    


```python
# conver the set to list
s = set([1, 2, 3, 4])
print(s)
print(type(s))
```

    {1, 2, 3, 4}
    <class 'set'>
    

### Add element to a Set

### set object doesn't support indexing


```python
s1 = {1,2}
print(s1[0])
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[80], line 2
          1 s1 = {1,2}
    ----> 2 print(s1[0])
    

    TypeError: 'set' object is not subscriptable



```python
# add element 
s1.add(3)
print(s1)
```

    {1, 2, 3}
    


```python
# add mutiple elements 
s1.update([4,5,6,7])
print(s1)
```

    {1, 2, 3, 4, 5, 6, 7}
    

### Remove elements from a Set


```python
s = {1,2,3,4,5,6}
print(s)
s.discard(4)
print(s)
s.remove(3)
print(s)
```

    {1, 2, 3, 4, 5, 6}
    {1, 2, 3, 5, 6}
    {1, 2, 5, 6}
    


```python
#remove an element not present in a set s
s.remove(7) # will get KeyError
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    Cell In[87], line 2
          1 #remove an element not present in a set s
    ----> 2 s.remove(7) # will get KeyError
    

    KeyError: 7



```python
#discard an element not present in a set s
s.discard(7)
print(s)
```

    {1, 2, 5, 6}
    


```python
###we can remove item using pop() method
s = {1,2,3,4,5,6}
s.pop()
print(s)
```

    {2, 3, 4, 5, 6}
    


```python
s.pop()
print(s)
```

    {3, 4, 5, 6}
    


```python
#remove all items in set using clear() method
s = {1,2,3,4,5,6}
s.clear()
print(s)
```

    set()
    

### Python Set Operations


```python
s1 = {1,2,3,4}
s2 = {3,4,5,6,8}
#union of 2 sets using | operator
s1 | s2

```




    {1, 2, 3, 4, 5, 6, 8}




```python
#another way of getting union of 2 sets
print(s1.union(s2))
```

    {1, 2, 3, 4, 5, 6, 8}
    


```python
#intersection of 2 sets using & operator
print( s1 & s2)
```

    {3, 4}
    


```python
#use the interdection function
print(s1.intersection(s2))
```

    {3, 4}
    


```python
#set Difference: set of elements that are only in set1 but not in set2
print( s1 - s2)
print(s1.difference(s2))
```

    {1, 2}
    {1, 2}
    


```python
"""symmetric difference: set of elements in both set1 and set2 
#except those that are common in both."""
print(s1 ^ s2)
print(s1.symmetric_difference(s2))
```

    {1, 2, 5, 6, 8}
    {1, 2, 5, 6, 8}
    

### is susbset 


```python
x = {"a","b","c","d","e"}
y = {"c","d"}
print("set x subset of y ?:", x.issubset(y))
print(" set y subset of x?:", y.issubset(x))
```

    set x subset of y ?: False
     set y subset of x?: True
    

## Frozen Sets

* Frozen sets has the characteristics of sets, but we can't be changed once it's assigned. While tuple are immutable lists,
  frozen sets are immutable sets
* Frozensets can be created using the function frozenset()
* Sets being mutable are unhashable, so they can't be used as dictionary keys. On the other hand, frozensets are hashable and
  can be used as keys to a dictionary.


```python
s1 = frozenset([1,2,3,4])
s2 = frozenset([4,5,6,7,8])
print(s1)
print(s2)

```

    frozenset({1, 2, 3, 4})
    frozenset({4, 5, 6, 7, 8})
    


```python
s1.add(5)
#try to add element into set1 gives an error
```


    ---------------------------------------------------------------------------

    AttributeError                            Traceback (most recent call last)

    Cell In[114], line 1
    ----> 1 s1.add(5)
          2 #try to add element into set1 gives an error
    

    AttributeError: 'frozenset' object has no attribute 'add'



```python
# frozen set doesn't support indexing
print(s1[1])
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[115], line 2
          1 # frozen set doesn't support indexing
    ----> 2 print(s1[1])
    

    TypeError: 'frozenset' object is not subscriptable



```python
print( s1 | s2)
```

    frozenset({1, 2, 3, 4, 5, 6, 7, 8})
    


```python
#intersection of two sets
print( s1 & s2)
```

    frozenset({4})
    


```python
# symmetric difference
print(s1 ^ s2)
print(s1.symmetric_difference(s2))
```

    frozenset({1, 2, 3, 5, 6, 7, 8})
    frozenset({1, 2, 3, 5, 6, 7, 8})
    

## Dictionary

### Python dictionary is an unordered collection of items. While other compound data types have only value as an element, a dictionary has a key: value pair.


```python
#empty dictionary
dit = {}
print(dit, type(dit))

# dict with mixed values 
dict = { 'name':'arvin', 1:['charani','sharada']}
print(dict)

#my_dict = dict()
#print(my_dict)

my_dict = dict([(1, 'abc'), (2, 'xyz')])
print(my_dict)
```

    {} <class 'dict'>
    {'name': 'arvin', 1: ['charani', 'sharada']}
    


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    Cell In[133], line 12
          7 print(dict)
          9 #my_dict = dict()
         10 #print(my_dict)
    ---> 12 my_dict = dict([(1, 'abc'), (2, 'xyz')])
         13 print(my_dict)
    

    TypeError: 'dict' object is not callable


### Dict Access


```python
my_dict = { 'name':'arvin', 'Age':27 , 'Address':'wanaparthy' }
print(my_dict)
print(my_dict['name'])
#another way of accessing key
print(my_dict.get('Address'))
```

    {'name': 'arvin', 'Age': 27, 'Address': 'wanaparthy'}
    arvin
    wanaparthy
    


```python
#if key is not present it gives KeyError
print(my_dict['raj'])
```


    ---------------------------------------------------------------------------

    KeyError                                  Traceback (most recent call last)

    Cell In[139], line 2
          1 #if key is not present it gives KeyError
    ----> 2 print(my_dict['raj'])
    

    KeyError: 'raj'



```python
#if key is not present it will give None using get method
print(my_dict.get('raj'))
```

    None
    

### Dict Add or Modify  Elements


```python
my_dict = { 'name':'arvin', 'Age':27 , 'Address':'wanaparthy' }
print(my_dict)
my_dict['name'] = 'bhavani'
my_dict['Address'] = 'annvaram'
print(my_dict)
```

    {'name': 'arvin', 'Age': 27, 'Address': 'wanaparthy'}
    {'name': 'bhavani', 'Age': 27, 'Address': 'annvaram'}
    

### # Dict Delete or Remove Element


```python
dict = { 'name':'arvin', 'Age':27 , 'Address':'wanaparthy' }
print(dict.pop('Age'))
print(dict)
```

    27
    {'name': 'arvin', 'Address': 'wanaparthy'}
    


```python
dict = { 'name':'arvin', 'Age':27 , 'Address':'wanaparthy' }
dict.popitem()
print(dict)
```

    {'name': 'arvin', 'Age': 27}
    


```python
sqr = {2:4, 3:5, 6:7}
print(sqr)
```

    {2: 4, 3: 5, 6: 7}
    


```python
sqr.clear()
print(sqr)
```

    {}
    


```python
sqr = {2:4, 3:5, 6:7}
print(sqr)
del sqr
print(sqr)
```

    {2: 4, 3: 5, 6: 7}
    


    ---------------------------------------------------------------------------

    NameError                                 Traceback (most recent call last)

    Cell In[160], line 4
          2 print(sqr)
          3 del sqr
    ----> 4 print(sqr)
    

    NameError: name 'sqr' is not defined


### Dictionary Methods


```python
squares = {2: 4, 3: 9, 4: 16, 5: 25}

my_dt = squares.copy()

print(my_dt)
```

    {2: 4, 3: 9, 4: 16, 5: 25}
    


```python
#fromkeys[seq[, v]] -> Return a new dictionary with keys from seq and value equal to v (defaults to None).
sub = {}.fromkeys(['Math','English','hindi'],1)
print(sub)
```

    {'Math': 1, 'English': 1, 'hindi': 1}
    


```python
#return a new view of the dictionary items (key, value)
sub = {2:4, 3:9, 4:16, 5:25}
print(sub.items())

```

    dict_items([(2, 4), (3, 9), (4, 16), (5, 25)])
    


```python
sub = {2:4, 3:9, 4:16, 5:25}

print(sub.keys())  #return a new view of the dictionary keys
```

    dict_keys([2, 3, 4, 5])
    


```python
sub = {2:4, 3:9, 4:16, 5:25}
print(sub.values())
```

    dict_values([4, 9, 16, 25])
    


```python
#get list of all available methods and attributes of dictionary

d = {}
print(dir(d))
```

    ['__class__', '__class_getitem__', '__contains__', '__delattr__', '__delitem__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getstate__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__ior__', '__iter__', '__le__', '__len__', '__lt__', '__ne__', '__new__', '__or__', '__reduce__', '__reduce_ex__', '__repr__', '__reversed__', '__ror__', '__setattr__', '__setitem__', '__sizeof__', '__str__', '__subclasshook__', 'clear', 'copy', 'fromkeys', 'get', 'items', 'keys', 'pop', 'popitem', 'setdefault', 'update', 'values']
    

### Dict Comprehension


```python
d = {'a': 1, 'b': 2, 'c': 3}
for i in d.items():
    print(i)
```

    ('a', 1)
    ('b', 2)
    ('c', 3)
    


```python
d = {'a': 1, 'b': 2, 'c': 3, 'd': 4}
new_dict = {k:v for k, v in d.items() if v > 2}
print(new_dict)
```

    {'c': 3, 'd': 4}
    


```python
#We can also perform operations on the key value pairs
d = {'a':1,'b':2,'c':3,'d':4,'e':5}
d = {k + 'c':v * 2 for k, v in d.items() if v > 2}
print(d)
```

    {'cc': 6, 'dc': 8, 'ec': 10}
    


```python

```
