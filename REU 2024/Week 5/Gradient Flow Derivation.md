
The gradient is the best linear approximation of a functional. Let $\mathcal{F}$ be a function space with an [[Inner Product]] $(\cdot,\cdot)$. Let $F:\mathcal{F}\rightarrow \mathbb{R}$ be an arbitrary functional. The gradient of $F$ at $u\in\mathcal{F}$, $\frac{\partial F}{\partial u}\in\mathcal{F}$ is the unique function with the following property. For all functions $v\in\mathcal{F}$ there exists $\epsilon>0$ such that
$$F(u+\epsilon v)=F(u)+\epsilon\left( \frac{\partial F}{\partial u},v\right)+O(\epsilon^{2})$$
For a functional $F$, the gradient flow is the differential equation: $$\frac{\partial u}{\partial t}=-\frac{\partial F}{\partial u}$$
The gradient of $F$ at $u\in\mathcal{F}$ is defined by $$\langle \cdot,v\rangle:= \frac{d}{d \epsilon}F(u+\epsilon v)\bigg|_{\epsilon=0}=(\frac{\partial F}{\partial u},v)_\mathcal{F}$$
Then, the gradient flow equation is $$...$$


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
We will consider a periodic subspace of $L^{2}$: $$L_{p}^{2}:=\{u\in L^{2}([0,1]^{d}):u\big|_{x_{i}=0}=u\big|_{x_{i}=1},1\le i\le d\}$$
This is a Hilbert space under the $L^{2}$ inner product and norm. 


Compute the linear approximation of the energy functional $F$ in $L^{2}_{p}$: $$\begin{align} %\label{eq_lin_approx}
F(u+\epsilon v)&= M\int_{\Omega}\psi(u+\epsilon v)+ \frac{\gamma}{2}|\nabla u+\epsilon\nabla v|^{2}\ dx\\
\end{align}$$

Using (\ref{eq_l2normsum}), the second term or (\ref{eq_lin_approx}) may be written $$\begin{split} %\label{eq_}
\int_{\Omega}|\nabla u+\epsilon\nabla v|^{2}\ dx&=\|\nabla u\|_{2}^{2}+2( \nabla u,\epsilon\nabla v)_{2}+\|\epsilon \nabla v\|_{2}^{2}\\
&=\|\nabla u\|_{2}^{2}+2\epsilon(\nabla u,\nabla v)_{2}+\epsilon^{2}\|\nabla v\|_{2}^{2}\\
\end{split}$$
To handle the inner-product term of (\ref{above}) we note the following useful vector relationships $$\begin{align*}
\nabla u\cdot \nabla v&= \sum_{n=1}^{d}\frac{\partial u}{\partial x_{n}}\frac{\partial v}{\partial x_{n}}\\
\nabla \cdot(u\nabla v)&= \sum_{n=1}^{d}\frac{\partial}{\partial x_{n}}\left(u \frac{\partial v}{\partial x_{n}}\right)\\
&= \sum_{n=1}^{d} \frac{\partial u}{\partial x_{n}}\frac{\partial v}{\partial x_{n}}+\sum_{n=1}^{d}u\frac{\partial^{2} v}{\partial^{2} x_{n}}\\
&= \nabla u\cdot \nabla v+u\nabla ^{2}v
\end{align*}$$
So, 
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
Therefore, 
$$\begin{align*}
\frac{d}{d \epsilon}F(u+\epsilon v)&= \frac{d}{d \epsilon}\left[\int_{\Omega}\psi(u+\epsilon v)\ dx+\|u\|_{2}^{2}+\epsilon(-\nabla ^{2}u,v)_{2}+\epsilon^{2}\|v\|_{2}^{2}\right]\\
&= \int_{\Omega} \frac{d}{d \epsilon}\psi(u+\epsilon v)~dx+(-\nabla ^{2}u,v)_{2}+2\epsilon \|v\|_{2}^{2}\\
&= \int_{\Omega}\psi'(u+\epsilon v)\cdot v~dx+(-\nabla ^{2}u,v)_{2}+2\epsilon \|v\|^{2}_{2}
\end{align*}$$
We have
$$\frac{d}{d \epsilon}F(u+\epsilon v)\bigg|_{\epsilon=0}=\int_{\Omega} \psi'(u)\cdot v~dx+(-\nabla ^{2}u,v)_{2}=(\psi'(u)-\nabla ^{2}u,v)_{2}$$
Using the $L^{2}$ association: $$\langle \frac{\partial F}{\partial u},v\rangle=(\psi'(u)-\nabla ^{2}u,v)_{2}\implies \frac{\partial F}{\partial u}=\psi'(u)-\nabla ^{2}u$$


The Allen-Cahn equation 

Therefore, in $L^{2}_{p}(\Omega)$, we have the following expression for the gradient of $F$:
$$\frac{\partial F}{\partial u}=M[\psi'(u)-\gamma\nabla ^{2}u]$$
Accordingly, we have the $L^{2}$ gradient flow for $F$: $$\begin{equation} %\label{eq_}
\frac{\partial u}{\partial t}=M[\gamma \nabla ^{2}u-\psi'(u)]
\end{equation}$$



Generally, the $L^{2}$ Sobolev spaces are defined by $$
H^{m}(\Omega)=\{u\in L^{2}(\Omega):\partial ^{\alpha}u\in L^{2}(\Omega)\text{ for all }|\alpha|\le n\}
$$
for non-negative integers $m$. 

$H^{m}(\Omega)$ is a Hilbert space with inner product $$(u,v)_{H^{m}}=\sum_{|\alpha|\le m}(\partial ^{\alpha}u,\partial ^{\alpha}v)_{2}$$
and induced norm $$\|u\|_{H^{m}}=\{(u,u)_{m}\}^{\frac{1}{2}}$$

Specifically considering functions on our domain $\Omega=[0,1]^{d}$, we define a periodic Sobolev space $$H^{m}_{p}=H^{m}([0,1]^{d})\cap L^{2}_{p}$$
To ensure uniqueness of solutions, we will further restrict our analysis to zero-average functions: $$\dot H_{p}^{m}=\{u\in H^{m}_{p}:\int_{\Omega}u(x)~dx=0\}$$
We note that $H^{m}_{p}$ and $\dot H^{m}_{p}$ are Hilbert spaces under the same inner product (\ref{eq_IP}). Additionally, for functions $u,v\in\dot H^{m}_{p}$, the inner product becomes $$(u,v)_{H^{m}}=\sum_{1\le|\alpha|\le m}(\partial ^{\alpha}u,\partial ^{\alpha}v)_{2}$$
We may extend these constructions to $m<0$ by defining $$H^{-m}(\Omega)=dual$$
and similarly for the periodic subspaces. The [[Riesz Representation Theorem]] defines an inner product on the dual spaces: $$(u^{*},v^{*})_{H^{-m}}:=(u,v)_{H^m}$$where for arbitrary $u^{*},v^{*}\in H^{-m}(\Omega)$, $u,v\in H^{m}(\Omega)$ are their associates. 



For the Cahn-Hilliard equation, we will find the gradient of (\ref{eq_func}) over $\dot H^{-1}_{p}$. Explicitly, the inner product is $$(u^{*},v^{*})_{H^{-1}}=(u,v)_{H^{1}}=\sum_{|\alpha|=1}(\partial ^{\alpha}u,\partial ^{\alpha}v)_{2}= (\nabla u,\nabla v)_{2}$$
To establish the associate corespondance between $\dot H^{1}_{p}$ and $\dot H^{-1}_{p}$, we consider the elliptic problem $$\begin{split} %\label{eq_periodic_problem}
-\nabla ^{2} u=f\\
\nabla u\big|_{x_{i}=0}=\nabla u\big|_{x_{i}=1}
\end{split}$$
where $u\in \dot H^{1}_{p}$ and $f\in\dot H^{-1}_{p}$. Say $u$ is a weak solution to (\ref{eq_periodic_problem}) if $$\langle f,v\rangle=(u,v)_{H^{1}}$$
The [[Riesz Representation Theorem]] guarantees the existence and uniqueness of such a $u$ as the associate of $f$. Additionally, the boundary conditions of (\ref{eq_periodic_problem}) along with the integration by parts identity (\ref{eq_IBP}) imply
$$\langle f,v\rangle=(u,v)_{H^{1}}=(\nabla u,\nabla v)_{2}=(-\nabla ^{2}u,v)_{2}$$
Thus, for $u^{*}\in \dot H^{-1}_{p}$ and its associate $u$, the $L^{2}$ association
$$\begin{equation}
u^{*}=-\nabla ^{2}u
\end{equation}$$
holds whenever $\nabla u$ is periodic.




Fix $u^{*}\in \dot H^{-1}_{p}(\Omega)$. Let $$w:=M[\gamma\nabla ^{2}u^{*}-\psi'(u^{*})]$$
and let $v^{*}\in \dot H^{-1}_{p}$ be arbitrary. Let $w^{*}\in H^{-1}_{p}$ be the function having $w$ as its associate (UNIQUE????). We will assume $\nabla w$ is periodic to use the association (\ref{eq_association}) and the integration by parts identity (\ref{eq_gen_IBP}). Denote the associates of $u^*$ and $v^*$ as $u$ and $v$, respectively.
$$\begin{align*}
(w^{*},v^{*})_{H^{-1}}&= (w,v)_{H^{1}_{0}}\\
&= \int_{\Omega}\nabla w\cdot \nabla v~dx\\
&= \int_{\Omega}w\cdot(-\nabla ^{2}v)~dx&(\ref{eq_gen_IPB})\\
&= \int_{\Omega}w\cdot v^{*}~dx&(\ref{eq_dirichlet})\\
&= \int_{\Omega}M[\gamma\nabla ^{2}u^{*}-\psi'(u^{*})]\cdot v^{*}~dx\\
&= (M[\gamma\nabla ^{2}-\psi'(\cdot)]u^{*},v^{*})_{2}
\end{align*}$$
Therefore, the gradient of $F$ in $\dot H_{p}^{-1}$ is given by $$\frac{\partial F}{\partial u^{*}}=w^{*}=-\nabla ^{2}(w)=M\nabla ^{2}[\psi'(u^{*})-\gamma \nabla ^{2}u^{*}]$$
The corresponding gradient flow is the Cahn-Hilliard equation...



Remark: We restricted the derivation to 0-average functions, but ...




