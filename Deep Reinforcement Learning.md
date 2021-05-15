## Deep Reinforcement Learning

[[Reinforcement Learning]]

Combines Deep Neural Networks with a Reinforcement Learning architecture, to learn the best actions possible within in a given task.

Unlike traditional [[Reinforcement Learning]] techniques which use tabular methods to store the state value estimates.  Instead of the tabular method requirement, Deep Reinforcement Learning methods use the Neural Network as a function Approximator or Regressor to hold the value estimates.

One issue with Tabular Methods is the memory requrements to store larger state action spaces.  To get a good approximation of these state action values, a very large number of sample transitions  is required.

For example, for the Atrai 2600 games, with 210x160 pixels, where every pixel has 128 possible clolurs, the total screens is 128^33600.  This would require billions of years on the fastest supercomputer.  This is known as the [[Curse of Dimensionality]]

### Continuous states or actions
In practical terms, due to the precision of sensors, continuous states have to be discretized.  Many control tasks are of this form, robot navigation, driverless vehicles.  Small changes in things like angular velocity will lead to the creation of new state values.  To overcome this, you need to sample neighbouring states to get an estimation of the current state.  

### [[Deep Q-Networks]]