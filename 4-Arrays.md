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

### Array length

Any variable that is holding an array has a `.length` property associated with it. This will tell you how *long* the array is.

```javascript
let fruits = ['apple', 'orange', 'banana', 'grapes', 'mango'];

console.log(fruits.length); // This will print 5 to the console.
```

### Adding values to an Array

Values can be directly assigned to an index. If you add a value after the last index of the array, the array length is automatically increased.

```javascript
let fruits = ['apple', 'orange', 'banana', 'grapes', 'mango'];

console.log(fruits.length); // This will print 5 to the console

fruits[5] = 'tomato';
console.log(fruits); // ['apple', 'orange', 'banana', 'grapes', 'mango', 'tomato'] to the console

// PS - 🍅 is a fruit!

console.log(fruits.length); // This will print 6 to the console
```

### Modifying values in an array

Existing values in the array can also be directly accessed and modified,

```javascript
let fruits = ['apple', 'orange', 'banana', 'grapes', 'mango'];

fruits[1] = 'pineapple';

console.log(fruits); // This will print 'pineapple' to the console.
```

![Reference anyone?](https://media.giphy.com/media/11FQncIaxjSGmA/giphy.gif)

### Nested arrays

Since arrays in Javascript can hold any value, they can also hold other arrays!

```javascript
let arr = [];

arr[1] = [1, 2, 3];
arr[2] = [4, 5, 6];
arr[3] = [7, 8, 9];

console.log(arr); // This will print [[1, 2, 3], [4, 5, 6], [7, 8, 9]] to the console
```

These are called nested arrays. To access values *inside* nested arrays, you need to first get the index of the nested array, and then the index of the value inside the nested array.
If we want to get the value *6* from the above nested arrays,

```javascript
let arr = [];

arr[1] = [1, 2, 3];
arr[2] = [4, 5, 6];
arr[3] = [7, 8, 9];

console.log(arr[1]); // This will print [4, 5, 6] to the console

console.log(arr[1][2]); // This will print 6 to the console
```

Pro Tip 💡: Sometimes you would want to insert a value to the end of the array but you don't know what the last index is. Here you can use the `array.length` data to figure this out!

```javascript
let arr = [1, 2, 3, 4, 5];

console.log(arr.length); // This will print 5

// Since array indices start from 0, (arr.length - 1) is the last used index
// So ...
arr[arr.length] = 6; 
```

### 🧠 Test your skills!

*Think of the answer before executing it yourself, execute it and see if you got it right! Questions marked with a* 🚀 *are slightly tricky.*

1) Create a triple nested array! That is, an array that contains arrays, that contains arrays. Give it a try! 😄

2) What happens here. 🚀

```javascript
let a = [1, 2, 3, 4, 5];

console.log(a.length);

a[100] = 6;

console.log(a.length);
```

## Iteration

Arrays and loops generally go hand-in-hand. Let's say we want to print out all the values in the array, or want to do some operations with each value in the array. We can combine loops and arrays to perform something called *iteration*.

Remember `for()` loops from the previous session? We know that arrays start from index `0` and we know that last index of the array is `array.length - 1`. We can use the `for()` loop syntax to our advantage to easily iterate through the array!

For example, the following snippet is for printing each value of the array,

```javascript
let arr = [1, 2, 3, 4, 5] ;

for(let i = 0; i < arr.length; i++) {
    console.log(arr[i]); // We can directly use `i` here since i would go 0, then 1, then 2 and so on till 4
}
```

### 🧠 Test your skills!

*Think of the answer before executing it yourself, execute it and see if you got it right! Questions marked with a* 🚀 *are slightly tricky.*

1) Create an array of names. Iterate over the array of names and print "Hi, My name is \<name\>" for each name in the array.

2) Create an array and print each value in the array. But here's the twist. The values need to be printed backward. For example, if my array is [1, 2, 3, 4, 5], the console should be `5 4 3 2 1`. 🚀


**Pro Tip** 💡: Continue and break

`continue` and `break` are keywords associated with loops. `continue` will immediately set the next iteration into action, while `break` will stop the iteration altogether.

### continue

Say we need to iterate through an array of numbers. In each iteration, the number should be printed to the console. However, if the number is divisible by 7, we don't want to print it to the console. Here, we need to use `continue`.

```javascript
let numbers = [1, 4, 7, 29, 49];

for (let i = 0; i < numbers.length; i++) {
    if (numbers[i] % 7 === 0) {
        continue; // This will stop the current iteration and immediately proceed with the next iteration
    }

    console.log(numbers[i]);
}
```

This will print out `1 4 29` to the console. 

### break

To understand `break`, say we need to iterate through an array of names, and print each name to the console. But on the first occurence of the name 'Hodor', we want to stop the execution of the loop and continue on with the rest of the code.

```javascript
let names = ['Jon', 'Bran', 'Hodor', 'Cercei', 'Jamie'];

for (let i = 0; i < names.length; i++) {
    if (names[i] === 'Hodor') {
        break;
    }

    console.log(names[i]);
}

console.log('The loop has ended'); // This is after the loop
```

The output of this snippet would be

```bash
Jon
Bran
The Loop has ended
```

The moment `break` is called, the loop stops execution and continues execution after the loop.

## Array Methods

Arrays have access to some helpful methods. A few easy to understand, but helpful ones, are:

- `push`
- `pop`
- `shift`
- `unshift`

### `push` and `pop`

The `push()` method lets you insert a value to the end of the array. You need not worry about indices.

```javascript
let a = [1, 2, 3, 4, 5];

console.log(a); // This will print [1, 2, 3, 4, 5]

a.push(6);

console.log(a); // This will print [1, 2, 3, 4, 5, 6]

a.push('hello');

console.log(a); // This will print [1, 2, 3, 4, 5, 6, 'hello']
```

The `pop` method lets your remove a value from the end of the array.

```javascript
let a = [1, 2, 3, 4, 5];

a.pop();

console.log(a); // This will print [1, 2, 3, 4]

a.pop();

console.log(a); // This will print [1, 2, 3]
```

### `shift` and `unshift`

`unshift` and `shift` do the same thing as `push` and `pop` respectively, except with the front of the array,

`unshift` will insert a value to start of the array.

```javascript
let a = [1, 2, 3, 4, 5];

a.unshift(6);

console.log(a); // This will print [6, 1, 2, 3, 4, 5]
```

`shift` will remove a value from the start of the array

```javascript
let a = [1, 2, 3, 4, 5];

a.shift();

console.log(a); // This will print [2, 3, 4, 5]

a.shift();

console.log(a); // This will print [3, 4, 5]
```

### 🧠 Test your skills!

*Think of the answer before executing it yourself, execute it and see if you got it right! Questions marked with a* 🚀 *are slightly tricky.*

1) Try to emulate a queue using arrays and array methods. A queue is a data structure that allows inserts from the end but removals happen from the front. This is called a FIFO (**F**irst **I**n **F**irst **O**ut) approach. 🚀

2) Try to emulate a stack using arrays and array methods. A stack is a data structure that allows inserts from the end and removals from the end. This is called a LIFO (**L**ast **I**n **F**irst **O**ut) approach. 🚀