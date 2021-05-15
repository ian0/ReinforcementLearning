## Deep Q-Networks

[[Deep Reinforcement Learning]] [[Q-Learning]]

As mentioned in the [[Deep Reinforcement Learning]] page, Tabular [[Q-Learning]] struggles when the count of obserable states is very large.

We want to identify the important states and maybe cluster states with minimal differences together.

### Function Approximation
As the state space is so large, we want to infer what the likley value a state would be even if we haven't/don't visit it.  We want to use the values from neighbouring states to help do this.  We'll make use of a deep neural network to estimate the Q-values for each state-action pair in a given environment, and in turn, the network will approximate the optimal Q-function.  The optimal Q-function will satisfy the Bellman equation.  


The traget network is used to keep a copy of the find Q(s', a') which is need to calculate Q(s, a).  The two networks are synced periodically.  The loss of the network is calculated by comparing the outputted Q-values from the target Q-values using the Bellman equation. The objective is to minimize this loss.

After the loss is calculated, the weights within the network are updated via Stochastic Gradient Descent and backpropagation. This process is repeated for each state in the environment until a minimium loss value is reached and and we get an approximate optimal Q-function.


#### Non-linear Regression
- Function approximation is similar to regression.
- We want to build a regressor like Stochastic Gradient Descent, using Deep Neural networks, which maps the state and action to a value.
- It’s a popular option, but other non-linear regression techniques will also work


#### SGD for DQN
- Use Stochastic Gradient Descent to train the network, approximating Q(s,a).
- calculate targets using the Bellman equation and “pretend” the problem is a supervised learning one.
- Training data distribution will not be identical to the optimal policy.
- To deal with this, need a replay buffer
	- Simple version is a fixed size buffer, to store state transition samples

The algorithim is:

![[DQN.png]]