## Reinforcement Learning Fundamentals

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

Here we describe the standard problem setup of reinforcement learning.

## Environment

### State

State s is representation of a location in the environment. It contains data that is used by RL algorithm.

### Action

Action a is the possible response that could be performed while the agent is at any state. Agent's actions affects the subsequent data it receives.

### Reward

Reward r is a scalar feedback provided by the environment after a particular action is taken in a given state. The total reward that the agent receives is delayed and not instantaneous.

The agent can prioritise over immediate or future reward. The return Rt\=∑k\=0∞γkrt+k is the discounted, accumulated reward with the discount factor γ ∈ (0, 1\]. Discount factor γ=0 means agent is very short sighted whereas γ=1 means the agent is very careful about future possible rewards.

The agent aims to maximize the expectation of such long term return from each state.

### Agent

A RL agent interacts with the environment over time. It's job is to maximise total future reward as it performs different actions and lands in different state. It may include one or more of these components:

### Policy

Policy is agent's behaviour function, represented as π(a|s). It is essentially a map from state to action. The goal of RL is to learn the policy which maximises the reward (optimal policy).

### Value Function

The value function is prediction of expected future reward. Value function is used to evaluate how good or bad a state or state-action pair is.

### Model

Model is the representation of how the agent thinks the environment works. It consists of:

### State Transition Function

State transition function$ $P(s_{t+1}|s_{t},a_{t})$ models the dynamics of the environment. It predicts the next state, given current state and action taken.

Reward function $R(s,a)$ predicts the next immediate reward given current state and action taken.

RL algorithms are categorized as[[Model Free Reinforcement Learning]] and [[Model Based Reinforcement Learning]]. Model Based algorithms use predefined or approximated state transition function and reward functions to figure out its policy. Model free algorithms don't figure out how the environment works, but use their experience to maintain a value function.

To sum it up, at each timestep t the agent is on a state st, it performs action at by following a policy π(at|st), then receives a scalar reward rt according to reward function R(s,a) and transitions to next state st+1 according to state transition probability P(st+1|st,at).

## Markov Decision Processes
[[Markov Decision Process]]

## Reinforcement Learning Ojective

$$maximizeπEat∼π(⋅∣st)st+1∼p(⋅∣st,at)\[∑t\=0∞γtr(st,at)\]$$

### The Value function
$V^π(s)$ is the state-value function of MDP (Markov Decision Process). It's the expected return starting from state s following policy π.

Gt is the total DISCOUNTED reward from time step t, as opposed to Rt which is an immediate return. Here you are taking the expectation of ALL actions according to the policy π.

### The Q function
Qπ(s,a) is the action-value function. It is the expected return starting from state s, following policy π, taking action a. It's focusing on the particular action at the particular state.

The relationship between Qπ and Vπ (the value of being in that state) is

You sum every action-value multiplied by the probability to take that action (the policy π(a∣s))

### When to use V and Q
Q-values are a great way to the make actions explicit so you can deal with problems where the transition function is not available (model-free). However, when your action-space is large, things are not so nice and Q-values are not so convenient. They are harder to compute in spaces with a huge number of actions or even continuous action-spaces.

From a sampling perspective, the dimensionality of Q(s,a) is higher than V(s) so it might get harder to get enough (s,a) samples in comparison with (s). If you have access to the transition function sometimes V is good.

There are also other uses where both are combined, for example [Actor-Critic](https://publish.obsidian.md/parasdahal/Actor-Critic) architectures.