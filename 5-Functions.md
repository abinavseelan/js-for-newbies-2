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

### Single source of truth

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