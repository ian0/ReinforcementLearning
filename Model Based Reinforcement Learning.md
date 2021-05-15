#DynamicProgramming

## Model Based Reinforcement Learning

Methods from Dynamic Programming such as [[Policy Iteration]] and [[Value Iteration]] are known as Model Based Methods

They require a complete model of the environment in order to learn optimal policies.  
A complete model

-   Set of all states (S)
-   Set of all actions (A)
-   Transition probabilities (T)
-   Rewards (R)

To qualify as a model  based learning the agent uses the model's predicted value of the next state or reward to determine the opti,iu, actions.  In dynamic programming, the model provides state transition probabilities and reawar for every state action pair.

Another way to say that is:

Model based reinforcement learning algorithms takes the state action reward tupples  and sends them to a model learner, which learns the transitions and rewards.

Those transition and rewards, once they have been learned by an algorithim like Value Iteration can be used to spit out  a optimal value function. And once you have the optimal value function, you can take the argmax of the state that you are in, you can choose which action you should take in any given state and that gives you the policy.

its alternative is [[Model Free Reinforcement Learning]]

