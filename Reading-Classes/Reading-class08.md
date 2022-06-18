## Create a List Using Loops and List Comprehension in Python
To better illustrate how a list comprehension can be used to write more efficient Python code,
 we’ll take a look at a side by side comparison. 

In the following example, you’ll see two different techniques for creating a Python list. 
The first is a for loop. We’ll use it to construct a list of the powers of two.

Example 1: Comparing list creation methods in Python

First, create a list and loop through it. Add an expression, in this example, we’ll raise x to the power of 2.

     create a list using a for loop
     squares = []

     for x in range(10):
     # raise x to the power of 2
     squares.append(x**2)
     print(squares)

     Output:
        [0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

The same thing can be done using a list comprehension, but with a fraction of the code. 
Let’s take a look at how to create a list of squares using the list comprehension method.

     create a list using list comprehension
     squares = [x**2 for x in range(10)]
     print(squares)

Even in this basic example, it’s obvious that list comprehensions reduce the code necessary to complete rather 
complicated task when working with a list.

## Multiplying Parts of a List
What if we wanted to multiply every number in a list by three in Python?
We could write a for loop and store the results in a new list, or we could use list comprehensions.

Example 2: Multiplication with list comprehensions
       
    create a list with list comprehensions
    multiples_of_three = [ x*3 for x in range(10) ]
    print(multiples_of_three)
     
    Output:
      [0, 3, 6, 9, 12, 15, 18, 21, 24, 27]

By taking advantage of list comprehensions, it’s possible to work on only part of a list. For instance, 
if you only wanted the even numbers in a given range, you could find them using a filter.

Adding a filter to the list comprehension allows for greater flexibility. By using filters, 
we can select certain items from the list, while excluding others. This is an advanced feature of lists in Python.

    even_numbers = [ x for x in range(1,20) if x % 2 == 0]
     Output:
        [2, 4, 6, 8, 10, 12, 14, 16, 18]


## Simple Decorators
Now that you’ve seen that functions are just like any other object in Python, you’re ready to move on and see the magical beast that is the Python decorator. Let’s start with an example:

    def my_decorator(func):
       def wrapper():
          print("Something is happening before the function is called.")
          func()
          print("Something is happening after the function is called.")
       return wrapper

    def say_whee():
    print("Whee!")

    say_whee = my_decorator(say_whee)
Can you guess what happens when you call say_whee()? Try it:
      
     Output :
     say_whee()
     Something is happening before the function is called.
     Whee!
     Something is happening after the function is called.

To understand what’s going on here, look back at the previous examples.
We are literally just applying everything you have learned so far.

The so-called decoration happens at the following line:

      say_whee = my_decorator(say_whee)

In effect, the name say_whee now points to the wrapper() inner function. Remember that you return wrapper as a function when you call my_decorator(say_whee):

> say_whee
<function my_decorator.<locals>.wrapper at 0x7f3c5dfd42f0>
However, wrapper() has a reference to the original say_whee() as func, and calls that function between the two calls to print().

Put simply: decorators wrap a function, modifying its behavior.

Before moving on, let’s have a look at a second example. Because wrapper() is a regular Python function, the way a decorator modifies a function can change dynamically. So as not to disturb your neighbors, the following example will only run the decorated code during the day:

from datetime import datetime

    def not_during_the_night(func):
       def wrapper():
          if 7 <= datetime.now().hour < 22:
              func()
          else:
              pass  # Hush, the neighbors are asleep
       return wrapper

     def say_whee():
      print("Whee!")

     say_whee = not_during_the_night(say_whee)

If you try to call say_whee() after bedtime, nothing will happen:

> say_whee()
