## Classes and Objects
Objects are an encapsulation of variables and functions into a single entity. Objects get their variables and functions from classes. Classes are essentially a template to create your objects.

     class MyClass:
     variable = "blah"
     def function(self):
        print("This is a message inside the class.")
     myobjectx = MyClass()

## Accessing Object Variables
To access the variable inside of the newly created object "myobjectx" you would add the following:

    myobjectx.variable
So the output would by the string "blah"

## Accessing Object Functions
To access a function inside of an object you use notation similar to accessing a variable:

     myobjectx.function()

This would print out the message, "This is a message inside the class."

## init()
The _ _init_ _() function, is a special function that is called when the class is being initiated. It's used for asigning values in a class.


## Recursive Functions in Python
A recursive function is a function defined in terms of itself via self-referential expressions.

This means that the function will continue to call itself and repeat its behavior until some condition is met to return a result. All recursive functions share a common structure made up of two parts: base case and recursive case.

Behind the scenes, each recursive call adds a stack frame (containing its execution context) to the call stack until we reach the base case. Then, the stack begins to unwind as each call returns its results:

![recursive call](https://files.realpython.com/media/stack.9c4ba62929cf.gif)


## Recursive Data Structures in Python
A data structure is recursive if it can be deﬁned in terms of a smaller version of itself. A list is an example of a recursive data structure. 

- Starting with an empty list, you can generate any list by recursively applying the attach_head function
- Recursion can also be seen as self-referential function composition.

List is not the only recursive data structure. Other examples include set, tree, dictionary, etc.

Recursive data structures and recursive functions go together like bread and butter. The recursive function’s structure can often be modeled after the definition of the recursive data structure it takes as an input.