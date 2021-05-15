## State Transition Function

[[Reinforcement Learning]]

State transition function$ $P(s_{t+1}|s_{t},a_{t})$ models the dynamics of the environment. It predicts the next state, given current state and action taken.

Reward function $R(s,a)$ predicts the next immediate reward given current state and action taken.

RL algorithms are categorized as[[Model Free Reinforcement Learning]] and [[Model Based Reinforcement Learning]]. Model Based algorithms use predefined or approximated state transition function and reward functions to figure out its policy. Model free algorithms don't figure out how the environment works, but use their experience to maintain a value function.

To sum it up, at each timestep t the agent is on a state st, it performs action at by following a policy π(at|st), then receives a scalar reward rt according to reward function R(s,a) and transitions to next state st+1 according to state transition probability P(st+1|st,at).