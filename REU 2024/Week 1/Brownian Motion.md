Special case of Langevin dynamics:
- mimics the viscous aspect of the solvent
- not full implicit solvent. missing
	- electrostatic screening
	- hydrophobic effect
Langevin Equation: $$MX''=-\nabla U(X)-\gamma MX'+\sqrt{sM \gamma k_{b}T}R(t)$$
This incorporates Newtonian mechanics: mass times acceleration is $(MX'')$ and the force is the derivative of potential energy ($-\nabla U(X)$). 

There is a damping term $(-\gamma MX')$ where the constant $\gamma$ is the collision frequency.

[[Monte Carlo]] is introduced with $R$. This is a stationary (time independent) Gaussian process that satisfies $$\begin{align*}
&\langle R(t)\rangle=0\\
&\langle R(t)\cdot R(t')\rangle=\delta(t-t')
\end{align*}$$
where $\delta$ is the [[Dirac delta]]. 


In the large damping/zero average acceleration limit, we get Brownian dynamics: $$\dot X= - \frac{D}{k_{b}T}\nabla U(X)+\sqrt{2D}R(t)$$
where we have changed the constants to the diffusion constant $D$.



Hydrodynamic Interactions
- Continuum solvent described by Navier-Stokes equation


Simulate Brownian motion with [[Metropolis Hastings Algorithm]]. We use $R$ as our proposal distribution (symmetric because gaussian). We use the potential energy function $U$ as the target distribution (or should we use total energy with Boltzmann distribution?).
- when does the potential energy function correspond to the density of states?
- is the ergodic hypothesis sufficient?

difference from [[Hamiltonian Monte Carlo]]: only randomly perturbing momentum each iteration instead of randomly assigning it?