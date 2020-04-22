# Set challenge

1. Using the array [1,2,2,3,4,5,5,5,6,6,7], convert this into a Set object (you'll probably have to look up what Sets are and how to create them). What happens when you do this? Why might this (and Sets in general) be useful in programming?
2. Add the number 8 to the set, and take out the number 3.
3. Now convert the Set back into an array using the spread operator.


A solution:

```js
let arr = [1,2,2,3,4,5,5,5,6,6,7];

let set = new Set(arr);
console.log(set);

set.add(8);
set.delete(3);
console.log(set);

let arr2 = [...set];
console.log(arr2);
```
