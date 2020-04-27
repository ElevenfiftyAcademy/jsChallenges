---
title: Tip calculator
author: anonymous
difficulty: 1.5
tags: [functions]
---

# Tip calculator

## context

Practice with `return` keyword.

## the challenge

- Make a tip calculator using a function
- Have it *return* the value 
- Capture that returned value in a variable
- Print that variable


## a solution

```js
function tipCalc(bill) {
  let tip = bill * 0.2;
  return tip.toFixed(2);
}

let totalTip = tipCalc(19.88);
console.log(totalTip);  // 3.98
```

Things to explain:
- `.toFixed`
- the difference between `return` and `console.log`