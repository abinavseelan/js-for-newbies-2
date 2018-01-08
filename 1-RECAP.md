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

```javascript
let a = 10;

console.log(a); // This will print the value 10 to the console
```