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
- undefined (An undefined value)
- object (An aggregate value of properties and values)

### number

A value of type `number` is any numeric value. There is not distinction in Javascript between integers and floating point numbers as in other languages. Whether the value is `5` or `5.5`, both are deemed to be of type `number`.

```javascript
let a = 10; // Value is of type number
a = 4.5; // Value is still of type number
```

### boolean

A value of type `boolean` can either be `true` or `false`. Boolean values are also called the logical type since its primary use is for logical operations. A boolean value is usually the outcome of a comparison operation.

```javascript
let yes = true;
let no = false;

let answer = 4 > 5;

console.log(answer); // This will print false to the console.

answer = 5 > 4;

console.log(answer); // This will print true to the console.
```

### string

A value of type `string` is any character or string value. There are three ways you can denote a string value

- Using single quotes, `'Hi 👋'`
- Using double quotes, `"Hi 👋"`
- Using backticks, <code>\`Hi 👋\`</code>

```javascript
let first = 'Charmander';
let second = "Charmeleon";
let third = `Charizard`;

// All valid values of type string
```

**Pro Tip** 💡: While there is no difference between single and double quotes, backticks help you create something called string literals.

Lets say we need to print the first name (stored in a variable called `firstName`) and the last name (stored in a variable called `lastName`) as a single name. To catenate two strings, we can use the `+` operator.

```javascript
let firstName = 'Tony';
let lastName = 'Stark';

console.log('My name is ' + firstname + ' ' + lastName); // This will print 'My name is Tony Stark' to the console.
```

However, with string literals, we can directly replace the variables inside the string!

```javascript
let firstName = 'Tony';
let lastName = 'Stark';

console.log(`My name is ${firstName} ${lastName}`); // This will print 'My name is Tony Stark' as well!
```

### undefined

*undefined* is a rather funny value type. It denotes that the variable has not yet been assigned a value. If a variable is defined but not given a value, then it's value is automatically `undefined`.

```javascript
let a;

console.log(a); // This will print undefined to the console

a = 10; // Assigning a value to a

console.log(a); // a is not longer undefined
```

### Objects

Objects, objects ... objects? We'll cover this in the next section shall we? There's a lot to talk about here. 🤓

## The typeof operator

Javascript has a handy `typeof` operator that tells you what the type of value stored in a variable is.

```javascript
let a = 10;

console.log(typeof a); // this will print number to the console
```

### 🧠 Test your skills!

*Think of the answer before executing it yourself, execute it and see if you got it right! Questions marked with a* 🚀 *are slightly tricky.*

What do you think will be the output of the following?

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