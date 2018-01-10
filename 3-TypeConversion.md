# Type Conversion

A variable's data type can be changed in Javascript in two ways:

- implicit type conversion, also known as coercion
- explicit type conversion, also known as type casting


## Implicit Type Conversion (Coercion)

Coercion is the programming paradigm of type conversion that happens implicitly, ie, automatically by the javascript runtime. Given that Javascript is a dynamically typed language, there may come times when variables of different types are put together in the same operation

For example,

```javascript
let a = 10;
let b = 'Hello World';

console.log(a + b); // This is a valid operation
```

In such a situation, what happens? 🤔 The output of the above snippet is `10Hello World`. Wait what?

The snippet is an example of coercion. What happened under the hood was that variable `a` was *coerced* from a *number* type to a *string* type and then the operation was performed, thereby catenating the two strings.

Similarly,

```javascript
let a = 20;
let b = "10";

console.log(a + b); // This will print 2010
console.log(a - b); // This will print 10
```

In `(a + b)`, the variable `a` is coerced to a value of type *string* and then `a` and `b` are catenated, resulting in `2010`. In `(a - b)`, the variable `b` is coerced to type *number* and then the equation is evalatued.

### 🧠 Test your skills!

*Think of the answer before executing it yourself, execute it and see if you got it right! Questions marked with a* 🚀 *are slightly tricky.*

What do you think will be the output of the following?

1)

```javascript
let a = "20";
let b = "10";

console.log(a + b);
console.log(a - b);
console.log(a * b);
console.log(a / b);
```

2)

```javascript
let a = "20";
let b = "40";

console.log(a > b);
console.log(a < b);
console.log(a > 10);
console.log(a < "10");
```

3) 🚀

```javascript
let a = "20";
let b = '';
let c = 0;
let d = -1;

console.log(a && true);
console.log(b && true);
console.log(c && true);
console.log(d && true);
```

## Explicit Type Conversion (Type Casting)

