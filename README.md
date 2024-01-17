# CSB430_Week3_TPS
## Team Design of Software Architecture
This in-class project will require student teams to brainstorm on a project idea, pick an architectural style and do some design around the project. This is the first part of a two-part in-class project.

## 1. Selection of Project Idea
### Team Choice:
The Card Matching Game "Memory" (a web game)

## 2. Requirements Gathering
### Functional:
Card grid, Score board, Click on cards to reveal them, timer/lives component, Keep track of found pairs and hide found cards on the grid, Match all cards to win, Game settings, Difficulty levels, Game levels 
### Non-Functional:
interactive User-interface, responsive and enjoyable User-experience

## 3. Choosing the Architectural Style
### Decision:
Model View Controller (MVC) Architecture.
### Reasoning:
The design of the game best supports the MVC architecture because we need a game UI for the user to interact with and view the game, we need data that represents cards that are accessed by the model, and the game logic and interactivity will be handled by the controller.


## 4. High-Level Design
### Model: 
Card Data, Level Data, Difficulty Settings Data, art assets
### View: 
Game UI, Card Grid, Display Game Data, Display setting menu
### Controller: 
game logic, on click event handlers
