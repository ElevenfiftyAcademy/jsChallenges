---
title: Whose name is longer?
author: anonymous
difficulty: 1.5
tags: [strings, conditionals, string methods]
---

# Whose name is longer?

## the challenge

### Bronze

Write two variables. One will store your name and another will store a friend's name.
Find out what property you can use to check how long the names are.
`console.log` how many letters are in each name.

### Silver

Expand on what you have already done and write a conditional to see who has the longer name.
Using string interpolation, `console.log` whose name is longer.
Example Result: "My name is longer than Adam's."

### Gold

In the `console.log` include how many letters difference there are between the names.
Example Result: "Adam's name is shorter than mine by 4 letters."

### Platinum

There is also one additional case that should be handled that has not been mentioned so far.
See if you can add that to your conditional!



## solutions

### Bronze

```js
let myName = "Danielle";
let friend = "Adam";

console.log(myName.length);
```

### combined Silver/Gold/Platinum

```js
if (myName.length > friend.length){
  let letters = myName.length - friend.length;
  console.log(`${friend}'s name is shorter than mine by ${letters} letters`);
} else if (myName.length < friend.length) {
  let letters = friend.length - myName.length
  console.log(`${friend}'s name is longer than mine by ${letters} letters`);
} else {
  console.log('Our names are the same length!');
}
```