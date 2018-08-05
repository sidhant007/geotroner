# GeoTroner

## More info can be found [here](https://devpost.com/software/geotroner)

## Inspiration
Our inspiration is the classic arcade game **Tron**, but then we thought why be bounded by a 2d grid, when you have the whole world around you. 

## What it does
It is a real-time online multiplayer game where users can create chains (i.e a polyline) and with the help of other users extend their chains. Each chain is defined by its color and the coordinates of the users which are a part of it. With the help of other users, you aim to maximize the number of nodes in your chain. Now the interesting part starts- 
If you self intersect your own chain, your entire chain is killed.

If you move to another place in real-time and are a part of a chain, then your chain also stretches and skews.
If your chain intersects with another chain and if you have at least half the number of users in your chain as compared to your opponent's, you kill it :) However if your opponent's chain has more than half of your users then you get killed. 

The scoring system is- 

Your Score += 50 (When you create a chain)

Your Score += 50 (When you join a chain)

Your Score += 50 (When you extend a chain)

Your Score += 100 * Number of nodes in your opponent chain (When you kill another chain)

Your Score += 500 * Number of nodes in your opponent chain (When you are the one who kills the other chain)

## How we built it
We build it primarily using node.js with express framework. We used sockets.io and bootstrap along with it. The main apis used were Google Map and npm module of geoDist to calculate distances between coordinates.

## Challenges we ran into
Fixing non - euclidean distance calculation on a map.

Conquered callback hell.

## Accomplishments that we're proud of
The game works :")

## What we learned
Got more proficient with node.js, google map api and bootstrap.

## What's next for GeoTroner
Adding special zones where you can get power ups. 

Allowing people to split their chain into 2 pieces.

Live chat with your teammates (i.e those who are on your chain).
