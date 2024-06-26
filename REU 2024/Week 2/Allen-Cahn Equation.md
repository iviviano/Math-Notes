For a two-component fluid, the phase-field variable (roughly the phase concentration) is described by the differential equation
$$\frac{\partial v}{\partial t}=\gamma\nabla^{2}v-f(v)$$

where $\sqrt{\gamma}$ is the interface thickness, and $F\in\mathcal{C}^{1}$ is the double well potential with $F'=f$. We typically use $F(v)= \frac{1}{4}(v^{2}-1)^{2}$, so $f(v)=v^{3}-v$. The equation becomes: $$\frac{\partial v}{\partial t}=\gamma\nabla^{2} v+v-v^{3}$$
Note that $v=0$ describes the interface between phases

For the 1D equation, $$v_{eq}(x,t)=\tanh\left( \frac{x}{\sqrt{2\gamma}}\right)$$is an equilibrium solution. For the 2D equation, $$v_{eq}(x,y,t)=\tanh\left(\frac{x+y}{2\sqrt{\gamma}}\right)$$is an equilibrium solution (the 1D equilibrium also works).

We can linearize AC about the equilibrium solution: https://math.colgate.edu/~wweckesser/math311/handouts/linearization.pdf

1D:
substituting $u=v_{eq}+\epsilon w$ gives
$$\epsilon\frac{\partial w}{\partial t}=\gamma\frac{\partial^{2} }{\partial x^{2}}(v_{eq}+\epsilon w)+v_{eq}+\epsilon w-(v_{eq}+\epsilon w)^{3}$$
$$\epsilon\frac{\partial w}{\partial t}=\gamma\left(\epsilon \frac{\partial ^{2}w}{\partial x^{2}}-\frac{\partial ^{2}v_{eq}}{\partial x^{2}}\right)+v_{eq}+\epsilon w-(v_{eq}+\epsilon w)^{3}$$
Differentiating with respect to $\epsilon$:
$$\frac{\partial w}{\partial t}=\gamma \frac{\partial^{2} w}{\partial x^{2}}+w-3w(v_{eq}+\epsilon w)^{2}$$
Taking the limit as $\epsilon \rightarrow 0$, $$\frac{\partial w}{\partial t}=\gamma\frac{\partial ^{2}}{\partial x^{2}}+w-3w\cdot v_{eq}^{2}$$
$$(v_{eq}+\epsilon w)^{3}=v_{eq}^{3}+3v_{eq}^{2}\epsilon w+3v_{eq}\epsilon^{2}w^{2}+\epsilon^{3}w^{3}$$





$$\frac{\partial v}{\partial t}=v-v^{3}$$



Linearized [[Allen-Cahn Equation]] about $v=1$: $$\frac{\partial v}{\partial t}=\frac{\partial ^{2}v}{\partial x^{2}}+ \frac{1}{\epsilon^{2}}(2-2v)$$
difference equation: $$v_{j}^{n+1}=v_{j}^{n}+ \frac{k}{h^{2}}(v_{j+1}^{n}-2v_{j}^{n}+v_{j-1}^{n})+ \frac{k}{\epsilon^{2}}(2-2v_{j}^{n})$$
We can inductively show that a stability condition holds:
$$\begin{align*}
|v_{j}^{n+1}|&=\left| v_{j}^{n}+ \frac{k}{h^{2}}(v_{j+1}^{n}-2v_{j}^{n}+v_{j-1}^{n})+ \frac{k}{\epsilon^{2}}(2-2v_{j}^{n})\right|\\
&= \left| (1- \frac{2k}{\epsilon^{2}}-2\lambda)v_{j}^{n}+ \lambda(v_{j+1}^{n}+v_{j-1}^{n})+ \frac{2k}{\epsilon^{2}}\right|\\
&\le \left|\underbrace{1- \frac{2k}{\epsilon^{2}}- 2\lambda}_{\ge0}\right|\cdot|v_{j}^{n}|+ \lambda(|v_{j+1}^{n}|+|v_{j-1}^{n}|)+ \frac{2k}{\epsilon^{2}}\\
&\le \left(1- \frac{2k}{\epsilon^{2}}- 2\lambda\right)\cdot\|v^{n}\|_{\infty}+ \lambda(\|v^{n}\|_{\infty}+\|v^{n}\|_{\infty})+ \frac{2k}{\epsilon^{2}}\\
&= \left(1- \frac{2k}{\epsilon^{2}}\right)\cdot\underbrace{\|v^{n}\|_{\infty}}_{\le1}+ \frac{2k}{\epsilon^{2}}\\
&\le 1
\end{align*}$$
if $$1- \frac{2k}{\epsilon^{2}}- \frac{2k}{h^{2}}\ge0\iff2k\left(\frac{1}{\epsilon^{2}}+ \frac{1}{h^{2}}\right)\le1\iff k\le \frac{\epsilon^{2}h^{2}}{2(\epsilon^{2}+h^{2})}$$
In the limit $\epsilon \rightarrow \infty$ (recovering the [[Heat Equation]]), we have stability if $$k\le \frac{h^{2}}{2}\iff \frac{k}{h^{2}}\le \frac{1}{2}$$which is the same sufficient stability condition as the forward difference scheme of the heat equation.

It is easy to show that the same condition holds for the linearization about $v=-1$

Write $$\begin{align*}
v_{j}^{n}&= \sum_{m=0}^{J-1}\alpha_{m}^{n}~e^{2\pi i \frac{mj}{J}}\\
\Delta^{h}v_{j}^{n}&= \sum_{m=0}^{J-1}\alpha_{m}^{n}\lambda_{m}~e^{2\pi i \frac{mj}{J}}\\
\lambda_{m}&= \frac{1}{h^{2}}\left(e^{2\pi i \frac{m}{J}}+e^{-2\pi i \frac{m}{J}}-2\right)=- \frac{4}{h^{2}}\sin^{2} \left(\pi \frac{m}{J}\right)
\end{align*}$$
In conjugate space, we have the following recurrence relation: $$\begin{align*}
\alpha_{0}^{n+1}&= \left(1- \frac{2k}{\epsilon^{2}}\right)\alpha_{m}^{n}+ \frac{2k}{\epsilon^{2}}\\
\alpha_{m}^{n+1}&= \left(\underbrace{1- \frac{2k}{\epsilon^{2}}+k \lambda_{m}}_{A_{m,k}}\right)\alpha_{m}^{n}
\end{align*}$$
We can impose the constraint that amplitudes are non-increasing in time $|\alpha_{m}^{n+1}|\le |\alpha_{m}^{n}|$. For the $m=0$ case, this is satisfied if $|\alpha_{0}^{n}|\le1$. So, this restricts to initial conditions with average value in $[-1,1]$. Since all functions of consideration map into this interval, this condition will be satisfied. For the $m≠0$ case, we need $|A_{m,k}|\le1$. Since $A_{m,k}\le1$, we need $$1- \frac{2k}{\epsilon^{2}}-4 \frac{k}{h^{2}}\sin^{2}\left(\pi \frac{m}{J}\right)\ge-1$$
Using the a-priori bound $|\sin(x)|\le1$, we have $$k\le \frac{h^{2}\epsilon^{2}}{h^{2}+2\epsilon^{2}}$$This is a slightly less restrictive bound on $k$ than from the other analysis. Note that it also recovers the heat equation stability condition in the $\epsilon \rightarrow \infty$ limit. 

Amplitude as a function of $m$ (x-axis) at $k$ just below $k_\text{crit}$.
![[Screenshot 2024-06-24 at 12.56.30 PM.png]]