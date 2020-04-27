---
title: Zipper challenge
author: anonymous
difficulty: 2
tags: [arrays, array methods]
---

# Zipper challenge

## the challenge

Given 2 arrays:
- `[10,20,30,40,50,70]`
- `[5,3,2,5]`

Create a function that multiplies 'like' indexes (0 with 0, 1 with 1, etc.) together then places the values in a new array. 
The function you create should return `[50, 60, 60, 200]` based on the arrays above.
Make sure the values given to the function are an array type and they have data inside of them.
If the first array has more values than the second, only return an array the length of the second (that is, skip over values from the first array that have no counterpart in the second array).
If the second array has more values than the first, 


## a solution

```js
const tensArray = [10,20,30,40,50,70];
const onesArray = [5,3,2,5];

const multiplyValues = (arr1, arr2) => {
  arr1 = (typeof arr1 == 'object' && arr1 instanceof Array && arr1.length > 0) ? arr1 : false;
  arr2 = (typeof arr2 == 'object' && arr2 instanceof Array && arr2.length > 0) ? arr2 : false;
  
  let newArray = [];
  
  if (arr1 && arr2) {
    
    for (let i = 0; i < Math.min(arr1.length, arr2.length); i++) {
      newArray.push(arr1[i] * arr2[i]);
    }

    return newArray;

  } else {
    return 'Error: Please provide valid arrays';
  }
}

let funArr = multiplyValues(tensArray, onesArray);
console.log(funArr);
```





## notes

The original version of this challenge didn't have the last condition about only zipping together as many elements as can be paired, I have added this, which matches the behavior of what the original author says the result should be for the given arrays.

The original of this challenge used default arguments for `arr1` and `arr2`, these have been removed for clarity.

Parentheses have been added for clarity in ternaries, these are not strictly needed.