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

## Objects in Javascript


### Creating an object

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

### Storing arrays, functions and objects

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

### Accessing values

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

A *key* can also be more than one word. But to do that the *key* will have to be quoted.

```javascript
let human = {
    name: 'Tony Stark',
    age: 40,
    'food preference': 'Shawarma',
    isAnAvenger: true
};
```

If the *key* is multiple words, the `.` notation will not work. Here you have to use `[]` to access the property.

```javascript
let human = {
    name: 'Tony Stark',
    age: 40,
    'food preference': 'Shawarma',
    isAnAvenger: true
};

console.log(human['food preference']); // This will print Shawarma.
```

Nested objects are accessed the same way

```javascript
let human = {
    name: 'Tony Stark',
    age: 40,
    foodPreference: 'Shawarma',
    isAnAvenger: true,
    girlfriend: { // Another object
        name: 'Pepper Potts',
        age: 30,
        isAnAvenger: false
    }
};

console.log(human.girlfriend.name); // This will print 'Pepper Potts'
```

### Adding more properties

After an object is created, we can add more properties directly to the object using the `.` notation again.

```javascript
let human = {
    name: 'Tony Stark',
    age: 40,
    'food preference': 'Shawarma',
    isAnAvenger: true
};

human.facialHair = true;

console.log(human);
```

This will print

```bash
{
    name: 'Tony Stark',
    age: 40,
    'food preference': 'Shawarma',
    isAnAvenger: true
    facialHair: true
}
```

### Modifying existing properties

Similar to arrays, objects allow you to directly modify any value in an object property

```javascript
let human = {
    name: 'Tony Stark',
    age: 40,
    'food preference': 'Shawarma',
    isAnAvenger: true
};

human.age = 35;

console.log(age);
```

This will print the following to the console.

```bash
{
    name: 'Tony Stark',
    age: 38,
    'food preference': 'Shawarma',
    isAnAvenger: true
}
```

### Deleting properties

Properties, once added, can be deleted using the `delete` keyword.

```javascript
let human = {
    name: 'Tony Stark',
    age: 40,
    'food preference': 'Shawarma',
    isAnAvenger: true
};

delete human.isAnAvenger. // Shh...let's keep it a secret!

console.log(human);
```

This will print the following to the console

```bash
{
    name: 'Tony Stark',
    age: 38,
    'food preference': 'Shawarma'
}
```

**Pro Tip** 💡: Did you know that arrays in Javascript are *actually* objects? 😱

### 🧠 Test your skills!

1) Try to model something you use on a daily basis, like a cellphone or a laptop as a javascript object. Add properties to it, delete properties from it. 