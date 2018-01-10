# Data Types in Javascript

## Javascript - A dynamically typed language

Javascript is what you would call a *dynamically typed language*. What that means is a variable in Javascript can hold any type of value. To draw some context, in other statically typed languages like C, C++ or Java, you are required to specify what *type* of value a variable you are creating can hold.

In C, if you want to create a variable,

```C
int a = 10;

a = 20; // This operation is allowed since 20 is a integer too.
a = 'Hello World!' // This operation will throw an error, since it's a string
```

In Javascript, there is no such requirement. The *let* keyword can be used to hold any type of value.

```javascript
let a = 10;
let b = 10.5;
let c = "Hola Amigo!";

// All valid operations! 🎉
```

## Data Types

While variables in Javascript don't have types, the values that you store in them do. What that means is the a value stored in a variable can be of the following types:

- number (A numeric value like 10 or 5.5)
- boolean (A conditional value like true or false)
- string (A character or string value like "Hey")
- object (An aggregate value of properties and values)
- undefined (An undefined value)

## The typeof operator

Javascript has a handy `typeof` operator that tells you what the type of value stored in a variable is.

```javascript
let a = 10;

console.log(typeof a); // this will print number to the console
```

### Test your skills 🧠

What do you think will be the output of the following?

*Think of the answer before executing it yourself, execute it and see if you got it right! Questions marked with a* 🚀 *are slightly tricky.*

1) 

```javascript
let a = 10;

console.log(typeof a);

let a = 'Hello World';

console.log(typeof a);

let a = 4.5;

console.log(typeof a);
```


2)

```javascript
let a;

console.log(typeof a);
```

3) 🚀

```javascript
let a;

console.log(typeof (typeof a));
```