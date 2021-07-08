---
title: JS design pattern
date: "2020-07-06T22:40:32.169Z"
description: ES5 design pattern.
--- 

## Constructor Pattern

```js

/*
 * Constructor Pattern
 */
class Car {
  constructor(opts) {
    this.model = opts.model;
    this.year = opts.year;
    this.miles = opts.miles;
  }

  // Prototype method
  toString() {
    return `${this.model} has driven ${this.miles} miles`;
  }
}

// Usage:
var civic = new Car({
  model: 'Honda',
  year: 2001,
  miles: 50000
});

// ES5 Example of constructor function
function Car() {
  this.model = opts.model;
  ...
  ...
}
Car.prototype.toString = function() {
  ...
}
```

## Module Pattern

```js
/* lib/module.js */
const shoppingList = new WeakMap()

/**
 * Module Pattern
 */
class AbstractDataType {
  constructor() {
    // woo! our Class is instantiated lets add some private properties.
    shoppingList.set(this, ["coffee", "chicken", "pizza"])
  }

  // Lets create a public prototype method to access our private `shoppingList`
  getShoppingList() {
    return shoppingList.get(this)
  }

  addItem(item) {
    shoppingList.get(this).push(item)
  }
}

// Now we export our `Class` which will become an importable module.
export default AbstractDataType
```

`WeakMap` is also a new ES6 feature that seems to be a good option for creating private memebers. It accepts any value as a key and doesn't prevent the key object from getting garbage collected when the `WeakMap` object still exists. It remove any entry containing the object once it's garbage collected.

## Observer Pattern

```js
/*
 * Observer Pattern
 */
var model = {}
Object.observe(model, () => {
  // async callback
  changes.forEach(change => {
    console.log(change.type, change.name, change.oldValue)
  })
})
```

Another popular pattern that is being simplified in ES6/ES7 is the `Observer Pattern`. If you're not familiar the `Observer Pattern` is a design pattern in which an object (known as the subject) maintains a list of objects depending on what it observes (observers), automatically notifying them of any changes to state. In ES5 this was a little cumbersome to setup but not difficult. You created a ObserverList constructor function which creates an empty list of observers. After that you create an interface of public prototype methods for tasks like adding, deleting, etc. Now it's much more simple we have a handy dandy Object.observe method we can use to do the same job with a lot less code.
