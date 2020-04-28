---
title: Basic array retrieval
author: anonymous
difficulty: 1
tags: [arrays]
---

# Basic array retrieval

## the challenge

```js
let muppets = ['Kermit', 'Fozzie', 'Gonzo', 'Rowlf', 'Piggy', 'Scooter', 'Beaker'];

let characters = [['Daphne', 'Fred', 'Velma', 'Shaggy', 'Scooby'],
                  ['Fred', 'Wilma', 'Barney', 'Betty', 'Dino'],
                  ['George', 'Elroy', 'Judy', 'Jane', 'Rosie']]
```

1. Go into the `muppets` array and assign 'Scooter' to a variable. Then `console.log` the variable.
2. Now go into the array and print out 'Kermit the Frog'. (You'll need to add 'the frog'!)
3. Go into the nested `characters` array and `console.log` 'Barney'.
4. Finally, go into `characters` and print out 'Shaggy and Scooby love sandwiches'.


## a solution

```js
// 1
let scooter = muppets[5];
console.log(scooter);

// 2
console.log(muppets[0] + ' the frog');

// 3
console.log(characters[1][2]);

// 4
console.log(`${characters[0][3]} and ${characters[0][4]} love sandwiches`)
```



