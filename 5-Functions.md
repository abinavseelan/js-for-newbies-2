# Functions

Functions help prevent code duplication.

## An Example

Say we have a set of variables and we want to add the value 2 to all of them and then print the value. We have the following variables

```javascript
let a = 10;
let b = 20;
let c = 30;
let d = 40;
let e = 50;
```
To get our expected output, we would need to do the following

```javascript
let a = 10;
console.log(a + 2);

let b = 20;
console.log(b + 2);

let c = 30;
console.log(c + 2);

let d = 40;
console.log(d + 2);

let e = 50;
console.log(e + 2);
```

Notice how we are copying over the same logic over and over again for each variable. This is called code duplication. Functions help us prevent this. A function is a snippet of code and logic, that can be called multiple times across the program you're writing.

And how do we create a function? We use the `function` keyword

```javascript
function someFunctionName() {
    // some code
}
```

A function has three main parts,

![Representation of a function](http://javascript.info/article/function-basics/function_basics@2x.png);

*Image source: javascript.info*

- function name: The function name help us reference this function across our program
- function parameters: These let us provide some data to the function (More on this in a bit)
- function body: This houses the logic that we want to execute everytime we call the function

Now, let's convert the logic we wrote to use a function. First we need to create a function. 

**Pro Tip** 💡: Make sure the function name is descriptive and helps explains what the function will do!

```javascript
function addAndPrint() {};
```

Then we copy over the logic

```javascript
function addAndPrint() {
    console.log(...); // Oh wait....how do I know what variable to add 2 to?
}
```

How *do* you let the function know what variable you want to add 2 to and print. That's where *function parameters* come in. You can specify the data you want to pass into the function by specifying the data in the `()`.

```javascript
function addAndPrint(someNumber) {
    console.log(someNumber + 2);
}
```

Now let's wire the variables `a`, `b`, `c`, `d` and `e`.

```javascript
function addAndPrint(someNumber) {
    console.log(someNumber + 2);
}

let a = 10;
addAndPrint(a);

let b = 20;
addAndPrint(b);

let c = 30;
addAndPrint(c);

let d = 40;
addAndPrint(d);

let e = 50;
addAndPrint(e);
```

The output will be

```bash
12
22
32
42
52
```

## Single source of truth

Functions are extremely useful since they create a single source of truth for logic. If your logic isn't working the way you want it, you know that all the logic is concentrated in one function rather than across your program in different places. Also, if the logic needs to be updated, we need to make the update in just *one* place!

Lets see this in action. In the above example, we're adding 2 to all the numbers. But what if we want to dynamically change the value? One way we can programmatically control the number being added to the variable is by passing in another parameter.

Right now we have this

```javascript
function addAndPrint(someNumber) {
    console.log(someNumber + 2);
}
```

We can take the value to be added as the *second* parameter

```javascript
function addAndPrint(someNumber, numberToAdd) {
    console.log(someNumber + numberToAdd);
}
```

And that's about it! Now lets wire in the variables. Now we can provide any value to add the variable, by passing in the value as the second parameter.

```javascript
function addAndPrint(someNumber, numberToAdd) {
    console.log(someNumber + numberToAdd);
}

let a = 10;
addAndPrint(a, 2); // This will print 12

let b = 20;
addAndPrint(b, 5); // This will print 25

let c = 30;
addAndPrint(c, 3); // This will print 33

let d = 40;
addAndPrint(d, 4); // This will print 44

let e = 50;
addAndPrint(e, 10); // This will print 60
```

## Variables in Functions

Functions can have their own *local* variables. Variables can be declared inside a function block. The reason thses variables are called *local* variables is because the variables can only be accessed by code *inside* the function block and not outside. This is related to something called Function Scope. This is out of the scope (heh. pun intended 😛) of this session. It should be covered in a future session!

```javascript
function someFunction() {
    let a = 10;

    console.log(a); // This will print 10. `a` is accessible here.
}

console.log(a); // This will tell you that `a` is not defined.
```

**Pro Tip** 💡: Function parameters are local variables too!

Variables declared outside the function block are actually accessible by code *inside* the function block. These variable, from the functions perspective are called *outer variables*.

```javascript
let a = 10;

function someFunction() {
    console.log(a); // `a` is accessible inside the function as an outer variable
}
```

However, if you declare a variable of the same name inside the function block, the *local* variable takes precedence over the *outer* variable.

```javascript
let a = 10;

function someFunction() {
    let a = 20;
    console.log(a); // This will print 20
}

console.log(a); // This will print 10
```

## Returning a value

In addition to just executing code, functions can also *return* a value to the function caller. Taking the previous example, instead of just printing out the addition `console.log(someNumber + numberToAdd);`, say we want the function to perform the operation and give us the result. Here we would need to *return* the value of `someNumber + numberToAdd`. We can do this by using the `return` keyword.

```javascript
function addNumber(someNumber, numberToAdd) {
     return someNumber + numberToAdd;
}
let answer;

let a = 10;
answer = addNumber(a, 2);
console.log(answer); // This will print 12 to the console

let b = 20;
answer = addNumber(b, 5);
console.log(answer); // This will print 25 to the console

let c = 30;
answer = addNumber(c, 3);
console.log(answer); // This will print 33 to the console

let d = 40;
answer = addNumber(d, 4);
console.log(answer); // This will print 44 to the console

let e = 50;
answer = addNumber(e, 10); // This will print 60 to the console
console.log(answer);
```

Here when we call `addNumber(x, y)`, we perform `x + y` but then return the value. But where will the returned value go? That's why we needed the `answer` variable. When we execute `answer = addNumber(x, y);` the runtime first executes the function `addNumber` and the value is returned to `answer` to hold.

### 🧠 Test your skills!

*Think of the answer before executing it yourself, execute it and see if you got it right! Questions marked with a* 🚀 *are slightly tricky.*

1) What do you think is the output of the following? 🚀

```javascript
function functionWithTwoReturns() {
    return true;
    return false;
}

let answer = functionWithTwoReturns();

console.log(answer); // ?
```

2) Create a simple function that takes in a number and finds out if the number is a prime number of not. 🚀 For example, if I pass in the number 7, it should return `true` and if I pass in the number 8 it should return `false`.

## Functions are first class citizens

> Functions are first class citizens of Javascript

You'd find this term being thrown around a lot when going through Javascript material. Functions in Javascript are a little bit different from functions from other programming like C and C++ in the sense that you can use a function the same way you would use any other value in the language.

For example, functions can be stored in arrays

```javascript
let a = [function() {}, function() {}, function() {}];
```

and functions can be even be passed in as a parameter to other functions!

```javascript
function someFunction() {
    // some code
}

function someOtherFunction(f) {
    // do something else
    f();
};

someOtherFunction(someFunction);
```

Functions can also be assigned to variables. So instead of 

```javascript
function someFunction() {
    // do something
};

someFunction();
```

you can do this.

```javascript
let someFunction = function() {
    // do something
};

someFunction();
```

### Array.forEach()

To highlight a good usecase for functions as parameters, we can take up the `forEach` method that arrays have. The `forEach` method helps us iterate through an array without having to define a loop!

The `forEach` method takes a function as a parameter. The function is executed for each value in the array. The function takes two parameters, the value at a given index and the index itself. Lets see this in action shall we? 🤖

```javascript
let letters = ['a', 'b', 'c', 'd', 'e'];

letters.forEach(function(value, index) {
    console.log(`${value} ${index}`);
});
```

This will print out the following to the console

```bash
a 0
b 1
c 2
d 3
e 4
```

### 🧠 Test your skills!

*Think of the answer before executing it yourself, execute it and see if you got it right! Questions marked with a* 🚀 *are slightly tricky.*

1) Create a function `parentFunction` that takes in a function as a parameter and executes that function inside its function block. Execute `parentFunction` multiple times, but each time a different function should be passed into it. 🚀 (This is the core concept behind a Javascript pattern called callbacks!)

## Arrow functions

Arrow functions are another way to define functions. While they do defer from function defined with the `function` keyword in some ways, specifically with regard to the `this` keyword (But more on that in a later session, for the purpose of this session, we can just assume it to work the same way as functions defined with the `function` keyword, but with a slightly different syntax.

An arrow function would look like thiis

```javascript
let someFunction = () => {

}
```

The main differences in the syntax are:
- the `function` keyword has been dropped.
- there is a `=>` added to signify that this block is a function block

Arrow functions allow for syntax reduction. If you have a function with only parameter, you can ignore the `()` surrounding the parameter

```javascript
let someFunction = (firstParam) => {

};

// can be written as 

let someFunction = firstParam => {

};
```

If you have more than one parameter, the `()` are required.

Also, if your function has just one line in it's function block *and* that one line is a *return* statement, the `{}` are optional as well.

```javascript
let someFunction = firstParam => {
    return firstParam + 2;
}

// can be written as

let someFunction = firstParam => firstParam + 2;
```

You might be scratching your head asking yourself why is all this necessary. So did I the first time I saw them and used them. But trust me. Over time it'll grow on you. 😄
