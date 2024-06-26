Applies to spherically symmetric brownian particles and particles with spherically symmetric subunits

>[!question]
>What does the diffusion tensor mean?

Fokker-Planck equation: PDE that describes time evolution of PDE of particle velocity under influence of drag force and random force
- We can obtain this from the coupled Langevin equations by calculating phase space trajectories and then averaging ([[Monte Carlo]])

For the large particles of Brownian Motion, distribution of momenta relaxes to equilibrium much faster than positions
- many collisions with solvent particles
- diffusion regime - time scale much larger than that of momentum relaxation

Given an initial coordinate $\{r_{i}^{0}\}$, we have an initial configuration distribution function $$W(\vec r,0)=\prod_{i}\delta(r_{i}-r_{i}^{0})$$
>[!question]
What does the $\Delta$ on $r_{i}$ mean below? (Average displacement, but how is it calculated)

From Fokker-Planck Description and approximation above, we get that the distribution $W(\vec{ r},\Delta t)$ is the unique multivariate normal distribution satisfying $$\begin{align*}
\langle \Delta r_{i}(\Delta t)\rangle&= \sum_{j} \left(\frac{\partial D_{ij}}{\partial r_{i}}+ \frac{D_{ij}}{kT}F_{j}\right)\Delta t\\
\langle r_{i}(\Delta t)\Delta r_{j}(\Delta t)\rangle&= 2D_{ii}\Delta t\  \delta_{ij}
\end{align*}$$
where the diffusion tensor, its gradient, and the forces are evaluated at the initial configuration.

We get the displacement equation: $$r_{i}=r_{i}^{0}+\sum_{j} \frac{\partial D_{ij}^{0}}{\partial r_{j}}\Delta t+\sum_{j}\frac{D_{ij}^{0}F_{j}^{0}}{kT}\Delta t+R_{i}(\Delta t)$$
where a zero superscript stipulates that the quantity is evaluated at the beginning of the time step. $R_{i}$ is the random Gaussian...

>[!note]
>The diffusion tensor will be diagonal and constant when we neglect hydrodynamic interactions. 

>[!question]
>Does this iterate by setting the new sampled position $r_{i}(\Delta t)$ as the initial position and repeating?

Rigid rod dimer simulation
- perturbation and correction method makes sense
- why is force proportional to delta function?
