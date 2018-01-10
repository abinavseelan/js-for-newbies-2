# Arrays

An *Array* is an ordered list of values.

## An Example

Let's say we want to have fruits in our program. A way to do this would be

```javascript
let fruit1 = 'apple';
let fruit2 = 'orange';
let fruit3 = 'banana';
let fruit4 = 'grapes';
let fruit5 = 'mango';
```

While this *is* one way to do it...it does get tedious to manage all the different variables once we have, say, a 100 fruits. And this is where Arrays come in. An Array is a ordered collection of values.

## Creating an array

So...how do we create an array?

```javascript
let arr = [];
```

That's pretty much it! Now let's convert the above snippet of fruits to use an array!

```javascript
let fruits = ['apple', 'orange', 'banana', 'grapes', 'mango'];
```

Ah! That's much cleaner. All the values we want to store and semantically stored in an array called `fruits`. But...how do we access the values stored in the array? 🤔

> An Array is an ordered list of values.

Array elements are numbered starting from 0. This is called an Array index. We can access any value in the array using the index - `array[<index>]`. To get the value 'orange' for example,

```javascript
let fruits = ['apple', 'orange', 'banana', 'grapes', 'mango'];

console.log(fruits[1]); // This will print 'orange' to the console.
```

and similarly to get the value 'mango'

```javascript
let fruits = ['apple', 'orange', 'banana', 'grapes', 'mango'];

console.log(fruits[4]); // This will print 'mango' to the console.
```

## Arrays in Javascript

Similar to how variables are dynamically typed in Javascript, arrays in Javascript, in contrast to other statically typed languages like C and C++, can hold **any** value in the same array!

```javascript
let list = ['Hey!', 2, true, undefined]; // A perfectly valid array.
```

Any variable that is holding an array has a `.length` property associated with it. This will tell you how *long* the array is.

```javascript
let fruits = ['apple', 'orange', 'banana', 'grapes', 'mango'];

console.log(fruits.length); // This will print 5 to the console.
```

Values can be directly assigned to an index. If you add a value after the last index of the array, the array length is automatically increased.

```javascript
let fruits = ['apple', 'orange', 'banana', 'grapes', 'mango'];

console.log(fruits.length); // This will print 5 to the console

fruits[5] = 'tomato';
console.log(fruits); // ['apple', 'orange', 'banana', 'grapes', 'mango', 'tomato'] to the console

// PS - 🍅 is a fruit!

console.log(fruits.length); // This will print 6 to the console
```

Existing values in the array can also be directly accessed and modified,

```javascript
let fruits = ['apple', 'orange', 'banana', 'grapes', 'mango'];

fruits[1] = 'green apple';

console.log(fruits); // This will print 'green apple' to the console.
```