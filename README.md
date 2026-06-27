# CS 370 Portfolio: Pirate Intelligent Agent

## Project Summary

This project focused on building an intelligent pirate agent for a treasure hunt game. The goal was for the pirate to learn how to navigate an 8x8 maze and reach the treasure using deep Q-learning. The maze included open paths, blocked cells, a starting location, and a treasure location. The agent had to learn which movement actions were most valuable over time so it could find a successful path consistently instead of only winning by chance.

The final implementation successfully trained the pirate agent to solve the maze. The final training run reached a 100% recent win rate at epoch 99, passed the full completion check with a result of `True`, and passed the top-left play test with a result of `True`.

## What Code Was Provided

The starter code included the structure for the treasure hunt game and several helper components. The provided files included `TreasureMaze.py`, which represented the maze environment, and `GameExperience.py`, which stored the agent’s experiences for replay during training.

The notebook also provided the maze layout, movement actions, helper functions for displaying the maze, the `play_game()` function, the `completion_check()` function, and the neural network model structure. The provided code gave the environment, the basic game mechanics, and the framework needed to test whether the agent could reach the treasure.

## What Code I Created

The main code I created was the deep Q-learning training implementation in the `qtrain()` function. This function trained the pirate agent by resetting the maze, choosing random starting positions, selecting actions through exploration and exploitation, storing experiences, training the neural network on replay data, tracking win history, and stopping when the model reached a strong enough win rate and passed validation.

I also added helper logic to improve training reliability. This included checking valid actions, reducing the value of invalid actions, using a target model, applying experience replay, tracking training progress, using early stopping, and adding a warm-start process to help the model learn useful pathfinding behavior more efficiently. These additions helped the agent move from partial learning to consistent maze completion.

## Connection to Computer Science

Computer scientists solve problems by designing, building, testing, and improving computational systems. Their work matters because software and intelligent systems are used in areas such as healthcare, education, transportation, cybersecurity, business, finance, entertainment, and scientific research. In this project, computer science mattered because the goal was not just to write code that ran, but to create an intelligent system that could learn from experience and make better decisions over time.

This project helped me see how artificial intelligence connects to the larger field of computer science. The pirate agent used states, actions, rewards, neural networks, and feedback to learn a path through the maze. These same ideas can apply to larger real-world problems where a system must make a sequence of decisions, evaluate outcomes, and improve its behavior.

## How I Approach Problems as a Computer Scientist

As a computer scientist, I approach problems by first understanding the goal, the inputs, the constraints, and the expected output. For this project, the goal was not simply for the pirate to win one game. The real goal was for the agent to learn a consistent policy that worked across valid starting positions. That meant I needed to test the model carefully and use the `completion_check()` result as the strongest validation measure.

I also learned the importance of debugging and iteration. My final solution required thinking about why a model might appear to perform well during training but still fail during validation. This led me to focus on invalid actions, replay memory, terminal states, exploration and exploitation, and stronger evaluation. This process reflects how computer scientists often work: test, observe, revise, and continue improving until the solution meets the real requirement.

## Ethical Responsibilities

Computer scientists have ethical responsibilities to both end users and organizations. End users deserve systems that are reliable, transparent, fair, secure, and respectful of their needs. Organizations need systems that are accurate, maintainable, and safe to deploy. In an AI project, these responsibilities are especially important because a model can produce results that appear correct even when it has not actually learned the intended behavior.

For this project, ethical responsibility connects to validation and transparency. If this were a real navigation, robotics, or decision-making system, it would not be enough to show one successful example. The system would need to be tested across different conditions so users could trust that it works consistently. It would also be important to explain what the model is designed to do, what its limitations are, and how its performance was evaluated.

## Files Included

* `Rodman_Michael_ProjectTwo.ipynb` — Jupyter Notebook containing the pirate intelligent agent implementation
* `Rodman_Michael_ProjectTwo.pdf` — PDF export showing the completed notebook and final output
* `Rodman_Michael_ProjectTwo.html` — HTML export of the completed notebook
* `Rodman_Michael_ProjectTwo_DesignDefense.docx` — written design defense for the project
