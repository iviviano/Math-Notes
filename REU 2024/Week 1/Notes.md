Experiment:
- Phase separation of polymers (coacervation)
- Two types of polymers start out mixed and separate spatially over time
	- may not separate cleanly
- solvent: water with a salt
	- how does the salt affect the phase separation
	- concentration and compound

Cahn-Hilliard equation describes phase separation

Approaches:
- Monte Carlo
	- find ground state
	- study equilibrium processes
- Molecular Dynamics - modeling system with Newtonian mechanics
	- time dependency
	- can tell us about transitions between states which are local ground states
- Dissipative Particle Dynamics??
	- abstract and introduction of fluids thing

Efficiency of Molecular Dynamics:
- Course graining
	- instead of looking at atoms, look at a bead which represents a set of molecules (Brownian dynamics - first order differential equation, implicit solvent model)


TODO:
Look at
- [[Brownian Motion]] wiki
- LAMMPS 
Read:
- [[ermak-mccammon-78.pdf]]
- [[science.7701345.pdf]] - candidate for simulation
	- LAMMPS or HOOMD-Blue
Chat GPT:
- generating lammps code with LLMs https://nanohub.org/resources/39045?r=nl77
MEET Office at 5pm on Friday

average kinetic energy in 3 dimensions: $$\langle E\rangle= \frac{3}{2}kT$$
so, the total dimensionless kinetic energy of the balls: $$\frac{N\langle E\rangle}{kT}=\frac{3}{2}N$$
but, does the solvent temperature matter?


Use this approximation: (Ermack and McCammon): $$X(t+\Delta t)=X(t)+ \Delta t D\cdot \frac{F(X(t))}{kT}+R(t)$$
Then, $R$ is a Gaussian noise vector with zero mean and standard deviation $\sqrt{sD \Delta t}$ in each entry

Times step: $$\Delta t>>m_{i} D/kT$$
