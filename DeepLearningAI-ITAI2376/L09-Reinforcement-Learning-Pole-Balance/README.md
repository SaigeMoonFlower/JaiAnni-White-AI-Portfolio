# ITAI 2376 — Module 09 Lab: RL Foundations (CartPole Q-Learning Agent)

## Problem Statement
This project explores the fundamentals of Reinforcement Learning (RL) using the CartPole-v1 environment. The goal is to understand how an agent learns to balance a pole through trial and error using Q-Learning, and how this learning process connects to modern AI systems like RLHF used in large language models.

The lab demonstrates:
- A random agent that fails immediately
- A Q-Learning agent that improves over time
- The impact of exploration vs exploitation
- How RL concepts connect to real-world AI agents

---

## Approach and Methodology
The project follows a structured reinforcement learning workflow:

### 1. Environment Setup
We use the Gymnasium CartPole-v1 environment where an agent must balance a pole on a moving cart.

### 2. Random Agent Baseline
A random agent selects actions without learning. This establishes a performance baseline and demonstrates failure without training.

### 3. Q-Learning Implementation
A Q-Learning agent is implemented with:
- State discretization (binning continuous values)
- Q-table initialization
- Epsilon-greedy action selection
- Reward-based Q-value updates
- Epsilon decay for reducing exploration over time

### 4. Training Process
The agent is trained over 500 episodes while tracking:
- Episode scores
- Learning curve progression
- Exploration rate (epsilon decay)

### 5. Exploration Experiment
Two additional agents are trained with different epsilon decay rates to compare:
- Fast decay (less exploration)
- Slow decay (more exploration)

### 6. Analysis
Performance is evaluated using:
- Rolling average reward
- Comparison to random agent baseline
- Visualization of learning behavior

---

## Results and Evaluation
- The random agent performs poorly, averaging ~25 steps per episode.
- The Q-Learning agent shows gradual improvement but remains unstable.
- Exploration rate strongly impacts performance:
  - Fast decay learns quickly but plateaus
  - Slow decay explores more but learns slower
  - Medium decay performs best overall
- The agent does not fully converge to optimal performance, showing the limitations of simple Q-Learning for continuous environments.

Key insight:
Balanced exploration and exploitation is critical for learning success.

---

## Learning Outcomes
Through this lab, the following concepts were reinforced:

- How reinforcement learning loops function in practice
- The role of reward signals in shaping behavior
- Exploration vs exploitation tradeoffs
- Why Q-Learning struggles with high-dimensional problems
- How RL connects directly to RLHF in modern LLMs
- Why scalable models like LLMs are needed for complex real-world tasks

