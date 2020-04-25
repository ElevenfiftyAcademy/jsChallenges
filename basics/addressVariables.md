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
let firstName = 'Tyler';
let lastName = 'Shelton';
let houseNumber = 12175;
let street = 'Visionary Way';
let city = 'Fishers';
let state = 'IN';
let zipcode = 46038;

console.log(firstName, lastName + ',', houseNumber, street + ',', city + ',', state, zipcode);
// Tyler Shelton, 12175 Visionary Way, Fishers, IN 46038
```

Bonus solution:

```js
console.log(firstName, lastName + '\n' + houseNumber, street + ',', city + '\n' + state, zipcode);
```

For both, notice `console.log` automatically puts spaces between the things we give it (arguments), so in order to *not* have the space (like before the commas), we need to use the `+` concatenation operator.