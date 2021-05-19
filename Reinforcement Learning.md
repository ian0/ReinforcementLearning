## Reinforcement Learning Fundamentals

#### could also be called reward maximisation

### Introduction
Reinforcement learning provides the capacity for us not only to teach an artificial agent how to act, but to allow it to learn through it’s own interactions with an environment.

By combining the complex representations that deep neural networks can learn with the goal-driven learning of an RL agent, computers have accomplished some amazing feats, like beating humans at over a dozen Atari games and defeating the Go world champion.

> Artificial Intelligence = Reinforcement Learning + Deep Learning - David Silver (2016)

Reinforcement Learning are the classes of algorithms that enables computers to experiment continually in a simulated environment and teach themselves how to act in most optimal way possible.

It is based on a simple idea that an "agent" when reinforced with reward on performing a good action will try to take actions that will maximises the future reward.

How is it different from supervised learning setup?

1.  In supervised learning, the goal is to learn a mapping from inputs to output labels, but in reinforcement Learning it is to learn a 'policy' that defines how agent will act in the given environment.
2.  RL algorithm are capable of multistep decision making i.e. perform a series of actions but supervised algorithms are capable of only single step prediction problem.
3.  RL algorithms do not need huge amount of human labelled data like supervised learning algorithm, and are guided by the reward signal provided by the environment.


## Markov Decision Processes
[[Markov Decision Process]]

## Planning by Dynamic Programming
[[Dynamic Programming]]

Here we describe the standard problem setup of reinforcement learning.

## Temporal Difference Learning
[[Temporal Difference]]


## Environment

![[environment.png]]

### [[State]]

### [[Action]]

### [[Reward]]

### [[Agent]]

### [[Policy]]

### [[Value Function]]

### [[State Transition Function]]

### [[Curse of Dimensionality]]

### [[Exploration vs Exploitation]]

### [[On-Policy vs Off-Policy]]

### [[Value-based vs Policy-based]]

### [[Taxonomy]]

### [[Deep Reinforcement Learning]]

### [[Game Theory]]

### [[Multi-Agent Systems]]

### Model

Model is the representation of how the agent thinks the environment works. It consists of:




