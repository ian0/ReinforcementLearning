#DynamicProgramming 

## Value Iteration

[[Value Function]]

1. Initialise values of all states V(i) to 0
2. Set discount rate to 0.9
3. For every state perform the Bellman update rule

$$\Large V_{0} = max_{a \in 1..N}(r_{a} + \gamma V_{a})$$

5. Repeat step 2 for a large number of
steps/episodes (~200)

#### Value Iteration algorithm

![[value-iteration-algo.png]]


Summary

- Works for Finite MDPs
- The complete environmental model must be present (S, A, T, R)
- Computationally intensive
- Really only practical as a learning exercise.

Forms the basis for [[Q-Learning]]