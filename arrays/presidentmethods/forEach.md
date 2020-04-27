---
title: 'Presidential array methods: forEach'
author: anonymous
difficulty: 1.5
tags: [arrays, array methods]
---


# Presidential array methods: `forEach`

## the challenge

- Write a function that uses the `Array.prototype.forEach()` & the `Array.prototype.push()` methods within it.
- Using the `.forEach` method, loop over all of the presidents from our presidents array.
- Then, push the president's last name and the year they were born to a new array as individual objects containing key/value pairs of each president's last name and date of birth.
- Then, return the new array from the function.


## a solution

```js
function pres () {
  let copy = [];

  presidents.forEach(president => {
    copy.push({
      last: president.last,
      yearBorn: president.year
    });
  })
  return copy
}

let newArr = pres();
console.log(newArr);          // [the whole new array]
console.log(newArr[8].last);  // 
```

