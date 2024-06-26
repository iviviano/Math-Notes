mass conservation:
- whenever the differential equation takes the form: $$\frac{\partial f}{\partial t}=\nabla^{2}g$$and we have neumann or periodic BC's for $g$, mass is conserved
- whenever the difference equation takes the form: $$\frac{f_{j}^{n+1}-f_{j}^{n}}{k}=\Delta^{h}(g_{j}^{n})$$and we have periodic BC's for $g$, mass is conserved

energy decreasing: how to get $$\frac{dF}{dt}(u)=-\int_{\Omega}|\nabla w|^{2}dx$$
This is equivalent to the differential equation for $u$ having the form $$\frac{\partial u}{\partial t}=M\nabla^{2}w$$
and the heat equation having energy functional $$F(u)=\int_{\Omega}|\nabla u|^{2}dx$$
$$\begin{align*}
\frac{d F}{d t}(u)&= \frac{d}{dt}\int_{\Omega}\psi(u)+ \frac{\gamma}{2}|\nabla u|^{2}\ dx\\
&= \int_{\Omega}\frac{\partial }{\partial t}\psi(u)+ \frac{\gamma}{2} \frac{\partial }{\partial t}\left(\frac{\partial u}{\partial x}\right)^{2}\ dx\quad(1\text{D})\\
&= \int_{\Omega}\psi'(u)\cdot \frac{\partial u}{\partial t}+\gamma\frac{\partial u}{\partial x}\cdot \frac{\partial ^{2}u}{\partial x \partial t}\ dx\\
&= M\int_{\Omega}\psi'(u)\cdot \frac{\partial w}{\partial x^{2}}+\gamma\frac{\partial u}{\partial x}\cdot \frac{\partial ^{2}w}{\partial x^{3}}\ dx\\
\end{align*}$$
$$w=\psi'(u)-\gamma\frac{\partial ^{2}u}{\partial x^{2}}$$

Gradient of the functional: gives best linear approximation of $F$. 

$$\begin{align*}\\
\int_{\Omega}|\nabla u|^{2}dx&= \int_{\Omega}\nabla u\cdot\nabla u\ dx\\
&= \int_{\Omega}\nabla\cdot(u\nabla u)-u\nabla^{2} u\ dx\\
&= 0-\int_{\Omega} u\frac{w-\phi(u)}{\gamma}\ dx\\
&= 
\end{align*}$$



Let $u:\mathbb{R}\rightarrow L^{4}(\mathbb{R}^{d})$ and $F:L^{4}(\mathbb{R}^{d})\rightarrow \mathbb{R}$ be defined by
$$F(u)=\int_{\Omega}\psi(u)+ \frac{\gamma}{2}|\nabla u|^{2}~dx$$
variational minimization gives: $$\psi'(u)-\gamma\nabla^{2}u=0$$
this is the equilibrium [[Allen-Cahn Equation]]

Gradient flow gives a differential equation: $$\frac{\partial u}{\partial t}=\nabla F(u)\overset{?}{=}\frac{\partial }{\partial u}F(u)=...?$$



TODO:
- try $\phi=0$ to get the code working
- work out the gradient of the energy functional for [[Cahn-Hilliard Equation]]

Meet Tuesday at 3