---
title: Map challenge
author: Eli T. Drumm
difficulty: 2
tags: [data structures, Map]
---

# Map challenge

## the challenge

1. Create a new Map object `petMap` where the key "cat" has the value 2, "dog" has the value 3, "fish" has the value 1, and "parakeet" has the value 0. Hint: you can do this either by passing an array of arrays to the Map constructor, or by creating an empty Map and using `.set` for each key-value pair individually.
2. Using `.set`, reassign "cat" to be 5. Check the size of `petMap` to make sure there are still 4 keys in it.
3. Now `console.log` the value of "dog".
4. Write a function that takes an array of elements and returns true only if every element is the array is a key in `petMap`. Bonus points for using an array method (keyword: "every").
5. When might you use a Map for storing keys and values as opposed to a regular Object? (see the docs!)




## a solution

```js
// 1
const petArray = [["cat", 2], ["dog", 3], ["fish", 1], ["parakeet", 0]];

let petMap = new Map(petArray);

// 2
petMap.set("cat", 5);
console.log(petMap.size);

// 3
console.log(petMap.get("dog"));

// 4
const petMapCheck = arr => arr.every(x => petMap.has(x));
```


For number 5, see the chart at the top of [the MDN docs on Map](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map). Some answers include
- arbitrary types of keys
- no default or inherited keys
- performance
- Maps are iterable and have a .forEach method