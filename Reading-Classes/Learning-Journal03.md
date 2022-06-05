Today lecture didn't add much from what I read from the reading task about how to open a file and how to write in it using 

    open("The path for the file"arg) 

In the arg here you can put what you want to do when you open that file for example "r" for reading and "w", you can add "b" for binary to become "rb" and "wb"

and I need to make sure to close the file by using **try-finally block** or **with statement**

    with open('dog_breeds.txt') as reader:
    Further file processing goes here
with statement will automaticlly close the file for me.

    try:
     Further file processing goes  here
    finally:
     reader.close()

when using finally here will be executed anyway so when you put 

     readed.close()

this will close the file for you even if try was not executed and there was exception.


## How to catch an error :
by using try-except block , you can put your code in try the except will catch the error for you . 

actually it is similler to try-catch block in JavaScript.


>Yes, it is my responsibility to find answers to my questions, but also that means the lecture should give me the basics or even more so I can understand and know where and how to start by myself. It is waste of time if I take a 5-hour lecture and then I have to search for everything and not have any information more than what I read in the reading task and not have professional assistance from the instructor at least during the lecture.