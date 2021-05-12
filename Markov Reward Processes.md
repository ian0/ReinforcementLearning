#mdp

## Markov Reward Processes

[[Markov Decision Process]]

A Markov reward process is a [[Markov Process]] or Markov Chain with an associated reward function.

*Definition*

A Markov Reward Process is a tuple $\langle S, P, R, \gamma\rangle$
- $S$ is a finite set of states
- $P$ is a state transition probability matrix,
$P_{ss'} = P[S_{t+1} = s' | S_{t} = s]$
- $R$ is a reward function, $R_{s} = E[R_{t+1} | S_{t} = s]$
- $\gamma$ a discount factor, $\gamma \in [0, 1]$

### Return
*Definition*

![[return.png]]


*Why discount?*

Most Markov reward and decision processes are discounted. Why?
- Mathematically convenient to discount rewards
- Avoids infinite returns in cyclic Markov processes
- Uncertainty about the future may not be fully represented
- If the reward is financial, immediate rewards may earn more
interest than delayed rewards
- Animal/human behaviour shows preference for immediate
reward
- It is sometimes possible to use undiscounted Markov reward
processes (i.e. γ = 1), e.g. if all sequences terminate.


Once we have the MDP, a policy can be learned by doing Value Iteration or Policy Iteration.

Note: Soft Markov Property

Examples of application of MDPs:

1.  Robot navigation problem
2.  Inventory management
3.  Portfolio optimization
4.  Purchase and production optimization

### Value Function
The value function $v(s)$ gives the long-term value of state $s$

*Definition*
The state value function $v(s)$ of an MRP is the expected return
starting from state s

 	$v(s) = E [G_{t} | S_{t} = s]$
	
	
### [[Bellman Equation]] for MRP's

The value function can be decomposed into two parts:

- The immediate reward you get from being where you are $R_{t+1}$
- The value of reward from that timestep onwards.  This is called the discounted value of successor state $\gamma v (S_{t+1})$ and is all the future reqard

Valuse function is the expected return if you start in a particular state, s.

$v(s) = E [G_{t} | S_{t} = s]$

$= E[R_{t+1} + \gamma R_{t+2} + {\gamma}^2R_{t+3} + ... | S_{t} = s]$
$= E[R_{t+1} + \gamma R_{t+2} + {\gamma}R_{t+3} + ... | S_{t} = s]$
$= E[R_{t+1} + \gamma G_{t+1} | S_{t} = s]$

Value function is the expected immediate reward plus the value function of the next state
$= E[R_{t+1} + \gamma v(S_{t+1}) | S_{t} = s]$