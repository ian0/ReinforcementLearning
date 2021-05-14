#mdp 

[[Markov Decision Process]]

### Policy

- Formally a policy is a mapping from states to the probability of selecting each possible action.
- It is given by the symbol π
- With ε – greedy you choose greedy actions most of the time save for a small percentage where you choose a non-greedy action.
- Combining this action selection strategy, with the value estimates, we get a policy
- π* is known as the optimal policy

*Definition*

A policy π is a distribution over actions given states,

$π(a|s) = P[A_{t} = a | S_{t} = s]$

- A policy fully defines the behaviour of an agent
- MDP policies depend on the current state (not the history)
 - i.e. Policies are stationary (time-independent),
$A_{t} ∼ π(·|S_{t} ), ∀_{t} > 0$

#### Greedy Policy
- A greedy action selection strategy always exploits current knowledge. It won’t try other actions in the hope that they may be better (exploration)

####  ε-greedy
= Choose highest valued reward most of the time save for a small number of times when you choose an exploratory action
- ε 10% to 15%




### Optimal Policy

so, how do we define that one policy is better than another policy?

![[optimal-policy.png]]

Finding an Optimal Policy

![[find-optimal-policy.png]]

Direct correlation between the value estimate and the policy being followed!

[[Policy Evaluation]]

[[Policy Iteration]]









