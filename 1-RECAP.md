# A quick recap of Session 1

Session 1 of *JS for Newbies* was taken by [Ashish Singh](https://github.com/ashish1729) on 7th January, 2018. The entire webinar has been recorded and can be [found here](https://www.youtube.com/watch?v=aljqhsGXgkk)! The talk has a companion repository as well, which can be found [here](https://github.com/ashish1729/jsForNewbies-talk-1). I strongly urge you to go through the content there as well if you haven't already. 😄

## What is Javascript?

Javascript is a programming language built for the web. It was initially designed for providing interactivity to static HTML-CSS websites. But over the course of its existence, Javascript has matured into a versatile programming language that has use-cases far beyond the interactivity that it was first designed for!

## Where can I run Javascript?

Javascript can be natively run inside your browser like Chrome, Firefox or Safari. Just fire up your developer console and you immediately have access to a "command line interface" where you can execute Javascript.

### Developer console in Chrome

![screen shot 2018-01-09 at 12 53 59 am](https://user-images.githubusercontent.com/6417910/34688300-a720488a-f4d7-11e7-8ffe-3c736d854ae0.png)

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

Here, `console.log(2)` will not execute since it has been commented and comments are ignore during execution!

## Variables

Remember algebra from school? 

```
x = 5

x + 10
```

Here we know that the value of `x + 10` is going to be 15 since the *variable* `x` holds the value 5.

Well...if you remember your 5th standard algebra well, then you've pretty much understood variables already! Similar to the way `x` holds 5 in the equation above, variables in programming languages can store some data that we can reference by just the variable name.

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

Constants function like variables. The only caveat is that once a value has been assigned to a constant, the value cannot be changed. Constants in JS can be created using the `const` keyword.

```javascript
const number = 10;


number = 20; // This line will throw an error!
```

<img width="434" alt="screen shot 2018-01-09 at 11 16 09 am" src="https://user-images.githubusercontent.com/6417910/34706559-9158c5fc-f52e-11e7-9a0e-ef162c485505.png">

## Operators

Programming revolves around solving problems and problems, in most cases, involve taking data and computing results with them. JS, like most other programming languages, lets you compute results using operators.

Operators are of different kinds:

- Numeric operators
- Comparison
- Logical

### Numeric Operators

Numeric operators function like their mathematical counterparts. JS supports the following numeric operators

- `+` - Addition
- `-` - Subtraction
- `*` - Multiplication
- `/` - Division
- `%` - Modulus

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

Sometimes you would want to compare data, and this is where comparison operators come in

The following are the supported comparison operators:

- `>` - Greater than
- `<` - Less than
- `>=` - Greater than or equal to
- `<=` - Less than or equal to
- `==` - Equal to
- `!=` - Not equal to
- `===` - Strictly equal to
- `!==` - Strictly not equal to

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

What is the difference between equal-to and strictly-equal-to? 🤔

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

