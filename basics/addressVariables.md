# Variables challenge

## the challenge

Set 7 (or 8) variables:
- `firstName`
- `lastName`
- `houseNumber`
- `aptNumber` (if applicable)
- `street`
- `city`
- `state`
- `zipcode`

You'll have to figure out the right type for each variable.

Then `console.log` the whole address.

Bonus: how do we break a line?

## a solution

```js
let firstName = 'Bill';
let lastName = 'Gates';
let houseNumber = 7400;
let street = 'NE 18th Street';
let city = 'Medina';
let state = 'WA';
let zipcode = 98039;

console.log(firstName, lastName + ',', houseNumber, street + ',', city + ',', state, zipcode);
// Bill Gates, 7400 NE 18th Street, Medina, WA 98039
```

Bonus solution:

```js
console.log(firstName, lastName + '\n' + houseNumber, street + ',', city + '\n' + state, zipcode);
```

For both, notice `console.log` automatically puts spaces between the things we give it (arguments), so in order to *not* have the space (like before the commas), we need to use the `+` concatenation operator.