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
let b = '10';

console.log(a + b); // This will print 2010
console.log(a - b); // This will print 10
```

In `(a + b)`, the variable `a` is coerced to a value of type *string* and then `a` and `b` are catenated, resulting in `2010`. In `(a - b)`, the variable `b` is coerced to type *number* and then the equation is evalatued.

### 🕵 Test your skills!

*Think of the answer before executing it yourself, execute it and see if you got it right! Questions marked with a* 🚀 *are slightly tricky.*

What do you think will be the output of the following?

1)

```javascript
let a = '20';
let b = '10';

console.log(a + b);
console.log(a - b);
console.log(a * b);
console.log(a / b);
```

2)

```javascript
let a = '20';
let b = '40';

console.log(a > b);
console.log(a < b);
console.log(a > 10);
console.log(a < '10');
```

3) 🚀

```javascript
let a = '20';
let b = '';
let c = 0;
let d = -1;

console.log(a && true);
console.log(b && true);
console.log(c && true);
console.log(d && true);
```

4) 🚀

```javascript
console.log(10 + '1' - 1 * 7);
```

## Explicit Type Conversion (Type Casting)

Javascript gives us control over type conversion as well. We can use `String(<variable>)` to convert a given variable to type *string*. `Number(<variable>)` can be used to the convert the variable to type *number*. `Boolean(<variable>)` can be used to convert a variable to a *boolean* value.

```javascript
let a = 10;

console.log(String(a)); // This will print "10" to the console
console.log(typeof String(a)); // This will print "string" to the console
```

```javascript
let a = '10';

console.log(Number(a)); // This will print 10 to the console
console.log(typeof Number(a)); // This will print "number" to the console
```

```javascript
let a = '';
let b = 0;
let c = 10;

console.log(Boolean(a)); // This will print false to the console
console.log(typeof Boolean(a)); // This will print "boolean" to the console

console.log(Boolean(b)); // This will print false to the console
console.log(Boolean(c)); // This will print true to the console
```

### 🕵 Test your skills!

*Think of the answer before executing it yourself, execute it and see if you got it right! Questions marked with a* 🚀 *are slightly tricky.*

What do you think will be the output of the following?

1)

```javascript
let a = -1;

console.log(String(a));
console.log(Number(a));
console.log(Boolean(a));

console.log(Boolean(a + 1));
```

## NaN

While converting other value types (both implictly and explicitly) to type *number*, there is chance that you might be performing an operation that does not make sense.

For example,

```javascript
let a = 'Hello World';

console.log(Number(a));
```

How do you convert the string *Hello World* to an integer or a floating point number? 🤔

The result of the above snippet is `NaN`, or "**N**ot **a** **N**umber".

The above snippet is a type cast. The same thing would happen with coercion as well

```javascript
console.log('Hello World' * 3);
```