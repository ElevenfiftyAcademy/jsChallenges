# Recreating the array methods

## the challenge

Write four functions that mimic the array methods we've learned so far. These will be plain functions, not methods, so they will take the array as an argument.

1. `myForEach`, which takes an array and a function and applies the function to each element in the array in order.
2. `myMap`, which takes an array and a function and returns a new array containing the results of applying the function to each element of the array in order.
3. `myFilter`, which takes an array and a function and returns a new array consisting of only those elements in the original array for which the function returns `true`.
4. `myReduce`, which takes an array, a function, and an initial value. It applies the function to the initial value and the first element in the array, then it applies the function to that result and the second element in the array, and so on, until it has a final value.

These are ordered from easier to harder, so if you can only get the first two or three, that's OK. Needless to say, do not use any array methods in your functions!


## possible solutions

```js
function myForEach (arr, f) {
  for (let x of arr) {
    f(x);
  }
}

function myMap (arr, f) {
  let mappedArr = [];
  for (let x of arr) {
    mappedArr.push(f(x));
  }
  return mappedArr;
}

function myFilter (arr, f) {
  let filteredArr = [];
  for (let x of arr) {
    if (f(x)) {
      filteredArr.push(x);
    }
  }
  return filteredArr;
}

function myReduce (arr, f, init) {
  let currval = init;
  for (let x of arr) {
    currval = f(currval, x);
  }
  return currval;
}
```