#ModelFree 

## Q-Learning

[[Model Free Reinforcement Learning]]

The easiest way to explain q-learning is to do so in the context of an example.  For this description we will use the frozen lake example as we implemented that previously.

![[lake.png]]

Imagine we have a 5 by 5 grid with 25 different states.  The agent can freely navigate this environment by taking one of the following 4 actions: up, down, left, right.  The agent is constrained to take one move per episode.  In this example the agent starts in in the top left corner, in position (0,0) on the gird.  It's goal is to reach the bottom right square (4, 4) without falling into any of the holes, as doing so kills the agent and terminates the game.  In the game, every time the agent takes an action it receives a reward which can be positive, negative or zero depedning on the rules of the game.  In this exmple, the agent receives a reward of +10 for reaching the goal, -5 for falling in a hole and -1 for every action.

We can record the actions the agent takes in a q-table, whch contains the coordinates of each state along with a value for the action taken.

For each state action pair, we want to model the expected long term reward.

$$Q(S, A) = E(R)$$

Given some state $s_{t}$ and action $a_{t}$ we can say the expected value of taking that action in that state is the sum of all the rewards in the following states.

$$Q(s_{t}, a_{t}) = r_{t+1} + \gamma r_{t+2} + \gamma r_{t+3} + ...$$

We can add a discounting factor, gamma ($\gamma$) to the future reward.  The discouting factor allows us to weigh the delayed reward.  If gamma is close to zero than we are effectively disregarding the future reward and only looking forward one step.  If gamma is close to 1 then we have "far sighted " evaluation of reward.

If we consider the reward from the next state, at t+1,

$$Q(s_{t+1}, a_{t+1}) = r_{t+2} + \gamma r_{t+3} + \gamma r_{t+4} + ...$$

we can see that we can write the first state value in tems of the next state value:

$$Q(s_{t}, a_{t}) = r_{t+1} + \gamma \, Q(s_{t+1}, a_{t+1})$$

As we are looking for the optimium policy, the one that returns the maximium reward, we can say that we are looking for the action that returns the maximium value for a particular state, so we can re-write the formula as 

$$Q(s_{t}, a_{t}) = r_{t+1} + \gamma \, max_{a} Q(s_{t+1})$$

As the agent will be moving through the environment, we want to improve the Q value at each state based on the prvvious state at a learning rate, alpha ($\alpha$).  So the equation becomes:

$$Q(S, A) \leftarrow Q(S, A) + \alpha [R + \gamma max_{a} Q(S', a) - Q(S, A)] $$

Where $S'$ stands for the next state.

The only thing missing from the above is that we don't always want to take the action that returns the maximium value, sometme we want it to take a random action to encourage exploration.  This is called an $e-greedy$ policy.











