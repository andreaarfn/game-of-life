# Game of Life

> This is a personal project that I created to get some hands in C language.

---

<p align="center">
  <img align="center" src="docs/animations/animation.gif" alt="Main Gif"/>
</p>

---

## Description

In this project I used C to build the Conway's Game of Life. 
The project contains two modules:
 - *life*: contains the game of life logic in both serial, and openmp parallelized
 - *animations*: contains an app to run the game of life in the console.

---

## Building & Running

```
  make                #Runs both serial and parallel version
  make run_serial     #Run just the serial (original) version
  make run_omp        #Run just the OpenMP version
```

---

## Usage

To run the game of life you can clone the repo and run the Makefile in the *animations* directory:

```
    .../game-of-life/animations$ make
```

---

## About Conway's Game of Life

The Game of Life, also known simply as Life, is a cellular automaton devised by the British mathematician John Horton Conway in 1970. It is a zero-player game, meaning that its evolution is determined by its initial state, requiring no further input. One interacts with the Game of Life by creating an initial configuration and observing how it evolves. It is Turing complete and can simulate a universal constructor or any other Turing machine.

You can check mor information about game of life [here](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life).

<p align="center">
  <img align="center" src="docs/animations/Gospers_glider_gun.gif" alt="Wiki Gif"/>
</p>

