### Value Function

[[Markov Decision Process]]

The value function is prediction of expected future reward. Value function is used to evaluate how good or bad a state or state-action pair is.

- Almost all RL algorithms involve estimating value functions
- Th value functions at a state estimate how good it is to be in that particular state
- How “good”, represents the expected future reward achievable from the current state.
- These future rewards are all obviously dependent on what actions the agent takes subsequent to leaving the state.

*Definition*
The optimal state-value function $v_{∗}(s)$ is the maximum value
function over all policies.  This tells you not what the best policy is, but the maximium reward you can expect from the system

$$\Large v_{∗}(s) = \frac{max}{\pi} v_{π}(s)$$

The optimal action-value function q ∗ (s, a) is the maximum
action-value function over all policies.  given you commit to a particular action, what is the most reward you can collect from that point onwards

$$\Large q_{∗}(s, a) = \frac{max}{\pi} q_{π}(s, a)$$

informally, an mdp is slved when we know this optimal value function

so what we really care about is the optimal [[Policy]] defines what is the best possible way to behavine in an [[Markov Decision Process]]


*State-Value function*
$V_{\pi}(s)$ describes how good is it to be in state s if I'm following policy $\pi$

$E_{\pi}$ is the *expectation* when we sample all actions according to the policy $\pi$

![[state-value-fn.png]]

*Action Value function*
the action value function defines how good is it to take a particular action when we're in a particular state.  This is the one we care about when trying to decide which action to take: choose the one that will generate the most reward.  for a given policy $q_{\pi}$ if I'm in state $s$ and I take action $a$, how much reward will I get from that point onwards

![[action-value-function.png]]
