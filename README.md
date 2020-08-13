# Project-Euler-answers-in-python
Hello folks, Are you a beginner in Python and trying to solve basic functions to improve your python knowledge and try testing yourself with Hackerrank or some other platforms to create a basic portfolio? then this repo might help you in right sense.

Questions taken from Project Euler Archives and addressed the piece of codes in Python.


**#Q1 - If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23. Find the sum of all the multiples of 3 or 5 below 1000.**

```python
def sum_of_multiples_of_3_or_5(max_limit):
    a = 0
    for i in range(1,max_limit):
        if i%3 or i%5:
            a += i
    print("Sum of multiples of 3/5 till {} is {}".format(max_limit,a))
```

