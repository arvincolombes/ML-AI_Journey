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
```python
     1dit = "bat"
     Cell In[21], line 1
    1dit = "bat"
SyntaxError: invalid decimal literal    
```
  ```python
      async = "wicket"
        Cell In[23], line 1
    async = "wicket"          
SyntaxError: invalid syntax  
````
# Single Line comment  
```python
# this python practise
```
# Multi-line Comments (using #)
When comments need to span several lines, you can put it at the start of each line. This keeps each line clearly a comment.
```python
#The following three lines are regulor single-Line comments
#They share ignored when the progras
#the single-tine caveents to lai mult details in stels  
```
# Multi-line Comments (single and triple quotes)
single quotes (') are used to define string literals. They are functionally identical to double quotes (")   
triple-quotes strings can span multiple lines and are often used for socstrings, they can also serve as long comments when placed where code execution will ignore them  
Trinle quoted strings can multiple lines   
They are often used for socstringe (documentation) or tong coments.  
```python
'this python practise'
 'this python practise'  
 
''' this python roadmap
 for ML jourey
 thans for watchin'''    
 
'this python roadmap\n for ML jourey\n thans for watchin'
```
## Variables ##

This notebook explains basic Python data concepts. Read each short note, then run the code cells to see examples
*
What is a variable?
A variable is a name that refers to a piece of data stored in the computer's memory. In Python you do not need to numbers and underscores and do not start with a number. a type assigning a value creates the variable Good variable names use letters
Variable Assignments
Use the equals sign to store a value in a variable. The left side is the name, the right side is the value.
Assign values to variables and shas thetr types
10
b-5.5
print(", type, type(s))
print('b, type, type(b))
print type, type(c))
Multiple Assignments
Python allows assigning several variables in one line, or assigning the same value to multiple name
Simple
b, 10, 5.5, M
04
Python 3 (pyliemedle
Mode Cortimand
ALLOT фу
Hamid
Arvinkumar
Revendra
Manoj Kumar Arram
R
