# React js

## Default parameters
Functions can be initialized with default parameters, which will be used only if an argument is not invoked through the
function.

    var func = function (a, b) {
    b = b === undefined ? 2 : b
    return a + b
    }
ex1

    let func = (a, b = 2) => {
    return a + b
    }
ex2

    func(10) // returns 12
    func(10, 5) // returns 15

## Spread syntax
Spread syntax can be used to expand an array.

ES6

    let arr1 = [1, 2, 3]
    let arr2 = ['a', 'b', 'c']
    let arr3 = [...arr1, ...arr2]

    console.log(arr3) // [1, 2, 3, "a", "b", "c"]

Spread syntax can be used for function arguments.

ES6

    let arr1 = [1, 2, 3]
    let func = (a, b, c) => a + b + c

    console.log(func(...arr1)) // 6

## Destructuring (object matching)
Use curly brackets to assign properties of an object to their own variable.

    var obj = {a: 1, b: 2, c: 3}
ES5
    
    var a = obj.a
    var b = obj.b
    var c = obj.c
ES6

    let {a, b, c} = obj

## Array iteration (looping)
A more concise syntax has been introduced for iteration through arrays and other iterable objects.

    var arr = ['a', 'b', 'c']
ES5

    for (var i = 0; i < arr.length; i++) {
      console.log(arr[i])
    }
ES6
    
    for (let i of arr) {
      console.log(i)
    }


## Classes/constructor functions
Introducess the class syntax on top of the prototype-based constructor function.

ES5
    
    function Func(a, b) {
      this.a = a
      this.b = b
    }

    Func.prototype.getSum = function () {
      return this.a + this.b
    }

    var x = new Func(3, 4)
ES6
    
    class Func {
      constructor(a, b) {
        this.a = a
        this.b = b
      }
    
      getSum() {
        return this.a + this.b
      }
    }
    
    let x = new Func(3, 4)
    x.getSum() // returns 7
    
