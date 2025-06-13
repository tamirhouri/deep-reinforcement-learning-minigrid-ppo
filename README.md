# Deep Reinforcement Learning - MiniGrid with PPO & Dueling DQN

A comprehensive implementation of deep reinforcement learning algorithms (PPO and Dueling DQN) applied to MiniGrid multi-room navigation environments.

## Project Overview

This project demonstrates the application of advanced reinforcement learning techniques to solve navigation tasks in partially observable grid-world environments. The agent must learn to navigate through multiple connected rooms to reach a goal, requiring exploration, memory, and strategic planning.

## Features

- **Multiple RL Algorithms**: Implementation of Proximal Policy Optimization (PPO) and Dueling Deep Q-Network (DDQN)
- **Progressive Difficulty**: Three environment sizes - Small (N2-S4), Medium (N4-S5), and Large (N6)
- **Partial Observability**: Agents only see the current room, adding complexity to navigation
- **Comprehensive Evaluation**: Statistical analysis and performance metrics

## Architecture

### Algorithms

1. **Proximal Policy Optimization (PPO)**
   - Actor-Critic architecture with policy clipping
   - Convolutional feature extractor for image observations
   - Suitable for continuous learning and policy optimization

2. **Dueling Deep Q-Network (DDQN)**
   - Separates state value and advantage estimation
   - Frame stacking for temporal information
   - Experience replay for stable learning

### Environments

- **MiniGrid-MultiRoom-N2-S4-v0**: Small environment (2 rooms)
- **MiniGrid-MultiRoom-N4-S5-v0**: Medium environment (4 rooms)
- **MiniGrid-MultiRoom-N6-v0**: Large environment (6 rooms)

## Results

Both algorithms successfully learn to navigate the MiniGrid environments:

- **PPO**: Achieves ~65% success rate on large environments
- **Dueling DQN**: Achieves ~63% success rate on large environments
- **Average Steps**: 40-50 steps to reach goal

### Key Components
- Feature extraction using CNN layers
- Layer normalization for stable training
- Experience replay buffer (DQN)
- GAE (Generalized Advantage Estimation) for PPO

## References

- [MiniGrid Documentation](https://minigrid.farama.org/)
- [Gymnasium](https://gymnasium.farama.org/)
- [PPO Paper](https://arxiv.org/abs/1707.06347)
- [Dueling DQN Paper](https://arxiv.org/abs/1511.06581)
