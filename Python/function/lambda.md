# Anonymous / Lambda Function

In Python, anonymous function is a function that is defined without a name.

While normal functions are defined using the def keyword, in Python anonymous functions are defined using the lambda keyword.

Lambda functions are used extensively along with built-in functions like filter(), map()

syntax:
    
    ## lambda arguments: expression


```python
print((lambda x,y: x*y)(6,7))
```

    42
    


```python
double = lambda x :x**2

print(double(6))
```

    36
    


```python
#Example use with filter()
lst = [1, 2, 3, 4, 5]
even_lst = list(filter(lambda x : x%2 == 0, lst))
print(even_lst)
```

    [2, 4]
    


```python
lst = [1,5,6,7,8]
square = list(map(lambda x : x**2 , lst))
print(square)
```

    [1, 25, 36, 49, 64]
    


```python
lst = [1,2,3,4,5]
from functools import reduce
sum = reduce(lambda x,y: x*y , lst)
print(sum)
```

    120
    
