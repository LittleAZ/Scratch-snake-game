# Scratch-snake-game
My first Scratch game (CS50 Week 0)
This is my first programming project, built with Scratch.

# Scratch Snake Game
This is my first programming project, built with Scratch.

# How to Play
Download the `.sb3` file and open it in Scratch.
Press any arrow key to start the game.

## Features & Implementation
### 1. Food Detection
Food is considered eaten when the head touches the food.

### 2. Food Respawn
At the start of the game and whenever food is eaten, it moves to a random position within a defined range.

### 3. Path Following (Instead of Direct Tracking)
The snake does not physically follow the head.
Instead, the head’s x and y coordinates are stored in lists.
Each body segment moves to a previous position from the list.

### 4. Score, Levels, and Win Condition
* Score increases by 1 when food is eaten
* Score = 5 → switch to level 2
* Score = 10 → switch to level 3
* Score = 15 → win the game
When switching levels:
* Head and body reset to (0, 0)
* Head moves to top layer
* Body becomes invisible (to prevent accidental collision)

### 5. Prevent Reverse Movement
A variable `direction` is used.
The snake cannot move directly in the opposite direction.

### 6. Prevent Instant Turning (Anti Self-Collision)
A timer is added:
* Reset on game start, turning, or level change
* Turning is only allowed if the timer > 0.5s
* This slightly affects control responsiveness but improves stability

### 7. Snake Growth
All body segments always follow the path but remain invisible.
They become visible as the score increases.

### 8. Self-Collision
Body segments only appear after:
* Score condition is met
* Head has moved enough steps (list length ≥ 20)
If the head touches the body → game over

## ⏱️ Development Time
About 10 hours

## 🧠 Notes
This is my first project, and many parts required debugging and experimentation, especially synchronization and collision handling.
