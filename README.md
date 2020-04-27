# jsChallenges

a collection of challenges for JS / web dev.

These are organized by topic folders. Until v1.0 (when this goes public), feel free to add new challenges within a topic or a new topic entirely.


## Format


Instead of .js files with comments, you can write [markdown files](https://github.github.com/gfm/) with code, which render well on GitHub and in VS Code.


### Code

You can write a code block in markdown by enclosing it in three backticks. Immediately after the opening backticks, write "js" to mark it as JS syntax for highlighting purposes. Example:
````
```js
import 'somelibrary';
let xs = new Set([1,2,3]);
console.log(document);
```
````
becomes
```js
import 'somelibrary';
let xs = new Set([1,2,3]);
console.log(document);
```

### Headers

We also want YAML headers at the start of each document. This is for later, when we might want to compile these into a site and have a system to sort by difficulty or tags. These look like this:

```yaml
---
title: My super cool array challenge
author: anonymous
difficulty: 2.5
tags: [functions, arrays, array methods]
---
```

- We still need to agree on standards for difficulty ratings.
- Proposal: difficulty should be increments of .5.
- If you write a new challenge, add your name as author (so we can complain to you 😉).
- If you add a challenge from somewhere else on the internet, you can add a `source` field with a URL.



## To-do

- [ ] import existing challenges
- [ ] finish style guide
- [ ] write longer/different README for when/if students access these