From 2.8: 4, 5

>[!note] 4
(a) The [[Equivalence Class]] of $x$ is $\{x\}$. The [[Quotient Map]] maps each element to the [[Set]] containing that element. The [[Quotient Space]] is the [[Collection]] of singletons.
>
(b) The [[Equivalence Class]] of $x$ is $x+\mathcal{M}$. The [[Quotient Map]] maps $x$ to $x+\mathcal{M}$. The [[Quotient Space]] is $$\{x+\mathcal{M}:x\in X\}$$
(d) The [[Equivalence Class]] of $x$ is the subset of $x$ that is mapped to $\{f(x)\}$. The [[Quotient Map]] is $$q(x)=f^{-1}(\{f(x)\})$$The [[Quotient Space]] is $$\{f^{-1}(\{f(x)\}:f(x)\in Y)\}$$
(e) The [[Equivalence Class]] of $x$ is $\{x\}$ if $x\in X-A$ and $A$ if $x\in A$. The [[Quotient Map]] is $$q(x)=\begin{cases}A  & \text{if }x\in A \\
\{x\} & \text{if }x\notin A\end{cases}$$The [[Quotient Space]] is $$\{A\}\cup\{\{x\}:x\in X-A\}$$


>[!note] 5
$\mathcal{U}$ is a [[Topology]] on $X/\sim$:
$q^{-1}(\emptyset )=\emptyset$ is [[Open Set]] in $X$, so $\emptyset \in \mathcal{U}$. For all $x\in X$, $q(x)\in X/\sim$, so $q^{-1}(X/\sim)=X$. As $X$ is [[Open Set]] in $X$, $X/\sim$ is [[Open Set]] in $X/\sim$.
>
Let $\mathcal{F}\subseteq \mathcal{U}$. Then, $$q^{-1}\left(\bigcup_{U\in \mathcal{F}}U\right)=\bigcup_{U\in \mathcal{F}}q^{-1}(U)$$by the [[Union Under Preimage]]. Since $U$ is [[Open Set]] in $X/\sim$ for all $U\in \mathcal{F}$, $q^{-1}(U)$ is [[Open Set]] in $X$. Therefore, the arbitrary [[Union]] $\bigcup\{q^{-1}(U):U\in \mathcal{F}\}$ is [[Open Set]] in $X$. So, $$\bigcup_{U\in \mathcal{F}}U\in \mathcal{U}$$
Let $U,V\in \mathcal{U}$. Then, $$q^{-1}(U\cap V)=q^{-1}(U)\cap q^{-1}(V)$$by the [[Intersection Under Preimage]]. Since $U,V$ are [[Open Set]] in $X/\sim$, $q^{-1}(U)$ and $q^{-1}(V)$ are [[Open Set]] in $X$. Therefore, the finite [[Intersection]] $q^{-1}(U)\cap q^{-1}(V)$ is [[Open Set]] in $X$, so $q^{-1}(U\cap V)$ is [[Open Set]] in $X$ and $U\cap V$ is [[Open Set]] in $X/\sim$. That all finite [[Intersection]]s of elements of $\mathcal{U}$ are in $\mathcal{U}$ follows from [[Principle of Mathematical Induction]].
>
That $q$ is [[Continuous]] is obvious from the definition of $\mathcal{U}$.
