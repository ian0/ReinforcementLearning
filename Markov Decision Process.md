#mdp
# Makov Decision Process

Decision Theoretic Mathematical framework for handling uncertainty

![[notes-mdp.png]]

From the course notes:

State Action space formalism
- A finite set of possible world states **S** (Fully/partially observable)
- A discrete set of possible actions within each state **A(s)**
- A real valued reward **R**
- The probability of transitioning between states for a given action **T(s,a)**
- Goal : Find the optimal policy π*


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


[[Value Function]]

[[Policy]]


### When to use V and Q

Q-values are a great way to the make actions explicit so you can deal with problems where the transition function is not available (model-free). However, when your action-space is large, things are not so nice and Q-values are not so convenient. They are harder to compute in spaces with a huge number of actions or even continuous action-spaces.

From a sampling perspective, the dimensionality of Q(s,a) is higher than V(s) so it might get harder to get enough (s,a) samples in comparison with (s). If you have access to the transition function sometimes V is good.

There are also other uses where both are combined, for example [Actor-Critic](https://publish.obsidian.md/parasdahal/Actor-Critic) architectures.

#### POMDPs 
A Partially Observable Markov Decision Process is an MDP with
hidden states. It is a hidden Markov model with actions.