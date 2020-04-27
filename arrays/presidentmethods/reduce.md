---
title: 'Presidential array methods: reduce'
author: anonymous
difficulty: 2.5
tags: [arrays, array methods]
---


# Presidential array methods: `reduce`

## challenge 1

### the challenge

Using the `Array.prototype.reduce()` method, find the sum of the birth years of all the presidents. So, it should be 1732 + 1735 + ... etc.

### a solution

```js
function sumAllYears (presArray) {
  return presArray.reduce((acc, currVal) => acc + currVal.year, 0)
}
```



## challenge 2

### the challenge

Using the `Array.prototype.reduce()` method, find the total number of years that presidents have lived.
You will need to implement logic that checks if the president is still currently living.
If the president IS still currently living, use the current year.

### a solution

```js
function livingYears (presArray) {
  return presArray.reduce((acc, currVal) => {
    if (currVal.passed !== undefined) {
      return acc + currVal.passed - currVal.year;
    } else {
      return acc + 2020 - currVal.year;
    }
  }, 0);
}
```