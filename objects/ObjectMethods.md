---
title: Methods of Object
author: anonymous
difficulty: 2
tags: [Object, object methods]
---

# Methods of Object

## the challenge

```js
const obj = {
    react: 'awesome',
    node: 'also awesome',
    javaScript: 'super cool',
    python: 'ok I guess'
};
```

Given the above object, find a function (or a method of some object) that returns an array of all the keys in that object. If you can't find such a function, you can write one yourself.

*Hint: look at the documentation for the Object object.*

Then, find or write a function (or method) that returns all the *values* of the object as an array.


## solution

The function we are looking for is the `.keys` method of `Object`.

```js
const objKeys = Object.keys(obj);
```

Similarly, the `Object.values` method returns an array of all the values:

```js
const objValues = Object.values(obj);
```

We can also do this manually using a for-in loop, but the methods above are preferable for this case.




## notes

I used this as an example to lightly introduce the difference between methods of `Object` and instance methods, which you can show are of the form `Object.prototype.methodName`.

Also, there are some other methods of `Object` that you could mention (e.g. `.entries`, `.freeze`).