# Q-Learning Grid Simulation

Autonomous agents that learn to navigate a 2D grid to a target position using **Q-learning**, a reinforcement learning algorithm. Built in **Roblox Studio (Luau)** in **2022**.

**Demo:** https://www.youtube.com/watch?v=hm42y6WEwmc

> **Note:** The original source files for this project were lost. This repository documents the project and links to a recovered recording of it running. The commit history reflects when this repo was created, not when the project was built.

## Overview

Each agent starts somewhere on a discrete grid with no knowledge of its environment. Through repeated episodes of trial and error, it learns which action to take in each cell to reach the target (the origin) efficiently. Its decisions are guided only by the rewards it receives.

## How it works

**State:** the agent's current cell on the grid.
**Actions:** move up, down, left, or right.
**Reward:** a custom reward function encourages progress towards the target and penalises inefficient movement.

The agent maintains a **Q-table** that stores an estimated value for every state–action pair. After each move, it updates that estimate using the Q-learning update rule:

```
Q(s, a) ← Q(s, a) + α [ r + γ · max Q(s', a') − Q(s, a) ]
```

- **α (learning rate):** how strongly new experience overrides old estimates
- **γ (discount factor):** how much future rewards matter compared with immediate ones
- **r:** the reward for the move just taken
- **s′:** the state the agent moved into

To balance **exploration vs exploitation**, the agent sometimes takes a random action to discover new paths and otherwise picks the action with the highest Q-value. As training progresses, it relies more and more on what it has learned.

## Features

- Discrete 2D grid environment
- Q-table of state–action values
- Custom reward function (reward shaping)
- Exploration vs exploitation strategy
- Deterministic and stochastic movement modes
- Real-time visualisation of agents learning in Roblox Studio

## Key concepts

- Reinforcement learning (Q-learning)
- State–action value tables
- Exploration vs exploitation
- Reward shaping

## Tech

- **Language:** Luau (Lua)
- **Engine:** Roblox Studio
- **Built:** 2022
