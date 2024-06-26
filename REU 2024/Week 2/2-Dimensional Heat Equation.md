Solve the differential equation: $$\frac{\partial u}{\partial t}= D\left(\frac{\partial ^{2}u}{\partial x^{2}}+\frac{\partial^{2} u}{\partial y^{2}}\right)$$
subject to the initial condition: $$u(x,y,t)=u_{0}(x,y)$$
Take the 2-dimensional [[Fourier Transform]] of each side
LHS: $$\frac{\partial }{\partial t}\widehat u(\omega_{x},\omega_{y},t)$$
RHS: 
$$((2\pi i \omega_{x})^{2}+(2\pi i \omega_{y})^{2})\widehat u(\omega_{x},\omega_{y},t)=-4\pi^{2}D(\omega_{x}^{2}+\omega_{y}^{2})~\widehat u(\omega_{x},\omega_{y},t)$$
Solving the [[Decay Equation]] gives: $$\widehat u(\omega_{x},\omega_{y} ,t)=\widehat u_{0}(\omega_{x},\omega_{y})\cdot e^{-4\pi^{2}D(\omega_{x}^{2}+\omega_{y}^{2})t}\quad(*)$$
Note the [[Fourier Transform]] of the 2d [[Gaussian]]: $$\begin{align*}
g(x,y)&= e^{-A(x^{2}+y^{2})}\\
\widehat g(\omega,\nu)&= \frac{\pi}{A}e^{- \frac{\pi^{2}}{A}(\omega^{2}+\nu^{2})} 
\end{align*}$$
and equivalently the inverse transform: $$\begin{align*}
\widehat g(x,y)&= e^{-A(x^{2}+y^{2})}\\
g(\omega,\nu)&= \frac{\pi}{A}e^{- \frac{\pi^{2}}{A}(\omega^{2}+\nu^{2})} 
\end{align*}$$
Applying the [[Convolution Theorem]], we see that $u$ is the convolution of the inverse transforms of each factor of $(*)$:

$$u(x,y,t)= \frac{1}{4\pi Dt}\int_{-\infty}^{\infty}\int _{-\infty}^{\infty}u_{0}(x',y')\cdot e^{- \frac{(x-x')^{2}+(y-y')^{2}}{4Dt}}\ d x'dy'$$
