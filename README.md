# FrozenLake Q-Learning

## Introduction

This project explores Reinforcement Learning (RL) by implementing a Q-learning agent in the FrozenLake environment using Gymnasium.

The goal is to train an agent to navigate a frozen grid, avoid holes, and reach the goal. The project explores how an agent learns through interaction with an environment and rewards.

## Project Overview

FrozenLake is a grid-based environment where an agent moves across icy tiles to reach a goal while avoiding holes. In this project, `is_slippery=True`, meaning the agent may not move in the intended direction because the surface is slippery.

Q-learning is a model-free reinforcement learning algorithm that learns action values for different states. These values are stored in a Q-table and used to select actions.

## Methodology

1. **Environment Setup:** Create the FrozenLake environment using Gymnasium.
2. **Q-table Initialization:** Initialize a Q-table with zeros for all state-action pairs.
3. **Epsilon-Greedy Policy:** Balance exploration and exploitation when selecting actions.
4. **Training:** Train the agent over multiple episodes.
5. **Q-table Update:** Update action values using the Q-learning update rule.
6. **Evaluation:** Evaluate the learned policy and measure its success rate.

## Training Configuration

| Parameter | Value |
|---|---:|
| Training episodes | 2,000 |
| Learning rate (alpha) | 0.1 |
| Discount factor (gamma) | 0.99 |
| Initial epsilon | 1.0 |
| Epsilon decay | 0.001 |
| Environment | FrozenLake-v1 |
| Slippery surface | True |

Epsilon decreases by a fixed amount after each episode until it reaches zero. The agent initially explores different actions and gradually relies on the learned Q-table.

## Results

The trained agent achieved a **75.3% success rate** over 1,000 evaluation episodes in one recorded evaluation run.

The notebook also includes:
- A Q-table showing learned action values.
- A plot of episode returns during training.
- A plot showing epsilon decay.
- A visualization of the FrozenLake environment.

Because the environment is slippery and involves randomness, evaluation results may vary between runs.

## Libraries and Tools

- Python
- Google Colab
- Gymnasium
- NumPy
- Pandas
- Matplotlib

## How to Run

1. Open the notebook in Google Colab.
2. Run the package installation and import cells.
3. Run the environment setup and training cells in order.
4. Review the Q-table and training plots.
5. Run the evaluation cells to measure the agent's success rate.

## Learning Outcomes

Through this project, I explored:
- The fundamentals of reinforcement learning.
- How Q-learning updates action values.
- How the epsilon-greedy policy balances exploration and exploitation.
- How training parameters and environment randomness can affect performance.

## Acknowledgements and Source

This project is based on a starter notebook provided as part of a workshop.

The original notebook structure and learning materials were provided by **[Imperial College London Workshop 2024/ Introduction to RL and Frozen Lake / Organised by ProEd]**. I used the provided notebook as a starting point to implement, configure, run, and evaluate the Q-learning experiment.
