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
Card Data, Game Logic, Level Data, Difficulty Settings Data, art assets
### View: 
Game UI, Card Grid, Display Game Data, Display setting menu
### Controller: 
Connect Model and View Logic, on click event handlers

# CSB430_Week4_TPS

## 5. Detailed Design

### Step 1:
**Classes**
- ModelClass - Game logic (FlipCard, CheckMatch, IsGameOver) & Data (CardData)
- ViewClass - Display Game Board, Stats, On-Click Event Handler
- ControllerClass - Connects Model and View

### Step 2:
**Classes**
- ConfigClass - For user Settings (session/cookie storage)

### Step 3:
### **a**
- ControllerClass -> Initialization: Takes in the view and model classes to maintain a reference. Tells model class to either pull in art assets (either from 3rd party or the repo where the project lives).
- ControllerClass -> Shuffle: Seeds a random value and then shuffles the deck of cards to match
### **b**
- This project is not complex enough to justify the use of interfaces. Also, we plan on building the project in JavaScript which may not even support interfaces.
### **c**
- Model: cardArt: an object collection of int identifiers and image references
- Model: userConfig: JSON object with user configuration settings such as difficulty or sound on/off
- Model: uiConstants: strings and numbers used for parts of the UI that we may want to make extra fancy but also want to be consistent
### **d**
- View class: receives the id of cards that were clicked by the user and sends them to the controller -> Controller class: receives the id of cards, compares them and returns whether they are matches. returns the result back to the view class. -> View class: resets the two cards (puts them in face down state) that were clicked if they were not matches. Leaves them face up if they were matches -> Calls a method on controller class to check if the player won.
  
### Step 4:
- JSON object that will hold the paths to a folder holding all card image files
