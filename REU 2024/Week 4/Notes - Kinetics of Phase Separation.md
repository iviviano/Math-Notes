Notes to [[Kinetics of phase decomposition processes  numerical solutions to Cahn Hilliard equation.pdf]]

Physical Experiment:
- Model phase separation of an alloy (cooled below a critical temperature)

Free energy of the system $\psi$ has the double well shape. 
>[!def]
>*Spinodal region*: where $\psi''<0$: $$(u_{a}^{s},u_{b}^{s})$$

>[!def]
>*Binodal region*: where the supporting tangent touches the $\psi$. For our symmetrical $\psi$, this is the region between its global mimima: $$(u_{a},u_{b})$$

The spinodal region is unstable: perturbations about the mean composition reduce the overall free energy. The system separates into two phases with concentrations $u_{a}$ and $u_{b}$. 

Outside the binodal region, the system is stable.

In the binodal but outside the spinodal region, the system is metastable. Small perturbations increase free energy and decay in time. However, large fluctuations can spark nucleation.

Use this form of the equation: $$\frac{\partial u}{\partial t}=M\nabla^{2}[\psi'(u)-\gamma\nabla^{2}u]$$
The linearization about the average concentration $u_{m}$ is $$\frac{\partial u}{\partial t}=M \psi''(u_{m})\nabla^{2}[u-\gamma\nabla^{2}u]$$
$$u=u_{m}+u_{p}$$
$$\frac{\partial u_{m}}{\partial t}+\frac{\partial u_{p}}{\partial t}=M\nabla^{2}[\phi'(u_{m}+u_{p})-\gamma\nabla^{2}(u_{m}-u_{p})]$$


For the linear equation in the spinodal region, small wavelengths grow exponentially in time.

>[!note]
>Without loss of generality, we may only consider double well potentials of the form $$\psi(u)=\frac{\alpha}{4}(u^{2}-\beta^{2})^{2}$$since any other potential can be transformed into the equation with a potential of this type

We use $$\psi(u)=\frac{1}{4}(u^{2}-1)^{2}$$
The total energy of the system: $$F(u)=\int_{\Omega}\underbrace{\psi(u)}_{\text{free}}+ \underbrace{\frac{\gamma}{2}|\nabla u|^{2}}_{\text{boundary}}d \omega$$
We see that the total energy decreases with time: $$\frac{dF}{dt}<0$$





find $a^{n}$ from $u^{n}$ with ifft (and $b^{n}?$) 
easy to show that the discrete laplacian satisfies the relationship they give
Just need to solve the linear equation in (5) and use fft to get $u^{n+1}$

