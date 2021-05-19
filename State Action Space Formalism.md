#mdp 

## State Action Space Formalism

[[Markov Decision Process]]

Decision Theoretic Mathematical framework for handling uncertainty

![[notes-mdp.png]]

From the course notes:

![[mdp-description.png]]

State Action Space Formalism
- A finite set of possible world states **S** (Fully/partially observable)
- A discrete set of possible actions within each state **A(s)**
- A real valued reward **R**
- The probability of transitioning between states for a given action **T(s,a)**
- Goal : Find the optimal policy π*

### Real World Example

A state action state formalism is a mapping of a real-world situation into an MDP.
An example is the use of an intelligent thermostat, one that learns a user's pattern of occupancy and can keep a room at the desired temperature based on that occupancy.  Here, the thermostat controls the comfort experienced by the occupants and also affects the energy consumption required to maintain that temperature.  

So there are two conflicting goals identified: minimize energy consumption while maximizing occupant comfort.  We want to create a simulator to speed up training, so we need to identify the parameters within which the thermostat operates.  The room size, number of windows and heat source will all affect the thermostat performance.  For example, a convection heater will heat a room quicker than geothermal underfloor heating and a room with more windows will tend to lose more heat.

Now we have a problem definition, we can map the real-world actors into the MDP.

Choosing a state representation is an important consideration as the state captures what we know at a given time.  In this case, the state space consists of the room temperature, time to occupancy and outside temperature.  The Actions are Heat on, heat off, cool on, cool off. 
The rewards are a function of room occupancy, action and the whether the current room temperature sits within the desired comfort band. The transition probabilities are unknown. 

With these paraments in place, we can run experiments in simulation to determine an optimum policy.