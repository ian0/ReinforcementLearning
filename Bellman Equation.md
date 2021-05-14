#mdp 
[[Markov Reward Processes]]

### Bellman Equation

The Bellman Equation is the fundamental equation that defines the true value of being in a particular state.

There are a few increments of this, the Bellman expectation equation for example.  The

### Bellman Optimally Equation 

- Bellman Optimality Equation is non-linear
- No closed form solution (in general)
- Many iterative solution methods
	- Value Iteration
	- Policy Iteration
	- Q-learning
	- Sarsa

for $v_{*}$ show the optimal values.

Use one step look ahead

Look at the value of each of the actions you can take, and take the max of them, and that will tell you how good it is to be in a particular state.

![[bellman-optimal.png]]

Bellman Optimality Equation for $Q∗$

![[optimal-bellman-q.png]]

We can put these two pieces together, you get a recursive relationship that relates $v_{**}$ to itself, which we can solve

see 126mins https://www.youtube.com/watch?v=lfHX2hHRMVQ&t=780s

![[bellman-opt-v2.png]]

![[bellman-opt-q2.png]]

![[student-mdp.png]]

