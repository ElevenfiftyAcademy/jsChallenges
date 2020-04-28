---
title: 'Digging into objects: Superstore'
author: anonymous
difficulty: 1.5
tags: [objects]
---

# Digging into objects: *Superstore*

## the challenge

Using the following object:

```js
var superstore = {
  id: 9,
  name: "Superstore",
  season1: {
    seasonInfo: {
      episodeInfo : [
        { episode: 1, episodeName: "Pilot"},
        { episode: 2, episodeName: "Magazine Profile"},
        { episode: 3, episodeName: "Shots and Salsa"},
        { episode: 4, episodeName: "Mannequin"},
        { episode: 5, episodeName: "Shoplifter"},
        { episode: 6, episodeName: "Secret Shopper"},
        { episode: 7, episodeName: "Color Wars"},
        { episode: 8, episodeName: "Wedding Day Sale"},
        { episode: 9, episodeName: "All-Nighter"},
        { episode: 10, episodeName: "Demotion"},
        { episode: 11, episodeName: "Labor"}
      ]
    }
  },
  season2: {},
  season3: {}
};
```

1. `console.log` the whole object
2. `console.log` just the season info for season 1
3. `console.log` the episode name of the fifth episode of season 1
4. Pick an episode in `episodeInfo` and save it to a variable. Then `console.log` "Episode [number] of season 1 is called '[title]'" for your episode.


## a solution

```js
// 1
console.log(superstore);

// 2
console.log(superstore.season1.seasonInfo);

// 3
console.log(superstore.season1.seasonInfo.episodeInfo[4].episodeName);

// 4
let myEpisode = superstore.season1.seasonInfo.episodeInfo[6];
console.log("Episode " + myEpisode.episode + " of season 1 is called " + myEpisode.episodeName + "'");
```