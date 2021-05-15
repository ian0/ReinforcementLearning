#DynamicProgramming 

## Value Iteration

[[Dynamic Programming]]

The goal of Value Iteration is to find a policy that maximizes the [[Value Function]]:

In **value iteration**, you start with any  initialised value function, for example set V(s) = 0 for all s in S.  Then iterate to find a new and improved improved value function, assuming that the agent takes the best possible action in that state under the current estimate of the value function, until you reach an optimal value function. This optimal value functional is the one that  finds the maximium final reward.  

Value iIteration visits all states in states in the statesspace, 

1. Initialise values of all states V(i) to some number, say 0
2. Set discount rate to some value, say 0.9
3. For every state perform the Bellman update rule

$$\Large V_{0} = max_{a \in 1..N}(r_{a} + \gamma V_{a})$$

4. Calcute a delata, the change in the Value Function for that state
5. repeat until delta is below some value

Once you have found the optimal value function, you can then derive the optimal policy $\pi*$ for the optimal value function. This process is based on the _optimality Bellman operator_.

Value iteration is an example of [[Model Based Reinforcement Learning]]

 
