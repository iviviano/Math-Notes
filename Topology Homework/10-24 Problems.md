From 2.3: 2, 7, 8

>[!note] 2
Let $X=[0,1]$ be equipped with the [[Metric Topology]] and $W=\{0,1\}$ have the [[Discrete Topology]] given by the [[Metric]] $\rho$. Let $A=[0,\frac{1}{2}),B=[\frac{1}{2},1]$. Clearly, $X=A\cup B$. Define $g:A \rightarrow W$ and $h:B \rightarrow W$ by $$\begin{align}
\forall x\in A:h(x)=0\\
\forall x\in B:g(x)=1\\
\end{align}$$
and let $f$ be given by the [[Pasting Lemma]]. Pick $\epsilon>0$ with $\epsilon<1$. Then, for all $\delta>0$ there exists $x\in A$ such that $x\in B_{d}(\frac{1}{2},\epsilon)$ in $X$. Then, $\rho(f(\frac{1}{2}),x)=\rho(1,0)=1>\epsilon$, so $f$ is not [[Continuous]] by the [[Ep-de Formulation of Continuity]]

>[!note] 7

Let $X_{1}=\mathbb{R},X_{2}=\mathbb{R}^{3}$ and let $Z_{1}=Z_{2}=\mathbb{R}^{2}$. Then, $$X=Z=\mathbb{R}^{4}$$so, $X$ is homeomorphic to $Z$. However, $X_{1}$ is not homeomorphic to $Z_{1}$ or $Z_{2}$. Suppose $f:\mathbb{R}\rightarrow \mathbb{R}^{2}$ is a [[Homeomorphism]]. Then, $f^{-1}(\mathbb{R}^{2})=\mathbb{R}$. Let $y=f(0)$. Then, $f^{-1}(\mathbb{R}^{2}-\{y\})=\mathbb{R}-\{0\}$. Clearly, $\mathbb{R}-\{0\}$ is not connected, since $\mathbb{R}-\{0\}=(-\infty,0)\cup(0,\infty)$. Let $Y=\mathbb{R}^{2}-\{y\}$ and give $Y$ the [[Subspace Topology]]. A set $A\subseteq Y$ is [[Open Set]] ([[Closed Set]]) if and only if it the intersection of a [[Open Set]] ([[Closed Set]]) [[Subset]] of $\mathbb{R}^{2}$ intersected with $Y$. Suppose $A\subseteq Y$ is both [[Open Set]] and [[Closed Set]] and nonempty. Pick $U,F\subseteq \mathbb{R}^{2}$ [[Open Set]] and [[Closed Set]], respectively, such that $A=Y\cap U$ and $A=Y\cap F$. Therefore, $A=Y\cap(U\cap F)$. As 

If $U$ doesn't contain $y$, then $A$ is [[Open Set]] in $\mathbb{R}^{2}$. If $F$ doesn't contain $y$, then $A$ is [[Closed Set]] in $\mathbb{R}^{2}$. As $\mathbb{R}^{2}$ is [[Connected]], $A$ cannot be both [[Open Set]] and [[Closed Set]] in $\mathbb{R}^{2}$ if $U\cap F$ doesn't contain $y$. So, $y\in U\cap F$, and $A=U\cap F-\{y\}$. 

As the [[Image]] of a [[Connected]] [[Set]] under $f^{-1}$ is not [[Connected]], $f^{-1}$ cannot be [[Continuous]] by the [[Intermediate Value Theorem]]. [[therefore]] $f$ is not a [[Homomorphism]]. 


>[!note] 7
Let $X_{1},X_{2},Z_{1},Z_{2}$ be [[Topological Space]]s and let $X=X_{1}\times X_{2}$ and $Z=Z_{1}\times Z_{2}$ be given the [[Product Topology]]. Let $\pi$ denote the [[Projection]] maps on $X$ and $\phi$ be the [[Projection]] maps on $Z$.
>
Suppose that after some renumbering of the spaces, $X_{k}$ and $Z_{k}$ are [[Homeomorphic]] for $k=1,2$. 
>
There are two possible orderings. Suppose $X_{1},Z_{1}$ and $X_{2},Z_{2}$ are [[Homeomorphic]]. Let $f_{1}:X_{1}\rightarrow Z_{1},f_{2}:X_{2}\rightarrow Z_{2}$ be [[Homeomorphism]]s. Let $U_{1}\times U_{2}$ be [[Open Set]] in $X$. Then, $U_{1}$ is [[Open Set]] in $X_1$ and $U_{2}$ is [[Open Set]] in $X_{2}$. So, $f_{1}(U_{1})$ is [[Open Set]] in $Z_{1}$ and $f_{2}(U_{2})$ is [[Open Set]] in $Z_{2}$. Therefore, $f_{1}(U_{1})\times f_{2}(U_{2})$ is [[Open Set]] in $Z$. So, $f:X \rightarrow Z$ given by the [[Rule of Assignment]] $$f=(f_{1},f_{2})$$ is an [[Open Map]] map. Let $V_{1}\times V_{2}$ be [[Open Set]] in $Z$. Then, $f_{1}^{-1}(V_{1})$ is [[Open Set]] in $X_{1}$ and $f_{2}^{-1}(V_{2})$ is [[Open Set]] in $X_{2}$. So, $f^{-1}(V_{1}\times V_{2})=f_{1}^{-1}(V_{1})\times f_{2}^{-1}(V_{2})$ is [[Open Set]] in $X$. [[therefore]] $f^{-1}$ is an [[Open Map]] map, and $f$ is a [[Homeomorphism]].
>
Suppose $X_{1},Z_{2}$ and $X_{2},Z_{1}$ are [[Homeomorphic]]. Let $f_{1}:X_{1}\rightarrow Z_{2},f_{2}:X_{2}\rightarrow Z_{1}$ be [[Homomorphism]]s. Let $f:X \rightarrow Z$ be given by the [[Rule of Assignment]] $f=(f_{2},f_{1})$. Clearly, the same argument shows that $f$ is a homeomorphism. The formulation given in the problem then follows from [[Principle of Mathematical Induction]].




>[!note] 8
Let $X=\{a,b\}$. Let $f:X \rightarrow X$ have the [[Rule of Assignment]] $f(x)=a$. Give $X$ the [[Topology]] $$T=\{\emptyset ,\{a\},X\}$$Then, $f$ is an open map. However, $f(b)=\{a\}$. As $X-\{a\}=\{b\}$ is not open, $f$ is not a closed map.
