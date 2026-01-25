# Number Guessing Game GUI

A Java Swing-based GUI application featuring two interactive number guessing games with different game modes.

## Project Overview

This is an educational project demonstrating Java GUI development using Swing components, binary search algorithms, and event-driven programming. The application provides two distinct game modes where users can play against the computer or have the computer guess against them.

## Features

### Game Modes

1. **Computer vs You**
   - You think of a number between 1-100
   - The computer uses binary search to guess your number
   - You respond with "Higher", "Lower", or "Correct"
   - Game tracks the computer's best score (fewest guesses)

2. **You vs Computer**
   - The computer thinks of a number between 1-100
   - You attempt to guess the number
   - The computer provides hints: "high", "low", or "Correct"
   - Game tracks your best score (fewest guesses)
   - Includes a cheat code: "DataBreach" to reveal the number

### Additional Features

- **Score Tracking**: Displays best scores for both game modes
- **Player Name**: Set your name to personalize the score display
- **Game Rules**: In-game rules display for each game mode
- **Input Validation**: Handles invalid user inputs gracefully with error messages
- **Cheat System**: One-time cheat code in You vs Computer mode

## Project Structure

```
Exam3GUI/
├── src/
│   ├── module-info.java
│   └── exam3GUI/
│       ├── NumberGuessGameGUI.java      # Main GUI frame and game logic
│       ├── ComputerVsUserGame.java      # Computer guessing game implementation
│       ├── UserVsComputerGame.java      # User guessing game implementation
│       └── package-info.java
└── bin/                                  # Compiled bytecode
```

## Classes

### `NumberGuessGameGUI.java`
Main GUI class extending `JFrame` and implementing `ActionListener`. Manages:
- UI layout with GridBagLayout and CardLayout
- Game mode initialization and switching
- Event handling for all buttons
- Score management and display

### `ComputerVsUserGame.java`
Implements the binary search guessing game where:
- Computer makes intelligent guesses using binary search
- Maintains search bounds (lowVal, highVal) and midpoint (midVal)
- Tracks guess count
- Methods: `setNextValues()`, `getCurrentGuessCount()`, `getMidVal()`

### `UserVsComputerGame.java`
Implements the number guessing game where:
- Computer generates random number in specified range
- Provides hints: "high", "low", or "Correct"
- Supports cheat code "DataBreach"
- Methods: `getHints()`, `enterCheatCode()`, `getNumberCheat()`

## Technical Details

- **Java Version**: 21
- **IDE**: Eclipse
- **GUI Framework**: Java Swing (AWT components)
- **Layout Managers**: GridBagLayout, BoxLayout, CardLayout
- **Build Tool**: Eclipse JDT Compiler

## Game Instructions

### Computer vs You
1. Click "Computer versus You"
2. Think of a number 1-100
3. Computer makes a guess
4. Reply "Higher", "Lower", or "Correct"
5. Computer uses your feedback to narrow down the number

### You vs Computer
1. Click "You versus Computer"
2. Computer thinks of a number 1-100
3. Enter your guess
4. Computer responds with feedback
5. Continue guessing until correct
6. **Cheat**: Type "DataBreach" to reveal the number (one-time use)

## Authors

**Project Developers**: Shelten Aguilar, Salvador Lugo  
**Completion Date**: November 13, 2025  
**Course**: CS 131 - Data Structures

## Learning Concepts

This project demonstrates understanding of:
- Object-Oriented Programming (OOP)
- GUI design and event handling
- Binary search algorithm
- String manipulation and input validation
- Exception handling
- Swing component hierarchy and layout management
