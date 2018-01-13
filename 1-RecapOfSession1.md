# A quick recap of Session 1

Session 1 of *JS for Newbies* was taken by [Ashish Singh](https://github.com/ashish1729) on 7th January, 2018. The entire webinar has been recorded and can be [found here](https://www.youtube.com/watch?v=aljqhsGXgkk). The talk has a companion repository as well, which can be found [here](https://github.com/ashish1729/jsForNewbies-talk-1). I strongly urge you to go through the content there as well if you haven't already. 😄

I'll be doing a quick recap of the topics covered in the previous session that are  important to this session.

## What is Javascript?

Javascript is a programming language built for the web. It was initially designed for providing interactivity to static HTML-CSS websites. But over the course of its existence, Javascript has matured into a versatile programming language that has use-cases far beyond the interactivity that it was first designed for!

## Where can I run Javascript?

Javascript can be natively run inside your browser like Chrome, Firefox or Safari. Just fire up your developer console and you immediately have access to a "command line interface" where you can execute Javascript.

### Developer console in Chrome

![getting to the developer console in chrome](https://user-images.githubusercontent.com/6417910/34688300-a720488a-f4d7-11e7-8ffe-3c736d854ae0.png)

## Comments

As a developer, there will sometimes be a need to document what your code does *within* the code itself. This is where comments come in.

Comments can be **single lined comments**. For example, here I want to explain what I'm doing with the `console.log()` statements. Single line comments can be created by adding a `//` to your code.

```javascript
// Printing the avengers to the console
console.log('Iron Man');
console.log('Captain America');
console.log('Hulk');
console.log('Thor');
```

Comments can also span multiple lines. You can do this by adding a `/* */` to your code.

```javascript
/*
    This
    is
    a
    multi
    line
    comment
*/
```

**Pro Tip** 💡 - You can actually use comments to prevent a line of code from executing!

```javascript
console.log(1);
// console.log(2);
console.log(3);
```

Here, `console.log(2)` will not execute since it has been commented out and comments are ignored during execution!

## Variables

Remember algebra from school?

```js
x = 5

x + 10
```

Here we know that the value of `x + 10` is going to be 15 since the *variable* `x` holds the value 5.

Well... if you remember your 5th standard algebra well, then you've pretty much understood variables already! Similar to the way `x` holds 5 in the equation above, variables in programming languages can store some data that we can reference by just the variable name.

Varibles in JS can be created using the `let` keyword.

```javascript
let a = 10;

console.log(a); // This will print the value 10 to the console
```

Variables can be reassigned to other values.

```javascript
let a = 10;

console.log(a); // This will print the value 10 to the console

a = 20; // Re-assigning the variable

console.log(a); // This will print the value 20 to the console
```

## Constants

Constants function like variables. The only caveat is that once a value has been assigned to a constant, their **value** cannot be changed. Constants in JS can be created using the `const` keyword.

```javascript
const number = 10;

number = 20; // This line will throw an error!
```

<center>
<img
    style="width:80%; margin: 0 auto;"
    alt="javascript constants cannot be re-assigned" src="https://user-images.githubusercontent.com/6417910/34706559-9158c5fc-f52e-11e7-9a0e-ef162c485505.png" />
</center>

## Operators

Programming revolves around *solving problems*. Problems, in most cases, involve taking data and computing results with them. JS, like most other programming languages, lets you compute results using operators.

Operators are of different kinds:

- Numeric operators
- Comparison
- Logical

### Numeric Operators

Numeric operators function like their mathematical counterparts.  
JS supports the following numeric operators:

|Operation|Operator      |Example  |
|:-------:|--------------|---------|
|`+`      |Addition      |`x + 10` |
|`-`      |Subtraction   |`20 - 15`|
|`*`      |Multiplication|`100 * y`|
|`/`      |Division      |`25 / x` |
|`%`      |Modulus       |`30 % 5` |

```javascript
let a = 10;
let b = 5;

console.log(a + b); // This will print 15 to the console
console.log(a - b); // This will print 5 to the console
console.log(a * b); // This will print 50 to the console
console.log(a / b); // This will print 2 to the console
```

The modulus operator, `%`, is something that you might not have seen before. In brief, the modulus operator performs a division operation but the result of the operation is the remainder, not the quotient.

```javascript
let a = 10;
let b = 5;
let c = 3;

console.log(a % b); // This will print 0 to the console since 10/5 has 0 remainder.
console.log(a % c); // This will print 1 to the console since 10/3 has a 1 remainder.
```

### Comparison Operators

Sometimes you would want to compare data, and this is where comparison operators come in.

The following are the supported comparison operators:

|Operation|Operator      |
|:-------:|--------------|
|`>`      |Greater than|
|`<`      |Less than|
|`>=`     |Greater than or equal to|
|`<=`     |Less than or equal to|
|`==`     |Equal to|
|`!=`     |Not equal to|
|`===`    |*Strictly* equal to|
|`!==`    |*Strictly* not equal to|

```javascript
console.log(10 > 5); // This will print true
console.log(5 > 10); // This will print false

console.log(10 < 5); // This will print false
console.log(5 < 10); // This will print true

console.log(10 >= 5); // This will print true
console.log(5 >= 10); // This will print false
console.log(10 >= 10); // This will print true

console.log(10 <= 5); // This will print false
console.log(5 <= 10); // This will print true
console.log(5 <= 5); // This will print true

console.log(10 == 10); // This will print true
console.log(5 == 10); // This will print false

console.log(10 != 10); // This will print false
console.log(5 != 10); // This will print true
```

What is the difference between equal-to and strictly-equal-to, you ask? 🤔

The `==` operator checks only the value being equated, while `===` checks both the value and the data types on either side of the operator (more on data types in Session 2).

```javascript
console.log(5 == '5'); // This will print true
console.log(5 === '5'); // This will print false since the LHS is a number and the RHS is a string
```

Comparison operators are extremely useful while working with control flows like loops and conditional statments.

### Logical operators

Sometimes you want to evaluate conditions.

For example, "The Indian cricket team can make it to the next round if they win this match **and** South Africa loses their match" means that India would progress to the next round only if *both* conditions were satisfied.

Similarly, "For lunch I'll have either Chinese or Italian" means that you'd be happy if *either* condition was satisfied, and would be unhappy only if *neither* was satisfied.

Javascript supports the following logical operators:

- `&&` - The logical `and` operator, which evaluates to `true` only if both LHS and RHS are true. Otherwise it evaluates to `false`
- `||` - The logical `or` operator, which evaluates to `true` if either LHS or RHS is true, or both are true. If both are false it evaluates to `false`

```javascript
console.log(true && true); // This will print true to the console
console.log(false && true); // This will print false to the console
console.log(true && false); // This will print false to the console
console.log(false && false); // This will print false to the console

console.log(true || true); // This will print true to the console
console.log(false || true); // This will print true to the console
console.log(true || false); // This will print true to the console
console.log(false || false); // This will print false to the console
```

## Conditional Flow

Programming is all about decisions and decisions are made possible using conditional flow statements.

### if-else block

The `if-else` block gives our code two branches to continue execution with. The decision on which branch to choose is made based on the condition provided in the `if (<condition>)`.

```javascript
let animal = 'cat';

if (animal === 'cat') {
    console.log("It's a 🐈");
} else {
    console.log("It's a 🐕");
}

// What's the output going to be?
```

Here, since `animal === 'cat'` is true, the output is `'It's a 🐈!'`. However, if `animal` was anything other than `cat`, then the code that executes will be from the `else` block.

### if-(else if)-else

While `if-else` gives us a decision tree of two paths the code can take, what if we want to have multiple choices. Lets say that if the variable `animal` is a cat, then we print `Meow!` to the console, if it's a dog, we print `Woof!` to the console, if it's a fish, we print `Blub!` to the console and it's neither of these, we print `Not an animal!` to the console.

It's in cases like these that `if-(else if)-else` blocks come in handy!

```javascript
let animal = 'cat';

if (animal === 'cat') {
    console.log('Meow!');
} else if (animal === 'dog') {
    console.log('Woof!');
} else if (animal === 'fish') {
    console.log('Blub!');
} else {
    console.log('Not an animal!');
}
```

### Switch statements

While the above `if-(else-if)-else` block does the job, it isn't the prettiest thing to look at sometimes, especially if the number of *cases* increases. Javascript provides another conditional flow construct called `switch` which makes reading conditional flow a little bit better.

```javascript
let animal = 'cat';

switch(animal) {
    case 'cat': {
        console.log('Meow!');
        break;
    }

    case 'dog': {
        console.log('Woof!');
        break;
    }

    case 'fish': {
        console.log('Blub!');
        break;
    }

    default: {
        console.log('Not an animal!');
        break;
    }
}
```

There are a few things to point out here.

The variable passed into `switch()` is the variable being evaluated. Each `case` compares the values in the `case` to the variable provided. For example, `case 'cat'` will check if `animal` is equal to `'cat'`.

Each `case` block has a `break` statement in them. A `switch` block is evaluated top to bottom. Any time a `case` evalauates to `true`, the execution continues from there. A `break` statement is required to stop the execution and to *break* out of the switch block. Not adding a `break` at the end of a `case` will continue the execution to the next `case` as well.

Still confused? Try executing the above code without the `break` statements. 🙂

## Loops

Let's say I want to print the numbers 1 to 5. I could do it manually by

```javascript
console.log(1);
console.log(2);
console.log(3);
console.log(4);
console.log(5);
```

But this easily gets tedious once I want to print more numbers, till 100 for example. This is where loops come in.

### while()

The `while()` loop allows us to specify a way to repeat the execution of some code until a certain condition is met. The condition is specified inside the `while()` brackets.

Taking the same example as before,

```javascript
let number = 1;

while(number !== 5) {
    console.log(number);
    number = number + 1;
}
```

Here, we first send in `number = 1`, which is not equal to 5, so the block executes. We then increment number by 1 and retry the condition. *2* is still not equal to *5* so the block is executed again. This goes on until number is now 5. *5* is equal to *5*. Now the block stops repeating the execution continues after this block.

### for()

`for()` allows you to define the starting point, the end constraint and the increment for the loop in a single statement.

```javascript
for(let number = 1; number < 5; number = number + 1) {
    console.log(number);
}
```

The `for()` loop functions the same way the `while()` loop does, except that the all the looping data is specified in a single statement, thereby leaving the code inside the block pretty much independent of looping data.

### do-while()

This is a looping construct that is used less often when compared to the looping constructs mentioned above. To explain the difference between `while()` and `do-while()`, let us take an example.

```javascript
let number = 10;

while(number < 10) {
    // do something
}
```

In the above snippet the code inside the `while()` loop will never execute since the condition `number < 10` is false.

However, with a `do-while()` loop,

```javascript
let number = 10;

do {
    // do something
} while(number < 10);
```

Here the code inside the `do {}` block will execute **at least** once, since the evaluation of the constraint happens at the bottom. It's a funny construct but it does have its uses. 😎