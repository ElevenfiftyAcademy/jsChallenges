---
title: 'Digging into Objects: The Good Place'
author: anonymous
difficulty: 1.5
tags: [objects, loops]
---

# Digging into objects: The Good Place

## the object in question

```js
let theGoodPlace = {
  id: 9,
  likes: 932,
  name: "The Good Place", 
  seasonInfo: {
    season1: {
      numberOfEpisodes: 5,
      episodeInfo : [
        { episode: 1, episodeName: "Pilot"},
        { episode: 2, episodeName: "Flying"},
        { episode: 3, episodeName: "Tahani Al-Jamil"},
        { episode: 4, episodeName: "Jason Mendoza"},
        { episode: 5, episodeName: "Category 55 Emergency Doomsday Crisis"}
      ]
    },
    season2: {
      numberOfEpisodes: 6,
      episodeInfo : [
        { episode: 1, episodeName: "Everything is Great!"},
        { episode: 2, episodeName: "Dance Dance Resolution"},
        { episode: 3, episodeName: "Team Cockroach"},
        { episode: 4, episodeName: "Existential Crisis"},
        { episode: 5, episodeName: "The Trolley Problem"},
        { episode: 6, episodeName: "Janet and Michael"}
      ]
    },
    season3: {
      numberOfEpisodes: 5,
      episodeInfo : [
        { episode: 1, episodeName: "Everything Is Bonzer!"},
        { episode: 2, episodeName: "The Brainy Bunch"},
        { episode: 3, episodeName: "The Snowplow"},
        { episode: 4, episodeName: "Jeremy Bearimy"},
        { episode: 5, episodeName: "The Ballad of Donkey Doug"}
      ]
    }
  },
  description: "Four people and their otherworldly frienemy struggle in the afterlife to define what it means to be good."
};
```


## the challenge

Using the above object:
1. `console.log` the description
2. `console.log` the episode name of episode 3 of season 2
3. `console.log` each episode name in season 3 using only one `console.log` (it can be in a loop!)


## a solution

```js
// 1
console.log(theGoodPlace.description);

// 2
console.log(theGoodPlace.seasonInfo.season2.episodeInfo[2].episodeName);

// 3
for (let episode of theGoodPlace.seasonInfo.season3.episodeInfo) {
  console.log(episode.episodeName);
}
```