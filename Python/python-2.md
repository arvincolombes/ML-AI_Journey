## Write a python program and using while loop to check whether a given number is prime or not

```python
num = int(input("Enter a number: "))

if num <= 1:
    print(num, "is not a prime number")
else:
    b = 2
    prime = True

    while b < num:
        if num % b == 0:
            prime = False
            break
        b += 1

    if prime:
        print(num, "is a prime number")
    else:
        print(num, "is not a prime number")

        Enter a number:  9
        9 is not a prime number    
          ```    
