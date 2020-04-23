# Objects: swapping values

## the challenge

Create a function that swaps the value of any 2 specified properties in a object, make sure you don't mutate (change) the original object. 
Your function may have three parameters: the original object, prop1, and prop2.


## solutions

### incorrect solution

Notice use of dot notation with the parameters in the function. This attempt *adds* two new properties called `prop1` and `prop2` to `obj` if those properties don't exist already.

```js
const person = {
  fName: 'Tom',
  lName: 'McClellan'
};

function changePerson(obj, prop1, prop2) {
  
  let temp = obj.prop1;
  obj.prop1 = obj.prop2;
  obj.prop2 = temp;

  return obj;
}

newObj = changePerson(person, 'fName', 'lName');

console.log(newObj);
```

### solution

Here we use square brackets to get the value of the properties we pass in as strings.

```js
const person = {
  fName: 'Tom',
  lName: 'McClellan'
};

const food = {
  food1: 'Steak',
  food2: 'Tacos'
};

const changePerson = (obj, prop1, prop2) => {
  let newObj = Object.assign({}, obj);
  // let newObj = obj;
  // do not mutate original object!

  let temp = newObj[prop1];
  newObj[prop1] = newObj[prop2];
  newObj[prop2] = temp;

  return newObj;
}

const newObject = changePerson(food, 'food1', 'food2');
console.log(food, "Unchanged Object");
console.log(newObject, 'Changed Object');
```


## notes

The correct solution makes use of `Object.assign`, which you might want to discuss.