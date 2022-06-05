<h1>Files In Python</h1>

A file object is:

“an object exposing a file-oriented API (with methods such as read() or write()) to an underlying resource.” (Source)

There are three different categories of file objects:

-Text files

-Buffered binary files

-Raw binary files

Each of these file types are defined in the io module. 

## Opening and Closing a File in Python

If you want to work in a file, you need to open it first, so to open a file we use a build-in function called open().
this function takes one argument which is the path for the file that you want to open.

After you finish working with this file you have to make sure that you closed it.
You can use more than one method to close a file, one of them is by using try-finally block:

reader = open('dog_breeds.txt')

  try:

    Further file processing goes here
    
  finally:

    reader.close()
    
Another way to close a file is by using **with** statement:

with open('dog_breeds.txt') as reader:

    Further file processing goes here
    
with statement automatically takes care of closing the file once it leaves the with block, even in cases of error.


## The try and except Block: Handling Exceptions
The try and except block in Python is used to catch and handle exceptions.
Python executes code following the try statement as a “normal” part of the program.
The code that follows the except statement is the program’s response to any exceptions in the preceding try clause.

  try:

    linux_interaction()
    
  except:

    print('Linux function was not executed')
    
## The else Clause
In Python, using the else statement, you can instruct a program to execute 
a certain block of code only in the absence of exceptions.

 try:
 
    linux_interaction()
    
 except AssertionError as error:

    print(error)
    
 else:

    print('Executing the else clause.')



## Things I want to know more about:
1- I want to know more about Big O notation.

2- I want to know more about readlines method in reading files in Python because I’m still confused about it.
