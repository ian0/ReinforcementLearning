#ModelFree

## Model Free Reinforcement Learning
[[Reinforcement Learning]]

So, what if we don't don't know all the states and rewards in an environment?  Thats where Model Free learning comes in.

There are two main types,
1. Monte-Carlo Learning
2. Temporal-Differerence Learning

If someone gives us a policy model free environment, how do we evaluate that policy to determine how much reward will be returned by following that policy.  We'll call this model-free prediction.
Once we can evaluate a policy in this enviroment, we can these use ideas to find the optimal value function and hence the optimal policy for that unknown mdp.

[[Q-Learning]]
