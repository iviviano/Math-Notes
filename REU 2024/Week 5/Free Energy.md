Let $\psi(u)$ be the double well potential: 
![[Screenshot 2024-06-24 at 9.48.18 AM.png | 300]]
The total energy of the system is approximated as $$F(u)=\int_{\Omega}\underbrace{\psi(u)}_{\text{free}}+ \underbrace{\frac{\gamma}{2}|\nabla u|^{2}}_{\text{boundary}}d \omega$$
Use the double well $\Psi(u)= \frac{1}{4}(u^{2}-1)^{2}$. Fix $t>0$. In one dimension, we have $$F(u)=\int_{0}^{1}\underbrace{\psi(u)+ \frac{\gamma}{2}\left(\frac{du}{dx}\right)^{2}}_{:=f(x,u,u')}dx$$
Compute: $$\begin{align*}
\frac{\partial f}{\partial u}&= \psi'(u)=u^{3}-u\\
\frac{\partial f}{\partial u'}&= \gamma u'\\
\frac{d}{dx}\left(\frac{\partial f}{\partial u'}\right)&= \gamma u''
\end{align*}$$
So, the condition that the variational derivative of $f$ vanishes ([[Euler-Lagrange Equation]]) may is $$u^{3}-u-\gamma \frac{d^{2}u}{dx^{2}}=0$$
This should describe an equilibrium solution