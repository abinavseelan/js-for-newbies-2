# Objects

An Object is an encapsulation of other data types. You can think of Objects as programmatic models of real-world entities.

## An Example

Say we want to describe a human in our program. A human has a name, an age and their preferred food choice. Using just variables, we would need to do something like this.

```javascript
let humanName = 'Tony Stark';
let humanAge = 40; // probably?
let humanFoodPreference = 'Shawarma';

let humanIsAnAvenger = true;
```

This does not scale well. The human here has just 4 properties. What if he/she has more? How can we semantically handle this?

And this...is where objects come in. An object is an encapsulation of data. Since we're defining properties for a human, a *human* can be an object that encapsulated properties (of other primitive data types) inside it, so that the data is semantically aggregated.

To create an object, we use the `{}` brackets.

```javascript
let human = {};
```

Properites for the *human* are specified within the `{}` brackets.

```javascript
let human = {
    name: 'Tony Stark',
    age: 40,
    foodPreference: 'Shawarma',
    isAnAvenger: true
};
```

Properties are stored as *key-value* pairs. In the above snippet, the keys would be *name*, *age*, *foodPreference* and *isAnAvenger*. A *key* can hold any value type, even arrays, functions and objects!

```javascript
let human = {
    name: 'Tony Stark',
    age: 40,
    foodPreference: 'Shawarma',
    isAnAvenger: true,
    friends: ['Thor', 'Hawkeye', 'Steve Rogers', 'Bruce Banner'], // Array
    says: function() { // Function
        console.log("I'm Iron Man");
    },
    girlfriend: { // Another object
        name: 'Pepper Potts',
        age: 30,
        isAnAvenger: false
    }
};
```

Objects use the `.` notation to access values stored in *keys*. For example, to access the `foodPreference* of this *human*.

```javascript
let human = {
    name: 'Tony Stark',
    age: 40,
    foodPreference: 'Shawarma',
    isAnAvenger: true
};

console.log(human.foodPreference); // This will print Shawarma.
```