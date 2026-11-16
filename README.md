# Prototype 4 – Gameplay Mechanics

## Overview

A Unity 3D arcade-style sumo battle game developed as part of the **Create with Code Live – Spring 2020** course. The objective is to knock increasingly challenging waves of enemies off a floating island while using temporary power-ups to gain an advantage.

The project focuses on implementing gameplay mechanics that add depth and challenge to a game, including enemy AI, physics-based interactions, temporary power-ups, random spawning, and progressive enemy waves.

## Features

- **Player Movement:** Implemented physics-based movement using Rigidbody forces and camera-relative directional controls.
- **Camera Controls:** Created a rotating camera system using a focal point and parent-child GameObject relationships.
- **Enemy AI:** Developed enemy behavior that uses directional vectors and Rigidbody forces to pursue the player.
- **Enemy Waves:** Implemented a wave-based spawning system that progressively increases the number of enemies.
- **Power-Up System:** Created a temporary power-up that repels nearby enemies using an increased force.
- **Power-Up Timer:** Used coroutines to manage power-up duration and countdowns.
- **Random Spawning:** Implemented randomized enemy and power-up spawn positions.
- **Physics Interactions:** Applied Physics Materials to create bouncy collisions between objects.
- **Enemy Tracking:** Implemented enemy counting to determine when a wave is completed and the next one can begin.
- **Power-Up Indicator:** Used GameObject activation and deactivation to visually indicate when the power-up is active.

## What I Learned & Implemented

### Player Movement and Camera Controls
- Applied texture wrapping to game objects.
- Used parent-child relationships to attach the Main Camera to a focal point, allowing the camera to rotate around the player.
- Implemented camera rotation using the horizontal input axis.
- Used the vertical input axis and `Rigidbody.AddForce()` to control player movement relative to the camera's forward direction.
- Worked with local XYZ coordinates to transform objects relative to their parent GameObjects.

### Enemy AI and Physics
- Created an enemy controller script that uses `Rigidbody.AddForce()` to make enemies pursue the player.
- Calculated directional vectors by subtracting the enemy's position from the player's position.
- Used vector normalization (`Vector3.normalized`) to maintain consistent enemy movement speed regardless of the distance to the player.
- Implemented a customizable speed variable to control enemy movement.
- Applied Physics Materials to modify collision behavior and make objects bounce upon impact.

### Power-Up Mechanics
- Implemented a power-up that activates when the player collides with it.
- Used directional vectors and `Rigidbody.AddForce()` with `ForceMode.Impulse` to repel enemies away from the player.
- Added a customizable force multiplier to control the power-up's knockback strength.
- Used `IEnumerator`, coroutines, and `WaitForSeconds()` to manage the power-up's temporary duration.
- Applied `SetActive()` to display and hide the power-up indicator depending on the power-up's activation state.

### Enemy Waves and Spawning Systems
- Used `Random.Range()` to generate randomized spawn positions along two axes.
- Created separate private functions to organize random position generation and improve code readability.
- Implemented `for` loops to spawn multiple enemies based on the current wave count.
- Incremented integer variables to progressively increase the number of enemies in each wave.
- Used `FindObjectsOfType()` to locate active enemy objects and determine how many remained in the scene.
- Used the `.Length` property to retrieve the number of elements in an array.
- Implemented enemy-count checks to determine when all enemies had been defeated and the next wave could begin.

### Debugging and Code Organization
- Used string concatenation and variables to create informative debug messages.
- Organized gameplay logic into custom functions and private variables to improve code readability and maintainability.

## Technologies & Tools

- **Game Engine:** Unity
- **Programming Language:** C#
- **IDE:** Visual Studio
- **Concepts:** Rigidbody Physics, Vector Mathematics, Vector Normalization, Enemy AI, Camera Controls, Physics Materials, Power-Ups, Coroutines, IEnumerators, Randomization, Object Spawning, For Loops, Object Detection, Wave-Based Progression

## Course

**Create with Code Live – Spring 2020**

A remote Unity course taught by professionals working at Unity, focused on learning game development and programming through hands-on projects.
