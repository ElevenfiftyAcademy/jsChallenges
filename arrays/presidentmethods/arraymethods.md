# Array Method Challenges

Use the presidents array in presidents.js for the following challenges.

## forEach

Write a function that uses the `Array.prototype.forEach()` & the `Array.prototype.push()` methods within it.
Using the forEach method, loop over all of the presidents from our presidents array.
Then, push the president's last name and the year they were born to a new array as individual objects containing key/value pairs of each residents last name and date of birth.
Then, return the new array from the function.

Solution:
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

let newArr = pres()
console.log(newArr)
console.log(newArr[8].last)
```


## filter

Using the `Array.prototype.filter()` method, filter through the presidents array and console.log() only the presidents who were born in the 1900's.

Solution:
```js
// solution goes here
```


## map

Using the `Array.prototype.map()` method, create a new array of strings, one for each president, where each string says "[PRESIDENT NAME] was born in [YEAR]".

```js
// solution goes here
```


## reduce

### challenge 1

Using the `Array.prototype.reduce()` method, find the sum of the birth years of all the presidents. So, it should be 1732 + 1735 + ... etc.

```js
function sumAllYears (presArray) {
  return presArray.reduce((acc, currVal) => acc + currVal.year, 0)
}
```

### challenge 2

Using the `Array.prototype.reduce()` method, find the total number of years that presidents have lived.
You will need to implement logic that checks if the president is still currently living.
If the president IS still currently living, use the current year.

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

## sort

### challenge 1

Using `Array.prototype.sort()`, sort the presidents by birth year, oldest to youngest. You will need to implement logic that checks the year each president was born.

Expanded solution:
```js
const ordered = presidents.sort((a, b) => {
    if(a.year > b.year){
        console.log('A: ' + a.last)
        console.log('B: ' + b.last)
        return 1
    } else {
        return -1
    }
});
```

Concise solution:
```js
const orderedConcise = presidents.sort((a, b) => a.year - b.year);
```

### challenge 2

Using the same `.sort()` method, sort the presidents by last name, then by first name when two presidents have the same last name.

```js
const nameOrdered = presidents.sort((a, b) => {
  if (a.last < b.last) {
    return -1;
  } else if (a.last > b.last) {
    return 1;
  } else {
    if (a.first < b.first) {
      return -1;
    } else if (a.first > b.first) {
      return 1;
    } else {
      return 0;
    }
  }
});
```