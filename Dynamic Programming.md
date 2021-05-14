#DynamicProgramming

[[Reinforcement Learning]] [[Markov Decision Process]]

## Dynamic Programming

*Sections*
- [[Policy Evaluation]]
- [[Policy Iteration]]
 - [[Value Iteration]]
- [[Extensions to Dynamic Programming]]

Both Policy Iteration and Value Iteration are control problems, and both tell you have to get the maximium reward from the mdp.

### What is Dynamic Programming?

Why is called Dynamic Programming?

dynamic - sequential or stepwise
Programming in this case refers to a policy, its a tems from maths - 
so its an optimisation method for solving complex sequential problems.

It solves them by breaking them down into subproblems
- Solve the subproblems
- Combine solutions to subproblems

Example: find the shortest path, can be broken into two pieces, find start to mid, find mid to end and combine.

Subproblems recur many times
solutions can be cached and reused

[[Markov Decision Process]] satisfy both properties
- [[Bellman Equation]] gives recursive decomposition
- [[Value Function]] stores and resuses solutions

We can use Dynamic Programming to evaluate a policy, and then in an inner loop use this evaluation to find the optimal policy.  This evaluation is alos called planning.

Planning by Dynamic Programming - We know everything about the MDP

![[planning.png]]

Dynamic programming is used to solve:
- Scheduling and Graph algorithms (e.g. shortest path algorithms) and Graphical models (e.g. Viterbi algorithm)

Methods from Dynamic Programming such as Policy Iteration and Value Iteration are known as Model Based Methods  [[Model Based Reinforcement Learning]]


Summary of DP Algorithms

![[sync-dynamic-prog.png]]

For large state spaces, Dynamic programming suffers from the [[Curse of Dimensionality]]

