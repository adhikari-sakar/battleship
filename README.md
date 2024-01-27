# Battleship Game

## Requirements
- JDK 8
- [Maven 3.6.x](https://maven.apache.org/download.cgi)
- [Docker](https://www.docker.com/products/docker-desktop) - Execute `docker run hello-world` to ensure docker is able to pull and run images

## Problem statement
Our aim is to write a Java program that will play the popular game of [Battleship](https://en.wikipedia.org/wiki/Battleship_%28game%29) against the computer.

The game is played on two fields, each 10 X 10 squares. The columns are labeled A-J, and
the rows are labeled 1-10. Each player's fleet of ships consists of one aircraft carrier, one
battleship, one destroyer, one submarine and one cruiser.

![Game in progress image](https://upload.wikimedia.org/wikipedia/commons/thumb/6/65/Battleship_game_board.svg/800px-Battleship_game_board.svg.png "A map of one player's ships from a game in progress")

The size and shape of each ship is as follows:
- Destroyer (2 squares)
- Submarine (3 squares)
- Cruiser (3 squares)
- Battleship (4 squares)
- Aircraft Carrier (5 squares)

Before the game starts, each player secretly places their ships anywhere on their own playing field. Ships cannot overlap one another, but may be placed either vertically or horizontally. The players don't know where the opponent's ships have been allocated.
The first turn is determined by some random means (throwing a die). Players take turns to try to guess the location of the other's ships by naming a square (e.g. F7). The opponent declares the square to be a hit or a miss, depending on whether there is a ship occupying that square. When all the squares occupied by a particular ship have been guessed, the player must announce that that particular ship is sunk. A player keeps track of the hits and misses on a copy of the opponent's field.
The first player to sink all the other's ships is the winner.


## Build

```
mvn clean package
```

## Docker network creation

```
docker network create battleship_net
```

## Run

```
docker-compose up --build
```

## Postman
[Postman project](docs/postman)
