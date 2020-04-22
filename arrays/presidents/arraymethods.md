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

Using the `Array.prototype.reduce()` method, find the total number of years that presidents have lived.
You will need to implement logic that checks if the president is still currently living.
If the president IS still currently living, use the current year.

Solution:
```js
// solution goes here
```