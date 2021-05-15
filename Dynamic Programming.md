#DynamicProgramming

[[Reinforcement Learning]] [[Markov Decision Process]]

## Dynamic Programming

### What is Dynamic Programming?

Why is called Dynamic Programming?

dynamic - sequential or stepwise
Programming in this case refers to a policy, its a tems from maths - 
so its an optimisation method for solving complex sequential problems.

It solves problems by breaking them down into subproblems
- Solve the subproblems
- Combine solutions to subproblems

Example: find the shortest path, can be broken into two pieces, find start to mid, find mid to end and combine.

Subproblems recur many times, so solutions can be cached and reused

DP uses an explicit model. DP requires that you know $p(s′,r|s,a)$. The update rule for DP is the first [[Bellman Equation]] equation turned into an update rule:

$$v_{k+1}(s) = {max}_{a} \sum\__{s',r} p(s',r|s,a)(r + \gamma v_{k}(s'))$$



There are two main methods of Dynamic Programming, [[Policy iteration]] and [[Value Iteration]]

In **Policy Iteration** \- You randomly select a policy and find [[Value Function]] corresponding to it , then find a new (improved) policy based on the previous value function, and so on this will lead to optimal policy .

In **Value Iteration** \- You randomly select a [[Value Function]] , then find a new (improved) value function in an iterative process, until reaching the optimal value function , then derive optimal policy from that optimal value function .

Both Policy Iteration and Value Iteration are control problems, and both tell you have to get the maximium reward from the mdp.

We can view the algorithms side by side:

![[Policy-vsValue-iter.png]]





