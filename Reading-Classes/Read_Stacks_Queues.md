Data structures organize storage in computers so that we can efficiently access and change data. 
Stacks and Queues are some of the earliest data structures defined in computer science.

Simple to learn and easy to implement, their uses are common, and you'll most likely find yourself incorporating 
them in your software for various tasks.

It's common for Stacks and Queues to be implemented with an Array or Linked List. 
We'll be relying on the List data structure to accommodate both Stacks and Queues.

## How do they Work?
## Stack
Stacks, like the name suggests, follow the Last-in-First-Out (LIFO) principle. 
As if stacking coins one on top of the other, the last coin we put on the top is the one that is 
the first to be removed from the stack later.

To implement a stack, therefore, we need two simple operations:

- push - adds an element to the top of the stack:

![Adding an item to a stack](../../../Downloads/stacks-and-queues-in-python-1.jpg)

- pop - removes the element at the top of the stack:

![removing an item](../../../Downloads/stacks-and-queues-in-python-2.jpg)

## Queue
Queues, like the name suggests, follow the First-in-First-Out (FIFO) principle. 
As if waiting in a queue for the movie tickets, 
the first one to stand in line is the first one to buy a ticket and enjoy the movie.

To implement a queue, therefore, we need two simple operations:

- enqueue - adds an element to the end of the queue:

![enqueue](../../../Downloads/stacks-and-queues-in-python-3.jpg)

- dequeue - removes the element at the beginning of the queue:

![dequeue](../../../Downloads/stacks-and-queues-in-python-4.jpg)

## Stacks follow these concepts:

FILO

First In Last Out

This means that the first item added in the stack will be the last item popped out of the stack.

LIFO

Last In First Out

This means that the last item added to the stack will be the first item popped out of the stack.

Conclusion
Stacks and queues are simple data structures that allow us to store and retrieve data sequentially. 
In a stack, the last item we enter is the first to come out. In a queue, the first item we enter is the first come out.

We can add items to a stack using the push operation and retrieve items using the pop operation. 
With queues, we add items using the enqueue operation and retrieve items using the dequeue operation.

In Python, we can implement stacks and queues just by using the built-in List data structure. 
Python also has the deque library which can efficiently provide stack and queue operations in one object. 
Finally, we've made our stack and queue classes for tighter control of our data.

There are many real-world use cases for stacks and queues, understanding them allows us to solve many data storage problems in an easy and effective manner.