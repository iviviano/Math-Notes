I will be presenting about my project on comparing continuum and particle-based chemical models.

# Outline
Start with the motivation and an overview of physical aspects of the problem

Talk about the differences between the models and the implementation details including the numerical method

We will show some results


# Motivation
For any model, interesting to ask what approximations are worth making
- sort of a cost-benefit analysis in terms of computational efficiency and simplicity vs accuracy tradeoffs

In chemical modeling, we have the physical reality of quantum mechanics
But quantum modeling is too expensive for most interesting system sizes
Classical particle-based modeling is more feasible, but still expensive as systems get large

We are interested in the question: 
When we are analyzing bulk properties, when is modeling the continuum limit reasonable?

<div style="page-break-after: always;"></div>

# Diffusion
This entropic process is characterized by spontaneous reduction in a chemical concentration gradient over time

Here, we have two figure depicting
on the left, continuum diffusion
on the right, atomistic diffusion

In both we see a centrally concentrated initial condition diffusing towards the uniform equilibrium


# Phase Separation
This is the spontaneous separation of a two-component mixture into pure regions

We write $[A]$ and $[B]$ for the concentrations of each component
We use a concentration scale where $A$ and $B$ are between 0 and 1

Generally, the sum of concentrations is unity

Define the order parameter as the difference in concentration functions
Pure $A$ corresponds to order 1 and pure $B$ corresponds to order $-1$
Note that there is only one degree of freedom and this is a convenient way to express that

We are using the spinodal decomposition model for phase separation
- Any initial perturbation is unstable and leads to growth
contrast to nucleation
- random fluctuations about 0
- threshold for phase separation to begin 
- Nucleation-random fluctuation allows local order parameter reaches critical value, it becomes unstable and grows

<div style="page-break-after: always;"></div>

# Modeling Approaches
Our atomistic model is molecular dynamics
It simulates the dynamics of a collection of classical particles
Dynamics come from approximations of the inter-particle forces
We generate a time-discretized trajectory of each particle

Our continuum model is differential equations
The order parameter fully describes the system
We assume a certain regularity of $u$
The dynamics come from a differential equation in $u$
We approximate the differential equation by discretizing time and space


# Model Type Comparison
To compare continuum and atomistic models, 
we estimate the order parameter from the molecular dynamics trajectories

We do this for an MD timestep by
dividing the spatial domain into a uniform grid
the distribution of particles is proportional to the number of atoms in each bin

For diffusion, the order parameter is exactly this distribution function
For phase separation, the order parameter is the difference between the distribution functions of the two components


<div style="page-break-after: always;"></div>

# Leonard-Jones Potential
We use the Leonard-Jones potential to model interparticle interactions

The energy for two particles at distance $r$ from each other is given by the sum of a repulsion term and an attraction term
At close distances, repulsion dominates, and at moderate distances, attraction dominates

This allows it to efficiently and accurately model London Dispersion forces

The model has two parameters
$\sigma$ is the interparticle distance where the interaction is $0$
and $\epsilon$ is the maximum depth of the well

Since the potential quickly approaches its 0 asymptote, it is common to implement interactions with a long-range cutoff
so atoms farther apart than the critical distance are modeled as non-interacting


# Leonard-Jones Fluid
For the full MD system, the potential is the sum of the pairwise potentials over all pairs of particles

For diffusion, we choose a one-component system representing Argon gas
We use experimentally determined parameter values and standard state conditions, simulating diffusion into a vacuum

For phase separation, we have a two component system
The components are equal in quantity
We set the Leonard-Jones parameters to facilitate phase separation
The interactions between like particles are much stronger than the interactions between different particles which causes pure phases to be more stable


<div style="page-break-after: always;"></div>

# LAMMPS 
We run MD simulations with LAMMPS
This open-source software is maintained by the national labs

It implements various different dynamics integrators and is compatible with analysis software

The user specifies the interparticle interactions and initial state and it generates the trajectories

From MD trajectories, we can extract physical parameters and state functions describing the system

MD has the unique capacity of complete state variable control


# Gradient Flow
Onto the continuum model with differential equations
We will model three differential equations, each of which can be viewed as a gradient flow.

The form of such an equation is that the derivative of the order parameter with respect to time is proportional to the negative gradient of some energy function over a hilbert space

We see that for any solution $u$ to a gradient flow equation, the energy is non-increasing in time.
Using the functional chain rule, we have $\frac{d}{dt}F$ as this inner product, and the definition of the differential equation gives a negative norm squared which is non-positive.


<div style="page-break-after: always;"></div>

# Energy Functionals
We have an energy functional for each physical process

The diffusion energy functional has an entropic justification
We integrate the gradient squared over the spatial domain $\Omega$
This causes larger concentration gradients to be higher in energy

The phase energy functional also has the diffusion term, since diffusive dynamics are present in any fluid
It has an additional term $\psi$, which accounts for the energy of phases

Generally, these functionals are constructed from physical principles
The function spaces we differentiate them over are chosen so that the resulting differential equations have certain physical or mathematical properties


# Double Well Potential
The phase energy function $\psi$ is a double-well potential energy function
In our models, we use this specific form as a symmetric fourth-order polynomial

We write its derivative as $\phi$

In the graph of $\psi$, we note the minima at -1 and 1. 
These are the values of the order parameter that correspond to pure phases
Since there are no other minima and the derivative is monotonic between -1 and 1, the pure phases are energetically stable


<div style="page-break-after: always;"></div>

# Derivation of the Heat Equation
We now derive the heat equation from the diffusion energy functional.
To compute the gradient of the functional at the point $u$, we look at its value at a small linear perturbation

1. We write $F_{d}(u+\epsilon v)$ as a norm squared
2. The norm of a sum identity
3. The first term is the norm squared of grad u, which is just $F_{d}(u)$
4. similarly, the last term is $\epsilon^{2}F_{d}(v)$
5. Finally, use integration by parts to write the inner product of gradients with a negative laplacian on the first factor
6. This holds when grad $u$ is periodic, so we add this as a boundary condition to the model

We then use the $L^{2}$ association to see the gradient of $F$ at $u$ as negative laplacian $u$


# Heat Equation
This gives the heat equation as the gradient flow of $F$

We denote the spatial domain $\Omega=$ the unit cube in $d$ dimensions.

We have a periodic boundary condition for $u$ and its first order derivatives.

We also have an initial spatial condition

The constant $D$ scaling the negative gradient is called the diffusion coefficient and it describes the rate of diffusion for real substances


<div style="page-break-after: always;"></div>

# Allen-Cahn Equation
Our first phase separation equation is the Allen-Cahn equation
It is derived similarly to the heat equation as the gradient flow of the phase energy functional over $L^{2}$

We have the same periodic boundary conditions with the order parameter and its derivatives being periodic

Here, the constant $\gamma$ is phenomenological
In the $\mathcal{C}^{2}$ solutions to the differential equation, there is a finite distance between pure regions in the steady state solution
$\gamma$ models the size of this distance


# Cahn-Hilliard Equation
The Cahn-Hilliard equation is our second continuum model for phase separation
It is the gradient flow of the phase energy functional over the Sobolev space $H^{-1}$

Here, we have introduced a generalized chemical potential $\mu$
Since one of its terms is the derivative of the free energy, it is consistent with the classical chemical potential

This equation is fourth-order, so it requires additional boundary conditions
We now have periodicity of $u$ and $\mu$ and their first-order derivatives

Again, $\gamma$ serves the same function as in the Allen-Cahn equation
The parameter $M$ is a phenomenological mobility coefficient


<div style="page-break-after: always;"></div>

# Differential Equation to Difference Equation
Numerically solving these differential equations requires translating them to a discrete problem

For the domain, we divide space into $N^{d}$ uniform rectangles
Here is what the one dimensional case of the unit interval looks like

We choose a finite timestep $k$ and approximate the order parameter by the sequence $u_{j}^{n}$

We discretize the differential operators as well
For the time partial derivative, we use a forward difference
and for the spatial second derivative, we use a central difference


# Our Difference Schemes
Using the discretization procedure, we can write a difference equation for each differential equation
- we replace the order parameter with its approximation and the differential operators with their discrete analogues

This defines an iterative algorithm for approximating $u$


# Difference Scheme Stability
We want to know under what conditions the difference scheme will be stable
One formulation of stability comes from the discrete fourier transform

Writing $u_{j}^{n}$ this way, we say the scheme is stable if the amplitude of every Fourier mode is non-increasing in time

These figures depict a stable numerical solution on the right and an unstable solution on the left for the same initial data
The oscillations display typical high frequency instability


<div style="page-break-after: always;"></div>

# Heat Equation Difference Scheme Stability
To see the stability of the heat equation forward difference scheme,
we need to understand how the discrete laplacian acts on Fourier space

Computing its value at each point in the sequence $u_{j}^{n}$, we see that differentiation in the space domain corresponds to multiplication by an amplification factor $\lambda_{m}$ in the frequency domain



# Heat Equation Difference Scheme Stability
This allows us to write the difference scheme in Fourier space

So, the stability condition that the amplitudes are non-increasing is equivalent to this factor $1+k \lambda_{m}$ being bounded by 1

Using the bounds for $\sin^{2}$, we see that this holds whenever $k$ is less than or equal to a critical value of $\frac{h^{2}}{2}$

So, the forward difference scheme for the heat equation is conditionally stable


# Stability of Nonlinear Schemes
This stability analysis relies on the Fourier transform being a linear operator
For the nonlinear Allen-Cahn and Cahn-Hilliard equations, it won't work
We can however do it for the linearized difference equations
Linearizing about 1 and -1, we have these stability conditions

Numerical results suggest that the linear conditions are reasonable estimates for the critical k values of the nonlinear equations
Here we have a simulation of the nonlinear Allen-Cahn equation that demonstrates this. 
We start with the same initial data
On the left, the timestep is at $k_{crit}$ and on the right it is just above

Notice how the right scheme exhibits numerical instability while the left does not seem to
It is reasonable that the stability of the linearized equations about -1 and 1 reflect the nonlinear stability since pure phases are stable equilibria


# Diffusion of Argon
Onto some results
Here is a LAMMPS simulation of Argon diffusion
Again, we used experimentally determined values of the Leonard-Jones parameters
700 particles are used here and the thermodynamic variables are near standard state

The simulation starts with particles concentrated in the center
As time progresses, they diffuse into the surrounding vacuum


# Fitted Difference Results
On the top row, we have used the procedure I described earlier for estimating the order parameter from the MD simulation you just saw
We then fit this estimated order parameter to the differential equation to approximate the diffusion coefficient

On the bottom row, we are solving the heat equation with the estimated diffusion coefficient and a continuous analogue of the initial condition

Playing the results, we can see how well the rates of diffusion agree


# LAMMPS Simulation of Phase Separation
We use a two-component Leonard-Jones fluid to simulate phase separation
Here is a system of 30000 particles
We are using a dimensionless unit system, but the relative energies of the potential wells are shown

The simulation starts with a uniform random distribution of particles
We see thin regions of pure phases form quickly and their thickness increases with time


# Next Steps
Our next step is to perform the same fitting procedure to this simulation that was done with the diffusion results using both Allen-Cahn and Cahn-Hilliard models

