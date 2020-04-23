# typeof/conditionals challenge

## the challenge

### Bronze

Create an Object that contains a string, number, boolean, and object.
`console.log` the type of one of the values in the object.

### Silver

Write a conditional that checks the type of one of the values stored in the object and console logs the data type. If the value is not a string, number, boolean, or object `console.log` 'What are you?!'.

### Gold

Rewrite this as a ternary.

### Platinum

Add a condition to check if the value is an array.





## solutions

### Bronze

```js
let obj = {
  string: 'test',
  number: 10,
  boolean: false,
  object: { key: 'value' }
};
console.log(typeof obj.object.key);

let objValue = obj.number;
console.log(typeof objValue);
```

### Silver

```js
if (typeof objValue === 'string') {
  console.log(`It's a string!`);
} else if (typeof objValue === 'number') {
  console.log(`It's a number!`);
} else if (typeof objValue === 'boolean') {
  console.log(`It's a boolean!`);
} else if (typeof objValue === 'object') {
  console.log(`It's a object!`);
} else {
  console.log('What are you?!');
}
```

### Gold

```js
console.log(
  typeof objValue === 'string' ? 'This is a string' 
  : typeof objValue === 'number' ? 'This is a number'
  : typeof objValue === 'boolean' ? 'this value is a boolean'
  : typeof objValue === 'object' ? 'this value is an object'
  : 'What are you?!'
);
```

### Platinum

The condition we want to add to the conditional is either
```js
Array.isArray(objValue)
```
or 
```js
objValue instanceof Array
```