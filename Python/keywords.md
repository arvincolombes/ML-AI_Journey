# __Python Keyword__

Keywords in Python are special reserved words that are part of the language itself. They define the rules and structure of Python programs which means you cannot use them as names for your variables, functions, classes or any other identifiers.
```python
import keyword

print("The list of keywords are : ")
print(keyword.kwlist)


The list of keywords are: 
['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await', 'break', 'class', 'continue', 'def', 'del', 'elif', 'else', 'except', 'finally', 'for', 'from', 'global', 'if', 'import', 'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise', 'return', 'try', 'while', 'with', 'yield']
```


# __Identifiers__

Identifier is the name given to entities like class, functions, variables etc. in Python. It helps differentiating one entity from another.
Rules for Writing Identifiers:
1. Identifiers can be a combination of letters in lowercase (a to z) or uppercase (A to Z) or digits (0 to 9) or an underscore ().
2. An identifier cannot start with a digit. Ivariable is invalid, but variablel is perfectly fine
3. Keywords cannot be used as identifiers.

   ```python
   Rajesh_3 = "ball"
   print(Rajesh_3)
   ball
   ```
   ---
```python
     1dit = "bat"
     Cell In[21], line 1
    1dit = "bat"
SyntaxError: invalid decimal literal    
```
---
  ```python
      async = "wicket"
        Cell In[23], line 1
    async = "wicket"          
SyntaxError: invalid syntax  
````
---
# Single Line comment  
```python
# this python practise
```
---  
# Multi-line Comments (using #)
When comments need to span several lines, you can put it at the start of each line. This keeps each line clearly a comment.
```python
#The following three lines are regulor single-Line comments
#They share ignored when the progras
#the single-tine caveents to lai mult details in stels  
```
---
# Multi-line Comments (single and triple quotes) #
single quotes (') are used to define string literals. They are functionally identical to double quotes (")   
triple-quotes strings can span multiple lines and are often used for socstrings, they can also serve as long comments when placed where code execution will ignore them  
Trinle quoted strings can multiple lines   
They are often used for socstringe (documentation) or tong coments.
---
```python
'this python practise'
 'this python practise'  
 
''' this python roadmap
 for ML jourey
 thans for watchin'''    
 
'this python roadmap\n for ML jourey\n thans for watchin'
```
---
# Doc strings (module/function/class documentation) 
* documentation strings are string literals that appear as the first statement in a module, function, class, or method definition. Unlike regular comments, docstrings are stored as metadata and can be accessed at runtime
* The __doc__ attribute is a special attribute in Python that stores the documentation string (docstring) for a function, class, or module
```python
def add_numbers(a,b):
  ''' the recolate the 
   work loaction.'''
  return a + b
print(add_numbers(5, 4))
print(add_numbers.__doc__)
9
the recolate the 
work loaction.
```
---
```python
def doc_string_example():
    '''
    this is the doc string of a funtction name doc_string_example
    '''
    return 'hello'
print(doc_string_example.__doc__)
this is the doc string of a funtction name doc_string_example
```
---
```python
def no_doc_string():
    return 'return stat'
print(no_doc_string.__doc__)
None
```
---  
# Varible Assigments and examples 
```python
a = 1
print (a)
1
```
---

```python
a = 18; b=20; c=30
print( a,b,c,)
18 20 30
```
---
```python 
d = 40
e = 50
f = 60
print( d,e,c)
40 50 30
```
---
```python
a=b=c=7
print(a)
print(b)
print(c)
7
7
7
```
---
