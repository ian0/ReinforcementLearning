#mdp
# Makov Decision Process
[[Reinforcement Learning]]

An MDP is the standard mathematical formalism for describing agent environment interactions and how to model uncertainty.

[[State Action Space Formalism]]


Building Blocks

1. [[Markov Property]]
2. [[Markov Chain]]
3. [[Markov Process]]
4. [[Markov Reward Processes]]

stochastic -> means uncertainty

A Markov decision process (MDP) is a Markov reward process with decisions. It is an environment in which all states are Markov.

It consists of states, rewards, actions and transitions( sometimes called models)

The transition probabiity matrix depends on which action you take.  Where you end up depends on the action you take.  In the descrete case, there is one, seperate matrix of transition probabilities for each action you take.  apart from that, the process is the same as for a [[Markov Reward Processes]], except that now instead of probabilities between states, there are choices:

![[mdp.png]]

The game of the mdp is to find the best path through the decision making process that maximises the sum of rewards.

![[mdp-graph.png]]

To play the game of an mdp, we need to define what it means to take decisions.  To do that we define a [[Policy]]

When we have a perfect model of the environmenr, we can use [[Dynamic Programming]] to compute the optimium [[Policy]]