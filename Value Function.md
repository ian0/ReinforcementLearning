#mdp 

### Value Function

[[Markov Decision Process]]

*State-Value function*
$V_{\pi}(s)$ describes how good is it to be in state s if I'm following policy $\pi$

$E_{\pi}$ is the *expectation* when we sample all actions according to the policy $\pi$

![[state-value-fn.png]]

*Action Value function*
the action value function defines how good is it to take a particular action when we're in a particular state.  This is the one we care about when trying to decide which action to take: choose the one that will generate the most reward.  for a given policy $q_{\pi}$ if I'm in state $s$ and I take action $a$, how much reward will I get from that point onwards

![[action-value-function.png]]

#### Bellman Expectation Equation

The state-value function can again be decomposed into immediate
reward plus discounted value of successor state,

![[state-valuue-bellman.png]]

The action-value function can similarly be decomposed,

![[state-action-bellman.png]]




