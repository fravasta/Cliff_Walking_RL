# Cliff Walking: From Bellman’s Equation to SARSA and Q-Learning

This project explores the **Cliff Walking problem** using **Temporal Difference (TD) learning algorithms**, specifically **SARSA** (on-policy) and **Q-Learning** (off-policy). 
It includes a Python implementation of the environment and the two algorithms, as well as a comparative analysis of their performance.

## Project Overview

The goal is to teach an agent how to navigate a grid-world environment safely and efficiently, avoiding a "cliff" that leads to heavy penalties. 
This classic reinforcement learning (RL) problem demonstrates the practical differences between on-policy and off-policy learning strategies.

The work was originally presented as part of a Master's course in Data Science.

## Algorithms

### SARSA (State-Action-Reward-State-Action)
- **On-policy** algorithm
- Learns the value of the policy being followed
- More conservative (avoids risky paths near the cliff)
- Slower convergence, but more stable

### Q-Learning
- **Off-policy** algorithm
- Learns the value of the optimal policy regardless of agent's behavior
- More aggressive (takes the shortest path, even near the cliff)
- Faster convergence, but potentially unstable

---

## Experiments & Key Features

- **Epsilon-greedy policy** for balancing exploration and exploitation
- **Epsilon decay** to encourage early exploration and late-stage exploitation
- **Comparison metrics**:
  - Reward trends
  - Convergence speed
  - Path optimality
- **Special case**: Both algorithms converge to the same solution under 100% greedy policy


## 📊 Results

| Algorithm | Convergence Speed | Stability | Path Safety |
|----------|-------------------|-----------|-------------|
| SARSA    | Slower            | High      | Safe        |
| Q-Learning | Faster          | Moderate  | Risky       |

Q-Learning achieves higher immediate rewards but at the risk of falling off the cliff. 
SARSA is more cautious, resulting in fewer penalties but longer paths.
