---
title: Reversing an array
author: anonymous
difficulty: 1.5
tags: [arrays, array methods]
---

# Reversing an array

## the challenge

Create an array and store it in a variable.
Then write code that does the following:

1. First, check to make sure the variable holds an array.
2. Then, use an array method to reverse the elements of the array. (Use the internet!)
3. Using a method (not a loop), print out each value of the reversed array in order.


### optional hints

1. You'll need some kind of conditional...
2. Google 'array reverse javascript'
3. Remember the `.forEach` method, which takes a function


## a solution

```js
let arr = [1, 2, 3, 4, 5];

// 1
if (arr instanceof Array) {
  
  // 2
  let revArr = arr.reverse();

  // 3
  revArr.forEach(x => console.log(x));
}
```