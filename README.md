# Decompile APK Game

This is an Android application featuring a simple game where players must follow a sequence of directions to win. The sequence is generated based on an input ID and additional data retrieved from a server.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [MenuActivity](#MenuActivity)
- [GameActivity](#GameActivity)
- [example](#example)

## Features

- Simple and intuitive game interface.
- Dynamic sequence generation based on input ID.
- Data fetching from a server to enhance game logic.
- Visual feedback for user actions.
- Toast messages indicating success or failure.

# Usage

Launch the app on your Android device.
Enter a valid EXTRA_ID in the input field.
Press the "Start" button to begin the game.
Follow the sequence of directions displayed on the screen to win the game.
Game Logic

# MenuActivity
The MenuActivity is the entry point of the application. It includes the following key components:

UI Elements: A TextInputEditText for entering the ID and a MaterialButton to start the game.
Server Call: Fetches data from a server using the URL specified in the string resources.
Start Game: Starts the GameActivity with the provided ID and a state derived from the server data.
# GameActivity
The GameActivity handles the game logic. It includes the following key components:

Direction Sequence Generation: Generates a sequence of directions based on the input ID.
User Interaction: Allows the user to click on direction buttons (left, right, up, down) to follow the sequence.
Winning Condition: Checks if the user's clicks match the generated sequence to determine success or failure.
# Sequence of Directions
The sequence of directions is determined by the EXTRA_ID string passed to the GameActivity. Each character in the EXTRA_ID string is converted to an integer and taken modulo 4 to determine the direction:

0: Left
1: Right
2: Up
3: Down
For example, given an EXTRA_ID of "318701869", the sequence of directions would be:

Down (3)
Right (1)
Left (0)
Down (3)
Left (0)
Right (1)
Left (0)
Up (2)
Right (1)
The player must follow this sequence to win the game.

# example 
For example, given an EXTRA_ID of 221345678, the sequence of directions would be:

Up (2)
Up (2)
Right (1)
Down (3)
Left (0)
Right (1)
Up (2)
Down (3)
Left (0)

![Screenshot_2024-07-09-00-37-19-978_com example deompileapk](https://github.com/ahmadzhalka/DeompileAPK/assets/119360009/1dba550f-8e2f-440d-81d1-0d8186ca6908)



