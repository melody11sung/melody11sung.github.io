---
layout: post
title:  "ML Ch3. Decision Tree Learning"
categories: [ML4T]
author_profile: true
sidebar_main: true
---

# "Machine Learning" by Tom M. Mitchell (1997)
## Chapter 13. Reinforcement Learning

1. Overview
- Reinforcement Learning (RL) is a type of machine learning where an agent learns to make decisions by performing actions and receiving feedback in the form of rewards or penalties. The goal is to learn a policy that maximizes the cumulative reward.

2. Key Concepts
- Agent and Environment: The agent interacts with the environment, which provides feedback in the form of rewards. The environment's response to actions is typically modeled as a Markov Decision Process (MDP).
- Rewards and States: The agent receives rewards as a result of actions taken in specific states. The state space can be discrete (finite) or continuous (infinite).
- Policy: A policy is a strategy used by the agent, defined as a mapping from states to actions. The optimal policy maximizes long-term rewards.
- Value Function: Represents the expected return (reward) for each state, under a particular policy. The value function helps in evaluating how good a state is under a certain policy.
- Q-Function: Represents the value of taking a particular action in a given state. Q-learning, a popular RL algorithm, uses this function to update policies based on a reward received after an action.

3. Algorithms
- Dynamic Programming: Used for problems with a known MDP. It involves iterative calculation of the value functions (e.g., value iteration and policy iteration).
- Monte Carlo Methods: Used when the model dynamics are unknown. These methods estimate value functions based on sample returns from episodes.
- Temporal Difference Learning (TD): Combines ideas from Monte Carlo methods and dynamic programming. It updates estimates based on the estimated values of subsequent states rather than waiting until the end of an episode.
- Q-Learning: A form of TD learning that directly approximates the Q-function, which is independent of the policy being followed. It is off-policy, meaning it can learn the optimal policy irrespective of the agent's actions.

4. Exploration vs. Exploitation
- Exploration involves trying new actions to discover their rewards.
- Exploitation involves choosing known actions that yield high rewards. Balancing these two is crucial for effective learning.

5. Practical Applications
- RL has been applied in various fields including robotics, automated trading, game playing, and more.

6. Challenges and Considerations
- Credit Assignment Problem: Determining which actions to credit for a particular outcome.
- Curse of Dimensionality: Handling large state or action spaces efficiently.
- Trade-off between Exploration and Exploitation: Requires careful tuning to ensure the agent explores enough to learn about the environment but exploits its knowledge to maximize returns.
