# Project Euler answers in python
Hello folks, Are you a beginner in Python and trying to solve basic functions to improve your python knowledge and try testing yourself with Hackerrank or some other platforms to create a basic portfolio? then this repo might help you in right sense.

Questions taken from Project Euler Archives and addressed the piece of codes in Python.


**#Q1 - If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23. Find the sum of all the multiples of 3 or 5 below 1000.**

```python
def sum_of_multiples_of_3_or_5(max_limit):
    a = 0
    for i in range(1,max_limit):
        if i%3==0 or i%5==0:
            a += i
    print("Sum of multiples of 3/5 till {} is {}".format(max_limit,a))
```

**#Q2 - Each new term in the Fibonacci sequence is generated by adding the previous two terms. By starting with 1 and 2, the first 10 terms will be: 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, ... By considering the terms in the Fibonacci sequence whose values do not exceed four million, find the sum of the even-valued term s.**

```python

def sum_of_even_valued_fibonacci():
    i=int(input("sum of fibonacci sequence value below = "))
    a ,b = 1,2
    x = []
    fib_seq = [1,2]
    while b<i:
        a,b = b,a+b
        if b<i:
            fib_seq.append(b)
    print(fib_seq)
    for i in fib_seq:
        if i%2 == 0:
            x.append(i)
    print(x)
    print("sum of even valued terms",sum(x))

```
Or if you wanted to get in short piece of codes, use the below

```python

def sum_of_even_valued_fibonacci():
    i=int(input("sum of fibonacci sequence value = "))
    a ,b = 1,2
    x = 0
    while b<i:
        if b%2 ==0:
            x += b
        a,b = b,a+b
    print("sum of even valued terms",x)

```

**#Q3 - The prime factors of 13195 are 5, 7, 13 and 29. What is the largest prime factor of the number 600851475143 ?**

```python

def Largest_Prime_Factor(n):
    prime_factor = 1
    i=2
    
    while i <= n / i:
        if n%i == 0:
            prime_factor = i
            n/= i
        else:
            i += 1
    if prime_factor < n:
        prime_factor = n
    return prime_factor

```

**#Q4 - A palindromic number reads the same both ways. The largest palindrome made from the product of two 2-digit numbers is 9009 = 91 × 99. Find the largest palindrome made from the product of two 3-digit numbers.**

```python

def largest_palindrome(max, min):
    n = 0
    for a in range(max, min, -1):
        for b in range(a, min, -1):
            x = a * b
            if x > n:
                s = str(a * b)
                if s == s[::-1]:
                    n = a * b
    print(n)

```

**#Q5 - 2520 is the smallest number that can be divided by each of the numbers from 1 to 10 without any remainder.What is the smallest positive number that is evenly divisible by all of the numbers from 1 to 20?**

```python

def smallest_div_1_to_20():
    for i in range(2520,999999999,2520):
        if all(i % n == 0 for n in range(11,21)):
            return i

```

**#Q6 - The sum of the squares of the first ten natural numbers is, 1^2 + 2^2 + ... + 10^2 = 385
The square of the sum of the first ten natural numbers is, (1 + 2 + ... + 10)^2 = 55^2 = 3025
The difference between the sum of the squares of the first ten natural numbers and the square of the sum is 3025 - 385 = 2640.
Find the difference between the sum of the squares of the first one hundred natural numbers and the square of the sum.**

```python

def diff_of_sum_of_squares(n):
    sq = []
    sq_of_sum = []
    for i in range(1,n+1):
        sq.append(i**2)
        sq_of_sum.append(i)
    return ((sum(sq_of_sum)**2) - sum(sq))

```
