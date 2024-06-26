Meet Monday at 2:00pm
Meet Thursday at 3:00pm
Questions:
1. Clearly, the definition of stable as $$\|u^{n}\|_{\infty}\le\|u^{0}\|_{\infty}$$is not conducive to the [[Allen-Cahn Equation]]
2. Error bound: $$\|e^{n}\|_{\infty}≤(1+k)^{n}\|e^{0}\|_{\infty}+2^{n}(1+k)^{n}k\|\tau\|_{\infty}$$for the linearization of [[Allen-Cahn Equation]] about $v=0$
3. 



$$\frac{\partial u}{\partial t}=D\frac{\partial^{2}u}{\partial x^{2}},\quad x\in[0,1]$$

Dirichlet Boundary: $$u(0,t)=u(1,t)=0$$


We choose the odd 2-periodic extension of the initial condition: $$f(x)=\begin{cases}-2x-2 & -1≤x< - \frac{1}{2} \\
2x & - \frac{1}{2}≤x< \frac{1}{2} \\
2-2x & \frac{1}{2}≤x≤1 \\
\end{cases}$$
The [[Fourier Coefficient]]s of $f$ are: $$\hat f_{n}= \frac{4}{\pi^{2}n^{2}}\left(\sin\left(\pi \frac{n}{2}\right)-\sin\left(3\pi \frac{n}{2}\right)\right)$$
So, the solution to the initial value problem is: $$u(x,t)=\sum_{n=1}^{\infty}\hat f_{n}e^{^{- n^{2}\pi^{2}Dt}\sin(n \pi x)}$$

Neuman Boundary:

$$u_{x}(0,t)=u_{x}(1,t)=0$$
even extension of triangle wave

We choose the even 2-periodic extension of the initial condition: $$f(x)=\begin{cases}-2 & -1≤x≤- \frac{3}{4} \\
1+4x & - \frac{3}{4}≤x≤- \frac{1}{4} \\
1 & - \frac{1}{4}≤x≤ \frac{1}{4} \\
1-4x & \frac{1}{4}≤x≤ \frac{3}{4} \\
-1 & \frac{3}{4}≤x≤ 1 \\
\end{cases}
$$
The [[Fourier Coefficient]]s of $f$ are: $$\hat f_{n}= \frac{8}{n^{2}\pi^{2}}\left(\cos\left(n \frac{\pi}{4}\right)-\cos\left(n \frac{3\pi}{4}\right) \right)$$
So, the solution to the initial value problem is $$u(x,t)=\sum_{n=1}^{\infty}\hat f_{n}e^{-n^{2}\pi^{2}Dt}\cos(n \pi x)$$
Periodic Boundary:

1-periodic extension of the triangle wave

We choose the odd 1-periodic initial condition: $$f(x)=\begin{cases}
4x & 0≤x≤ \frac{1}{4} \\
2-4x & \frac{1}{4}≤x≤ \frac{3}{4} \\
4x-4 & \frac{3}{4}≤x<1 \\
\end{cases}$$
The [[Fourier Coefficient]]s of $f$ are $$\hat f_{n}= \frac{4}{\pi^{2}n^{2}}\left(\sin\left(n \frac{\pi}{2}\right)-\sin\left(n \frac{3\pi}{2}\right)\right)$$
So, the solution to the initial value problem is $$u(x,t)=\sum_{n=1}^{\infty}\hat f_{n}e^{-4\pi^{2}n^{2}Dt}\sin(2\pi nx)$$



rate of convergence ([[Supremum Norm]]) as $\lambda$ is fixed (1/4) with $h,k \rightarrow 0$

find constant solutions in space and time to [[Allen-Cahn Equation]]. Linearize about these and look at 
$$\frac{d y}{d t}=y-y^{3}$$
This ODE has general solution: $$y(t)=\frac{Ae^{t}}{\sqrt{1+A^{2}e^{2t}}}$$
The stable equilibrium solutions can be found as limiting behavior: $$\begin{align*}
y(t)&= 1=\lim_{A \rightarrow \infty}y(t)\\
y(t)&= -1=\lim_{A \rightarrow -\infty}y(t)
\end{align*}$$
and the unstable equilibrium is given by $A=0$


$$\frac{\partial v}{\partial t}= \frac{\partial ^{2}v}{\partial x^{2}}- \frac{1}{\epsilon^{2}}(v^{3}-v)$$

or, $$\frac{\partial v}{\partial t}=\epsilon^{2}\frac{\partial ^{2}v}{\partial x^{2}}-v+v^{3}$$

The following are for the case where $v$ is assumed to be 1-periodic.

Linearizing about $v=0$, we have the linear PDE: $$
\frac{\partial v}{\partial t}=\frac{\partial^{2}v}{\partial x^{2}}+ \frac{1}{\epsilon^{2}}v
$$
which has solution $$v(x,t)=\sum_{n=-\infty}^{\infty}C_{n}e^{\left(\frac{1}{\epsilon^{2}}-4\pi^{2}n^{2}\right)t}~e^{2\pi inx}$$
with the initial condition $v(x,0)=v_{0}(x)$, we have the following for the values of the constants $C_{n}$: $$C_{n}=\widehat{[v_{0}]}_{n}$$

Linearizing about $v=1$, we have the linear PDE: $$
\frac{\partial v}{\partial t}=\frac{\partial ^{2}v}{\partial x^{2}}+ \frac{1}{\epsilon^{2}}(2-2v)
$$
This sets up an ODE for the [[Fourier Coefficient]]s: $$\begin{align*}
\frac{d\hat v_{n}}{dt}(t)=-4\pi^{2}n^{2}\hat v_{n}(t)+ \frac{1}{\epsilon^{2}}(2-2\hat v_{n}(t))\quad(n=0)\\
\frac{d\hat v_{n}}{dt}(t)=-4\pi^{2}n^{2}\hat v_{n}(t)- \frac{2}{\epsilon^{2}}\hat v_{n}(t))\quad(n≠0)
\end{align*}$$
which has solution: $$\begin{align*}
\hat v_{n}(t)&= \begin{cases}
C_{n}e^{-\alpha_{n}t}+ \frac{2}{\epsilon^{2}\alpha_{n}} & n=0\\
C_{n}e^{-\alpha_{n}t} & n≠0\\
\end{cases}
\end{align*}$$

where $$\alpha_{n}:=2\left(\frac{1}{\epsilon^{2}}+2\pi^{2}n^{2}\right)$$
and $$C_{n}=\begin{cases} \widehat{[v_{0}]}_{n}- \frac{2}{\epsilon^{2}\alpha_{n}}  & n=0\\
\widehat{[v_{0}]}_{n} & n\ne0
\end{cases}$$



Linearizing about $v=-1$, we have the linear PDE: $$
\frac{\partial v}{\partial t}=\frac{\partial ^{2}v}{\partial x^{2}}- \frac{1}{\epsilon^{2}}(2+2v)
$$

Note that the differential equation: $$\frac{dy}{dt}=ay+b$$has solution $$y=\alpha e^{at}- \frac{b}{a}$$
which was used to solve the $v=±1$ cases.

math 156 notes


For Neumann: $$u^{n}_{-1}=u_{1}^{n}$$









graph interpreted as graphon: 
entropy of a random variable
representation theory
young diagram





Linear stability analysis Allen-Cahn ODE
movies in python
local truncation error
For Crank-Nicolson:


$$\tau_{j}^{n}= \frac{k^{2}}{12}v_{ttt}- \frac{h^{2}}{12}v_{xxxx}+O(k^{3}+h^{3})$$
computing diffusion coefficient



