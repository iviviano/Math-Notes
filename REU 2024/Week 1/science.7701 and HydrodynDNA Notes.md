>[!def]
>A *free draining* polymer: A model for polymer molecules in solution that are not well approximated by a solid particle. In this model the polymer is considered as a string of beads through which the solvent streams during viscous flow.

worm-like chain model describes polymer behavior: https://en.wikipedia.org/wiki/Worm-like_chain#Stretching_worm-like_chain_polymers. This gives multiple expressions for the force on the chain, with varying levels of accuracy

>[!note]
>The persistence length $A$ or $P$ is a constant that depends on the polymer 

>[!question]
Wiki for worm-like chain gives (1) in terms of the contour length, but says that the contour length is the maximum stretch length. Does this mean that $L$ in the paper refers to the maximum stretch length as well?

I assume hydrodynamic drag is the same as the force $F$ in (1) - only external force?
- I think this would be true at equilibrium, since $F$ is the force required to stretch to $x$.





Extremely unsatisfying model:
approximate continuum worm-like chain by chain of balls and springs so we can use molecular dynamics
- encode the drag stretching force as a tension spread out over each ball
- encode the elastic restoring force as pairwise interactions between adjacent balls

How do I make sure total chain length is constant?
- encode the drag stretching force as a tension spread out over each ball
- encode the elastic restoring force as restoring force spread over each ball
- fix the distance between each adjacent pair of balls
	- or just make them stiff springs

Model they used:
- ball and springs representation of polymer
- adjacent balls pulled together by the polymer restoring force
	- requires a slight modification of the restoring force equation due to the extra flexibility this introduces
- drag on each ball comes from explicit drag at point plus the affects of the drag on other balls
	- how hydrodynamic interactions are handled

>[!note]
>Handles tension force indirectly through the restoring spring forces

>[!question]
>Is the total potential energy the sum of the individual ball potentials?