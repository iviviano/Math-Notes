$$\frac{\partial c}{\partial t}=M\nabla^{2}[\psi'(c)-\gamma\nabla^{2}c]$$
where $\psi$ is the double well potential: $$\psi(c)=\frac{1}{4}c^{4}- \frac{1}{2}c^{2}$$
$$\frac{\partial c}{\partial t}=M\nabla^{2}[c^{3}-c-\gamma\nabla^{2}c]$$
The 1D case may be written: $$\frac{\partial c}{\partial t}=M\frac{\partial ^{2}}{\partial x^{2}}\left[c^{3}-c-\gamma \frac{\partial ^{2}c}{\partial x^{2}}\right]$$
or, equivalently, $$\frac{\partial c}{\partial t}=M\left[6c\left(\frac{\partial c}{\partial x}\right)^{2}+3c^{2}\frac{\partial ^{2}c}{\partial x^{2}}-\frac{\partial ^{2}c}{\partial x^{2}}-\gamma\frac{\partial ^{4}c}{\partial x^{4}}\right]$$
Discretizing time, we have: $$c^{n}=c^{n-1}+k$$

Mass conservation with periodic boundary conditions: $$\begin{align*}
\frac{\ud}{\ud t}\int_{\Omega} c(x,t)~\ud x&=\int_{\Omega} \frac{\ud}{\ud t}c(x,t)~\ud x\\
&= M\int_{\Omega}\nabla^{2}w(x,t)\ud x\\
&= M\int_{[0,1]^{d}}\sum_{n=1}^{d}\frac{\partial ^{2}w}{\partial x_{n}^{2}}(x,t)\ud x\\
&= M\sum_{n=1}^{d}\int_{[0,1]^{d}}\frac{\partial ^{2}w}{\partial x_{n}^{2}}(x,t)\ud x\\
\end{align*}$$
Without loss of generality, consider the first term: $$\begin{align*}
\int_{[0,1]^{d}}\frac{\partial ^{2}w}{\partial x_{1}^{2}}\ud x_{1}\cdots \ud x_{d}&= \int_{[0,1]^{d-1}} \frac{\partial w}{\partial x_{1}}(x_{1},\dots,t)\bigg|_{x_{1}=0}^{1}\ud x_{2}\cdots \ud x_{d}\\
&= \int_{[0,1]^{d-1}}\frac{\partial w}{\partial x_{1}}(1,\ldots,t)-\frac{\partial w}{\partial x_{1}}(0,\ldots,t)\ud x_{2}\cdots\ud x_{d}\\
&= 0
\end{align*}$$


Can also use divergence theorem (makes Neumann boundary conditions trivial)






Linearize about $c=1$:
$$f(x,y)=xy^{2}\approx f(x_{0},y_{0})+f_{x}(x_{0},y_{0})(x-x_{0})+f_{y}(x_{0},y_{0})(y-y_{0})$$
We have $$\begin{align*}
c&= 1\\
\frac{\partial c}{\partial x}&= 0\\
\frac{\partial^{2} c}{\partial x^{2}}&= 0
\end{align*}$$
Linearization of first term: $$6c\left(\frac{\partial c}{\partial x}\right)^{2}\approx0$$
Linearization of second term: $$3c^{2}\frac{\partial ^{2}c}{\partial x^{2}}\approx c-1$$

So, the linearization about $c=1$ is $$\frac{\partial c}{\partial t}=M\left[c-1-\frac{\partial ^{2}c}{\partial x^{2}}-\gamma\frac{\partial ^{4}c}{\partial x^{4}}\right]$$
The forward difference scheme: $$\frac{c_{j}^{n+1}-c_{j}^{n}}{k}=M\left[c^{n}_{j}-1- \frac{c^{n}_{j+1}-2c_{j}^{n}+c_{j-1}^{n}}{h^{2}}-\gamma \frac{c_{j+2}^{n}-4c_{j+1}^{n}+6c_{j}^{n}-4c^{n}_{j-1}+c_{j-2}^{n}}{h^{4}}\right]$$

$$\begin{align*}
|c_{j}^{n+1}|&= kM+\left|\left(1+kM+ \frac{2kM}{h^{2}}- \frac{6\gamma kM}{h^{4}}\right)c_{j}^{n}- \frac{kM}{h^{2}}(c_{j+1}^{n}+c_{j-1}^{n})- \frac{\gamma kM}{h^{4}}(c_{j+2}-4c_{j+1}^{n}-4c_{j-1}^{n}+c_{j-2}^{n}) \right|\\
&\le kM+\left|1+kM+ \frac{2kM}{h^{2}}- \frac{6\gamma kM}{h^{4}}\right|\cdot |c_{j}^{n}|+\left| \left(\frac{4\gamma kM}{h^{4}}- \frac{kM}{h^{2}}\right)(c_{j+1}^{n}+c_{j-1}^{n}) \right|\\
&+\left| \frac{\gamma kM}{h^{4}}(c_{j+2}+c_{j-2})\right|
\end{align*}$$
