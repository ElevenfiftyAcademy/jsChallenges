---
title: FizzBuzz
author: anonymous
difficulty: 1.5
tags: [conditionals, operators]
---

# FizzBuzz

Store a number in a variable `fb`.
Write a conditional that: 
- Prints out (`console.log`) "Fizz" if the number is divisible by 3
- Prints out "Buzz" if the number is divisible by 5
- Prints out "FizzBuzz" if the number is divisible by BOTH 3 and 5
- If none of the above conditions hold, print the number itself


If/else solution:

```js
if (fb % 15 === 0) {  // alternatively, (fb % 3 === 0 && fb % 5 === 0)
  console.log('FizzBuzz');
} else if (fb % 5 === 0) {
  console.log('Buzz');
} else if (fb % 3 === 0) {
  console.log('Fizz');
} else {
  console.log(fb);
}
```

Switch solution:

```js
switch (true) {
  case (fb % 15 === 0):
    console.log('FizzBuzz')
    break;
  case (fb % 5 === 0):
    console.log('Buzz')
    break;
  case (fb % 3 === 0):
    console.log('Fizz')
    break;
  default:
    console.log(fb)
```

Ternary solution:

```js
(fb % 15 === 0) ? console.log('FizzBuzz')
  : (fb % 5) ? console.log('Buzz')
    : (fb % 3) ? console.log('Fizz')
      : console.log("It's not divisible")
```



### notes

Instead of printing out the number as the default, you can have students print out a message using string interpolation.