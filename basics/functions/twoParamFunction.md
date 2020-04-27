# Two-parameter function challenge

## the challenge

Write a function that takes two parameters:
- One parameter is for a first name,
- The other paramter is for a last name;
- Have them come together in a variable inside the function.
- `console.log` 'Hello, my name is Maxwell Smart.'
- Call your function 


## a solution

```js
function myName(fName, lName) {
  let fullName = fName + ' ' + lName;
  console.log(`Hello, my name is ${fullName}.`);
}

myName('Maxwell', 'Smart');  // Hello, my name is Maxwell Smart
```