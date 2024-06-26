
The gradient is the best linear approximation of a functional. Let $\mathcal{F}$ be a function space with an [[Inner Product]] $(\cdot,\cdot)$. Let $F:\mathcal{F}\rightarrow \mathbb{R}$ be an arbitrary functional. The gradient of $F$ at $u\in\mathcal{F}$, $\frac{\partial F}{\partial u}\in\mathcal{F}$ is the unique function with the following property. For all functions $v\in\mathcal{F}$ there exists $\epsilon>0$ such that
$$F(u+\epsilon v)=F(u)+\epsilon\left( \frac{\partial F}{\partial u},v\right)+O(\epsilon^{2})$$
For a functional $F$, the gradient flow is the differential equation: $$\frac{\partial u}{\partial t}=-\frac{\partial F}{\partial u}$$


Consider the energy functional $$F(u)=M\int_{\Omega}\psi(u)+ \frac{\gamma}{2}|\nabla u|^{2}~dx$$
Letting $$f(x,u,\nabla u)=\psi(u)+ \frac{\gamma}{2}|\nabla u|^{2}$$
the [[Euler-Lagrange Equation]] for $F$ is $$\frac{\partial f}{\partial u}-\sum_{n=1}^{d}\frac{\partial }{\partial x_{n}}\frac{\partial f}{\partial u_{x_{n}}}=0$$
or equivalently: $$\frac{\partial f}{\partial u}-\nabla_{x}\cdot\nabla_{u_{x}}f=0$$
We have $$\frac{\partial f}{\partial u_{x_{n}}}=\gamma\frac{\partial u}{\partial x_{n}}$$
so, $$\nabla_{x}\cdot\nabla_{u_{x}}f=\gamma\nabla^{2}u$$
and $$\frac{\partial f}{\partial u}=\psi'(u)=\phi(u)$$
So the Euler-Lagrange equation is $$\phi(u)-\gamma\nabla^{2}u=0$$

We introduce the space of square integrable functions: $$\begin{equation} %\label{eq_l2space}
L^{2}(\Omega,\mathbb{R}^{d}):=\left\{f\colon \Omega\to \mathbb{R}^{d}~\bigg|~\int_{\Omega}|f(x)|^{2}~dx<\infty\right\}
\end{equation}$$
Define the $L^{2}$-inner product: $$\begin{equation} %\label{eq_l2ip}
( f,g)_{2}:=\int_{\Omega}f(x)\cdot g(x)~dx
\end{equation}$$
and induced norm: $$\begin{equation} %\label{eq_l2norm}
\|f\|_{2}=\sqrt{( f,f)_{2}}=\left(\int_{\Omega}|f(x)|^{2}\ dx\right)^{\frac{1}{2}}
\end{equation}$$
Note that $$\begin{split} %\label{eq_l2norm_sum}
\|f+g\|_{2}^{2}&=\int_{\Omega}|f(x)+g(x)|^{2}~dx\\
&=\int_{\Omega}|f(x)|^{2}+2f(x)\cdot g(x)+|g(x)|^{2}~dx\\
&=\|f\|^{2}_{2}+( f,g)_{2}+\|g\|^{2}_{2}
\end{split}$$
Compute the linear approximation of the energy functional $F$ in $L^{2}(\Omega)$: $$\begin{align} %\label{eq_lin_approx}
F(u+\epsilon v)&= M\int_{\Omega}\psi(u+\epsilon v)+ \frac{\gamma}{2}|\nabla u+\epsilon\nabla v|^{2}\ dx\\
\end{align}$$
Since the derivative of a (multivariable) function into $\mathbb{R}$ is also the best linear approximation, we have the following for the first term of (\ref{eq_lin_approx}).
$$\int_{\Omega}\psi(u+\epsilon v)\ dx=\int_{\Omega}\psi(u)+\epsilon \psi'(u)v +O(\epsilon^{2})\ dx=\int_{\Omega}\psi(u)\ dx+\epsilon\int_{\Omega}\psi'(u)v\ dx+O(\epsilon^{2})$$
Using (\ref{eq_l2normsum}), the second term or (\ref{eq_lin_approx}) may be written $$\begin{split} %\label{eq_}
\int_{\Omega}|\nabla u+\epsilon\nabla v|^{2}\ dx&=\|\nabla u\|_{2}^{2}+2( \nabla u,\epsilon\nabla v)_{2}+\|\epsilon \nabla v\|_{2}^{2}\\
&=\|\nabla u\|_{2}^{2}+2\epsilon(\nabla u,\nabla v)_{2}+\epsilon^{2}\|\nabla v\|_{2}^{2}\\
&=\int_{\Omega}|\nabla u|^{2}\ dx+2\epsilon(\nabla u,\nabla v)_{2}+O(\epsilon^{2})
\end{split}$$
Note the following useful vector relationships $$\begin{align*}
\nabla u\cdot \nabla v&= \sum_{n=1}^{d}\frac{\partial u}{\partial x_{n}}\frac{\partial v}{\partial x_{n}}\\
\nabla \cdot(u\nabla v)&= \sum_{n=1}^{d}\frac{\partial}{\partial x_{n}}\left(u \frac{\partial v}{\partial x_{n}}\right)\\
&= \sum_{n=1}^{d} \frac{\partial u}{\partial x_{n}}\frac{\partial v}{\partial x_{n}}+\sum_{n=1}^{d}u\frac{\partial^{2} v}{\partial^{2} x_{n}}\\
&= \nabla u\cdot \nabla v+u\nabla ^{2}v
\end{align*}$$

$$\begin{split} %\label{eq_genIBP}
(\nabla u,\nabla v)_{2}&= \int_{\Omega}\nabla u\cdot \nabla v~dx\\
&= \int_{\Omega}\nabla \cdot(v \nabla u)-v \nabla ^{2}u\ dx\\
&= \underbrace{\int_{\partial \Omega}v\nabla u\cdot n~dx}_{=0}-\int_{\Omega}(\nabla ^{2}u)\cdot v~dx\quad(\text{Divergence Theorem)}
\\
&= -(\nabla ^{2}u,v)_{2}
\end{split}$$
The periodic boundary conditions make the boundary integral term vanish: $$\begin{align*}
complete
\end{align*}$$
Therefore, the functional $F$'s linear approximation of the perturbation $u+\epsilon v$ is given by $$\begin{align*}
F(u+\epsilon v)&= M\int_{\Omega}\psi(u)+ \frac{\gamma}{2}|\nabla u|^{2}\ dx+M\epsilon\int_{\Omega}\psi'(u)\cdot v\ dx- M\epsilon \gamma(\nabla ^{2}u,v)_{2}\\
&= F(u)+\epsilon(M[\psi'(~\cdot~)-\gamma \nabla ^{2}]u,v)_{2}
\end{align*}$$


The Allen-Cahn equation 

Therefore, in $L^{2}(\Omega)$, we have the following expression for the gradient of $F$:
$$\frac{\partial F}{\partial u}=M[\psi'(u)-\gamma\nabla ^{2}u]$$
Accordingly, we have the $L^{2}$ gradient flow for $F$: $$\begin{equation} %\label{eq_}
\frac{\partial u}{\partial t}=M[\gamma \nabla ^{2}u-\psi'(u)]
\end{equation}$$




Define the Sobolev space $$\begin{equation} %\label{eq_h1}
H^{1}(\Omega):=\{\phi\in L^{2}(\Omega): \phi_{x_{n}}\in L^{2}(\Omega) \text{ for }1\le n\le d\}
\end{equation}$$where the partial derivatives are taken in the sense of distributions. We also define a subspace $$\begin{equation} %\label{eq_h10}
H^{1}_{0}(\Omega):=\text{cl }(\mathcal{C}^{\infty}_{c}(\Omega))
\end{equation}$$This is the closure of the set of test functions in $H^{1}$.

>[!question]
When is it true that for $u\in H^{1}_{0}(\Omega)$, $$u^{*}=-\nabla ^{2}u?$$do we need that $$u\big|_{\partial \Omega}=0?$$

If not, then the argument below will work, since we have periodicity of $w$ and its gradient





Fix $u^{*}\in H^{-1}(\Omega)$. Let $$w:=M[\gamma\nabla ^{2}u^{*}-\psi'(u^{*})]$$ and let $v^{*}\in H^{-1}$ be arbitrary. Denote the associate of $w$ as $w^{*}$ and the associates of $u^*$ and $v^*$ as $u$ and $v$, respectively.
$$\begin{align*}
(w^{*},v^{*})_{H^{-1}}&= (w,v)_{H^{1}_{0}}\\
&= \int_{\Omega}\nabla w\cdot \nabla v~dx\\
&= \int_{\Omega}w\cdot(-\nabla ^{2}v)~dx&(\ref{eq_gen_IPB})\\
&= \int_{\Omega}w\cdot v^{*}~dx&(\ref{eq_dirichlet})\\
&= \int_{\Omega}M[\gamma\nabla ^{2}u^{*}-\psi'(u^{*})]\cdot v^{*}~dx\\
&= (M[\gamma\nabla ^{2}-\psi'(\cdot)]u^{*},v^{*})_{2}
\end{align*}$$
where in the application of (\ref{eq_genIBP}), we assumed the periodicity of $\nabla w$. Therefore, the gradient of $F$ in $H^{-1}$ is given by $$\frac{\partial F}{\partial u^{*}}=w^{*}=-\nabla ^{2}(w)=M\nabla ^{2}[\psi'(u^{*})-\gamma \nabla ^{2}u^{*}]$$
The corresponding gradient flow is the Cahn-Hilliard equation...


Remark: the periodicity of the first 3 derivatives of $c$ is a sufficient condition for the periodicity of $\nabla w$ assumed above. 






