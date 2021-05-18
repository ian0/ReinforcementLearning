#GameTheory 
## Agent Cooperation

[[Game Theory]]

The [[Prisioners Dilema]] with rational agents and Nash Equilibrium offers a bleak outlook for interaction and doesn't explain any of the cooperative strategies that emerge in nature.

How then can agents start to exhibit cooperative strategies?

#### The Spatial Prisoner's Dilemma
Spatial clustering was an idea introduced by Martin Novak and Robert May.  Spatial clustering introduced an element of social networking as they identified that, typically, agents don't interact with all their peers all the time. Instead, agents are much more likely to interact with their neighbours.  They defined a peer group by stating that agents exist on a grid and only interact with other agents close to that grid.  

This spatial clustering demonstrated that the emergence of cooperation was tied to agents interacting within a social network. The social network was also crucial in successfully maintaining cooperation among agents.  

Novak also looked at adapting the payoff matrix from the [[Prisioners Dilema]] and identified thresholds above and below which agents tended to cooperate or defect.  They determined a parameter *b* to characterizes the advantage of defectors against cooperators.  

1. if b < 1.8 then only Cooperation clusters can keep growing
2. if b > 2 then only defector clusters can keep growing
3. if 1.8 < b < 2 then both clusters can keep growing.

#### Tag Mediated Interactions
Around 2005 Rick Riolo introduced Tag Mediated Interactions which are an abstract representation of Martin Novak's spatial dilemma.  Much like the patches worn by a motorcycle gang, the Tag's indicate some shared interests or bond.  The presence of similar tags increases the probability of cooperation, as they demonstrate a level of shared interest. In this way, the tags are an abstract representation of underlying social and tribal principles.  

Riolio demonstrated that the probability of two agents interacting is equal to one minus the difference in their tag values, so if they have very different tag values, they're highly unlikely to interact, and if their tags are the same, they are guaranteed to interact.  

The percentage of agents cooperating was directly related to how the overall agent population was divided into tagged sub-groups.  If the tagged populations are consistent within their subgroups, then cooperation increases, and the group grows.  


#### Tag Group Size
Later work demonstrated that rather than a probabilistic distribution, tags can be given whole number values.  The level of cooperation is then directly proportional to the Tag Group size.  Allowing the tags to mutate saw a dramatic reduction in cooperation.  