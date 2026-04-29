# Dodge The Creeps

[![Ask DeepWiki](https://devin.ai/assets/askdeepwiki.png)](https://deepwiki.com/MRdyRy/DodgeTheCreeps)

This repository contains the source code for "Dodge The Creeps," a simple 2D survival game built with the Godot Engine. The objective is to navigate your character and survive for as long as possible by dodging the enemies that spawn from the edges of the screen.

## Gameplay

- Control the player character using the arrow keys.
- Mobs will randomly appear along a defined path and move across the screen.
- Avoid colliding with any of the mobs.
- The game ends when your character is hit.
- Your score increases the longer you survive.
- Press the "Start" button to begin a new game.

## Features

- Responsive player controls for movement in four directions.
- Animated sprites for both the player and the various enemy types.
- A dynamic scoring system that tracks survival time.
- Randomized mob spawning, including different animations ('fly', 'swim', 'walk') and movement vectors.
- A complete game loop with start, game over, and restart functionality.
- An interactive Heads-Up Display (HUD) showing the current score and game state messages.
- Background music and sound effects.

## Project Structure

The game is organized into several key scenes and scripts:

-   **`Main.tscn` (`main.gd`):** The root node of the game. It orchestrates the main game loop, manages timers for score and mob spawning, and handles the `new_game` and `game_over` logic.
-   **`Player.tscn` (`player.gd`):** Defines the player character. This script handles input for movement, updates animations based on direction, and emits a `hit` signal upon collision with a mob.
-   **`Mob.tscn` (`mob.gd`):** Represents an enemy creep. Mobs are `RigidBody2D` nodes that are assigned a random animation and velocity when spawned. They are automatically removed when they leave the screen.
-   **`HUD.tscn` (`hud.gd`):** A `CanvasLayer` that manages all UI elements. It displays the score, shows messages like "Game Over", and contains the "Start" button to initiate a new game.

## How to Run

To run this game, you will need the Godot Engine (version 4.x).

1.  Clone this repository to your local machine:
    ```sh
    git clone https://github.com/mrdyry/dodgethecreeps.git
    ```
2.  Open the Godot Engine Project Manager.
3.  Click the "Import" button and navigate to the cloned repository folder.
4.  Select the `project.godot` file to import the project.
5.  Once imported, select the project and click "Run" (or press F5).

## Controls

-   **Move Up:** `Up Arrow`
-   **Move Down:** `Down Arrow`
-   **Move Left:** `Left Arrow`
-   **Move Right:** `Right Arrow`

## Assets & Credits

-   **Art:** All character and enemy sprites are located in the `art/` directory.
-   **Audio:** Music and sound effects are located in the `art/` directory.
    -   Background Music: `House In a Forest Loop.ogg`
    -   Sound Effect: `gameover.wav`
-   **Font:** The game uses the **Xolonium** font, which is licensed under the SIL Open Font License, Version 1.1. See `fonts/LICENSE.txt` for more details.
