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


## Results
All in all, the contribution of this project lies in highlighting how different exploration strategies affect the learning behavior of reinforcement learning agents:
- SARSA is preferable for scenarios where the agent is risk-avoidant. Its on-policy nature leads to safer, more conservative paths that prioritize stability over speed.
- Q-Learning is more suitable for scenarios where the agent is a risk-taker, as it aggressively exploits high-reward paths—even when they come with higher risks, like walking close to the cliff.
The essential difference between SARSA and Q-Learning lies in their exploration strategies rather than in their convergence capabilities.
When they adopt the same updating policy (100% greedy) they converge to the same solution

| Algorithm | Convergence Speed | Stability | Path Safety |
|----------|-------------------|-----------|-------------|
| SARSA    | Slower            | High      | Safe        |
| Q-Learning | Faster          | Moderate  | Risky       |

Q-Learning achieves higher immediate rewards but at the risk of falling off the cliff. 
SARSA is more cautious, resulting in fewer penalties but longer paths.
