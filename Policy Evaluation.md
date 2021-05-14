#DynamicProgramming 
## Policy Evaluation

[[Dynamic Programming]] [[Policy]]

#### Iterative Policy Evaluation
How to figure out the value of the current policy, iterate the [[Bellman Equation]] again and again, feeding the value back into itself, look ahead one step,  and figure out what th new value is at every state.  This process allows us to figure out how much reward we will get at any state.

- At each iteration k + 1
- For all states s ∈ S
- Update v k+1 (s) from v k (s 0 )
- where s' is a successor state of s

An example is evaluating a random policy in a gridworld.