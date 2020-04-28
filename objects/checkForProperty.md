---
title: Check for a property
author: anonymous
difficulty: 1.5
tags: ['objects']
---

# Check for a property

## context

At this point in the course, some students might be ready for the bonuses, most probably won't be.


## the challenge

```js
let exampleObj = {
  name: 'Hulk',
  alterEgo: 'Bruce Banner',
  age: 34,
  color: 'green',
  smashes: true
};
```

Create a function that takes in an object, for example the one above.

In the function, check if the object contains a specific property and return a boolean answer. By this we mean

Bonus: modify your function to take in an object *and* a string, and checks the object for a key matching that string. Hint: consider the `in` keyword.

Double bonus: modify your function to take in an object and *two* strings `k` and `v`, and checks the object for the key `k` having the value `v`.


## a solution

Using our `exampleObj`, writing a function to check that `color` has the value of `green`.

```js
function (obj) {
  if (obj.color === 'green') {
    return true;
  } else {
    return false;
  }
}
```


Bonus:

```js
function (obj, k) {
  if (k in obj) {
    return true;
  } else {
    return false;
  }
}
```


Double bonus:

```js
function (obj, k, v) {
  if (obj[k] === v) {
    return true;
  } else {
    return false;
  }
}
```



