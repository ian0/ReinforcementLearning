Value-based vs Policy-based

[[Reinforcement Learning]]

### Value-Based
[[Value Iteration]], [[Q-Learning]], [[Sarsa]]
You have to specify the explicit kind of exploration strategy for example epsilon-greedy strategy or Boltzmann softmax strategy. Basically, you have your Q-values and you determine the probabilities of actions given those Q-values and any other parameter you want.

The state value function V(s) should estimate the future reward starting in state s. The state-action value function Q(s,a) should estimate the future reward starting in state s and taking action a (this is different because state transitions may be random). These value functions are very useful. We can choose the best action a from state s by picking the one with the value, but do some exploration in the "worse" actions because these are noisy estimates after all. That's the policy, and the estimates Q(s,a) are learned with temporal difference errors.

### Policy Based
Cross-Entropy Method

Policy based methods try to directly approximate the policy of the agent, using a probablility distribution over the available actions.  i.e.

- S1 ({up, 20%}, {down, 30%}, {left, 0%}, {right,50%})

We are not exactly looking for which action is best to transition to some next state, more basic than that, instead learning action sequences leading to goal states.

What the Cross-Entropy method does is take a bunch of inputs, see the outputs that were produced, choose the inputs that have led to the best outputs and tune the Agent till until a satisfactory policy is found.

In practice, the policy is usually represented as a **probability distribution over actions** (that the Agent can take at a given state), which makes it very similar to a classification problem.

*core of the Cross-Entropy method*
 generate batches of episodes, throw away bad episodes in a batch to train the neural network of the Agent on better ones. 
 
 To decide which ones to throw away, use the 70th percentile, ie keep the best 30%.
 
 Train the neural network of the Agent using the remaining , that means the transitions **<_s_,_a_,_r_\>**) from the remaining “elite” episodes, using the state **_s_** as the input and issued actions **_a_** as the label.
 
 repeat until convergence