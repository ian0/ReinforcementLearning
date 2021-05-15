 #mdp 
 ## Policy Iteration
 
 **Policy iteration** includes: **policy evaluation** + **policy improvement**, and the two are repeated iteratively until policy converges.
 
 In **policy iteration** algorithms, you start with a random policy, then find the value function of that policy (policy evaluation step), then find a new (improved) policy based on the previous value function, and so on. In this process, each policy is guaranteed to be a strict improvement over the previous one (unless it is already optimal). Given a policy, its [[Value Function]] can be obtained using the [[Bellman Equation]].
 
 
 How to Improve a Policy

![[policy-iteration.png]]

In the diagram below, we do policy evaluation on the up arrows, and policy improvement on the down arrows.

![[policy-iteration-1.png]]

We can say one policy is better than another if the value function for a particular policy is strictly better than the other policy.  This gives a partial ordering over states.




#### Policy Evaluation

[[Dynamic Programming]] [[Policy]]

#### Iterative Policy Evaluation
How to figure out the value of the current policy, iterate the [[Bellman Equation]] again and again, feeding the value back into itself, look ahead one step,  and figure out what th new value is at every state.  This process allows us to figure out how much reward we will get at any state.

- At each iteration k + 1
- For all states s ∈ S
- Update v k+1 (s) from v k (s 0 )
- where s' is a successor state of s

An example is evaluating a random policy in a gridworld.