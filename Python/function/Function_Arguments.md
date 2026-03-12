```python

```

#**Function Arguments**


```python
def greet(name, message):
  """
    This function greets to person with the provided message
  """
  print("hello {0} , {1}".format(name, message ))

greet('Arvin','hello')
```

    hello Arvin , hello
    


```python
#suppose if we pass one argument

greet('CHARANI')
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    /tmp/ipykernel_391/2277400115.py in <cell line: 0>()
          1 #suppose if we pass one argument
          2 
    ----> 3 greet('CHARANI')
    

    TypeError: greet() missing 1 required positional argument: 'message'


# Different Forms of Arguments
### We can provide a default value to an argument by using the assignment operator (=).


```python
def greet(name, msg="Good Morning" ):
    """
    This function greets to person with the provided message
    if message is not provided, it defaults to "Good Morning"
    """
    print(" Hello {0}, {1}".format(name, msg))



greet("raj","good")

```

     Hello raj, good
    


```python
greet("arvin")
```

     Hello arvin, Good Morning
    

# 2. Keyword Arguments
### kwargs allows you to pass keyworded variable length of arguments to a function. You should use **kwargs if you want to handle named arguments in a function

### In Python, **kwargs is a special syntax used in a function definition to accept an arbitrary number of keyword arguments (arguments passed as key=value). The arguments are collected into a dictionary within the function, where the keys are the argument names and the values are the argument values


```python
def greet(**kwargs):
  for key, value in kwargs.items():
    print(key, value)

greet(name="arvin", age=22, address="hyderabad")

```

    name arvin
    age 22
    address hyderabad
    


```python
def test(**kwarge):
  if kwarge:
    # Access 'name' and 'msg' from the kwarge dictionary
    print(f"hello {kwarge['name']} and {kwarge['msg']}")

test(name="arvin", msg="good Morning")
```

    hello arvin and good Morning
    

# 3. Arbitary Arguments

### Sometimes, we do not know in advance the number of arguments that will be passed into a function.Python allows us to handle this kind of situation through function calls with arbitrary number of arguments.


```python
def fun(*name):
  print("list tuple numbers : ", name)

fun(1,2,4)

```

    list tuple numbers :  (1, 2, 4)
    


```python
def bun(*name):
    s = 0
    for i in name:
      s += i
    print(s)

bun(1, 2, 3, 4, 5)


```

    15
    


```python
def factorial(num):
    """
    This is a recursive function to find the factorial of a given number
    """
    return 1 if num == 1 else (num * factorial(num-1))

num = 5
print ("Factorial of {0} is {1}".format(num, factorial(num))
```


      File "/tmp/ipykernel_1779/4064647510.py", line 8
        print ("Factorial of {0} is {1}".format(num, factorial(num))
                                                                    ^
    SyntaxError: incomplete input
    

