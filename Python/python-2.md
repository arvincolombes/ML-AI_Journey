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
   
## Write python program using for loop print the all prime numbers within a input intervel
```python
start = int(input("Enter the start of interval: "))
end = int(input("Enter the end of interval: "))

print(f"Prime numbers between {start} and {end} are:")

for num in range(start, end + 1):
    if num > 1:   # prime numbers are greater than 1
        is_prime = True
        for i in range(2, int(num**0.5) + 1):  # check divisors up to sqrt(num)
            if num % i == 0:
                is_prime = False
                break
        if is_prime:
            print(num)
```
---

  
