# Teaching-a-Pirate-to-Find-Treasure-with-Deep-Q-Learning
# CS 370 – Pirate Intelligent Agent (Deep Q-Learning)

# Project overview 

This project is a small “treasure hunt” game. A pirate agent learns to navigate an 8×8 maze and reach the treasure using deep Q-learning (neural networks + experience replay + ε-greedy exploration).

## Given (unchanged):

TreasureMaze.py – the environment (grid, rewards, valid moves, win/lose rules)

GameExperience.py – the replay buffer that stores transitions and builds training targets

## What I built (in the notebook):

The Q-Training Algorithm: a Keras model that predicts Q(s, a), a training loop that plays many games, stores experiences, samples mini-batches, computes targets, and trains the model

Simple logging (loss, steps, win rate) and a completion check to verify the learned policy from multiple starting cells

Result: after training, the pirate reliably reaches the treasure and passes the completion check.

## Reflection

What do computer scientists do and why does it matter?
We turn fuzzy goals into reliable systems. Here the goal “make the pirate find treasure” became a clear setup (states, actions, rewards) and a solution that works. This same process—define, build, measure, iterate—shows up across software, AI, and real products.

How do I approach a problem as a computer scientist?
Start with constraints (don’t change the .py files; use RL). Break the work into parts (model, replay, action selection, training loop, evaluation). Instrument it (track win rate and steps). Keep it as simple as possible, then improve based on evidence.

What are my ethical responsibilities to the end user and the organization?
Be honest about results (evaluate without randomness when reporting). Build for reliability (respect environment rules). Credit ideas appropriately. Follow course policies and keep code you share safe and clean (no secrets, no private data).

## How to run

Open the notebook in Jupyter.

Run the cells in order: define the maze, build the model, train, run the completion check, and play one game from (0, 0).

You should see the win rate climb and the final plot show the pirate’s path to the treasure.

