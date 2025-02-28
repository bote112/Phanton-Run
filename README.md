# Phantom-Run

## Description
Phantom-Run is a multi-level game where the objective is to complete each level as quickly as possible. What makes this game unique is that every level contains a puzzle that can be solved in a single attempt. However, the optimal way to solve it involves using a **"Ghost Run"**—a ghost version of the player from a previous attempt that can take on some of the tasks instead of the player.

In essence, the player controls two characters simultaneously and must figure out how to divide tasks between them to complete the level more efficiently.

### How It Works
For example, imagine a level where there is a button on the left side and the finish point on the right side. The button must be pressed to open the path to the finish line.

- **First Attempt:** The player moves left, presses the button, then heads to the finish.
- **Second Attempt:** The ghost from the first attempt presses the button, allowing the player to go directly to the finish line, minimizing the completion time.

## Technical Specifications
- **Development Platform:** Windows 11
- **Initial Version:** 5.4.4 (Updated to 5.5.1 due to an error)
- **Storage Requirement:** ~5GB
- **Additional Packages:** None required
- **Internet Connection:** Not needed
- **Save Data Size:** Varies based on different SaveGame blueprints
- **Total Save Files:** Up to 9 files (each level has 2 save files: one for best time, one for ghost data, plus separate save/load files)
- **Maximum Save Data Size:** 9MB

## Thematic Specifications
- **Game Genre:** 3D Platformer, Parkour, Fast-Paced, Puzzle
- **Why This Theme?** Traditional Ghost Run mechanics in other games often feel redundant. This game aims to make Ghost Runs a crucial gameplay element.
- **Completion Time:** ~10-15 minutes
- **Game Mode:** Singleplayer

## Controls
The game is designed for **keyboard and mouse**:
- **Movement:** `WASD`
- **Sprint:** `SHIFT`
- **Crouch:** `CTRL`
- **Change Camera View:** `V`
- **Reset Level:** `R`
- **Pause Game:** `P`
- **Save Game:** `F6`
- **Load Game:** `F7`
- **Look Around:** Mouse movement
- **Dash:** Left Mouse Click

## Custom Classes
Several custom classes have been implemented, primarily for level objects:
- **Button** (activates elements in the level)
- **Gate** (opens/closes based on conditions)
- **Finish** (marks level completion)
- **Platform** (various types of moving/static platforms)
- **Splines** (path-following mechanics for objects)

### Level Design
- Levels are created using the **Cube Grid tool** in **Modeling Mode**.

### Save System
There are **three save classes**:
1. **Best Time Save:** Records the fastest time for a level.
2. **Ghost Data Save:** Stores player movements to replay them as a ghost.
3. **Game Progress Save:** Stores the player's current level for save/load functionality.

### Game Mode Functions
The game mode class defines **five core functions**:
- **Save Function** (stores game state)
- **Load Function** (retrieves game state)
- **Record Function** (logs player movements for ghost playback)
- **Replay Function** (executes ghost movement from a previous run)
- **Ghost Spawn Function** (creates the ghost entity based on saved data)

---
## How to Play
1. Complete a level normally on your first attempt.
2. On the second attempt, use your **ghost's previous actions** to optimize your run.
3. Find the best way to **split tasks between you and your ghost** for the fastest completion time.

