## How to use the Random Module in Python
## When to use it?
We want the computer to pick a random number in a given range Pick a random element from a list, pick a random card from a deck, flip a coin etc. When making your password database more secure or powering a random page feature of your website.

## Random functions
The Random module contains some very useful functions.

## Randint
If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number. Generate integers between 1,5. The first value should be less than the second.

    import random

    print random.randint(0, 7)
This will output either 1, 2, 3, 4, 5, 6 or 7.

## Random
If you want a larger number, you can multiply it.

For example, a random number between 0 and 200:

     import random
     random.random() * 200


## Choice
Generate a random value from the sequence sequence.

    random.choice( ['red', 'black', 'green'] ).
The choice function can often be used for choosing a random element from a list.

    import random
    myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
    random.choice(myList)

## Shuffle

The shuffle function, shuffles the elements in list in place, so they are in a random order.

     from random import shuffle
     x = [[i] for i in range(10)]
     shuffle(x)
     Output:
     print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]] 


## Randrange
Generate a randomly selected element from range(start, stop, step)

    random.randrange(start, stop[, step])
    import random
    for i in range(3):
    print random.randrange(0, 101, 5)

    import random
    import itertools

     outcomes = { 'heads':0,
             'tails':0,
             }
     sides = outcomes.keys()

    for i in range(10000):
    outcomes[ random.choice(sides) ] += 1

     print 'Heads:', outcomes['heads']
     print 'Tails:', outcomes['tails']

There are only two outcomes allowed, so rather than use numbers and convert them, the words “heads” and “tails” are used with choice().