---
title: 'Presidential array methods: sort'
author: anonymous
difficulty: 2
tags: [arrays, array methods]
---


# Presidential array methods: `sort`

## challenge 1

### the challenge

Using `Array.prototype.sort()`, sort the presidents by birth year, oldest to youngest. You will need to implement logic that checks the year each president was born.

### possible solutions

#### Expanded solution

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

#### Concise solution

```js
const orderedConcise = presidents.sort((a, b) => a.year - b.year);
```


## challenge 2

### the challenge

Using the same `.sort()` method, sort the presidents by last name, then by first name when two presidents have the same last name.

### a solution

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