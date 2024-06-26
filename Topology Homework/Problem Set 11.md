<h1 align=center>
Topology<br>
Problem Set 11<br>
Isaac Viviano
</p>

---

>[!note] 2.7.3
Let $f:X \rightarrow Y$ be [[Continuity at a Point]] $x\in X$ and let $(x,I)$ be a [[Net]] in $X$ with $x_{i}$ [[notation for clusters]] $x$. Let $V$ be a [[Neighborhood]] of $f(x)$ and let $j\in I$. Then, $f^{-1}(V)$ is [[Open Set]] in $X$, since $f$ is [[Continuous]] at $x$. Pick $i≥j$ such that $x_{i}\in f^{-1}(V)$. Then, $f(x_{i})\in V$, so $f(x_{i})\rightarrow _\text{cl}x$.
>
I am taking the converse to be the statement: let $f$ be a [[Continuous]] [[Function]]; then whenever $\{x_{i}\}$ is [[Net]] in $X$, if $f(x_{i})$ [[notation for clusters]] $f(x)$ for some $x\in X$, then $x_{i}\rightarrow _\text{cl }x$. The converse is not true. Let $f:\mathbb{R}\rightarrow \{0\}$ and let $\{x_{i}:i\in \mathbb{N}\}$ be a [[Net]] defined by $x_{i}=i$. Then, $f$ is [[Continuous]] on $\mathbb{R}$, $f(x_{i})\rightarrow _\text{cl }0$, but $x_{i}$ does not have a [[Clusters]] point.

>[!note] 2.7.8
Let $X=\mathbb{N}$ with the [[Discrete Topology]] and let $I=\mathbb{N}$. Let $(x,I)$ be a [[Net]] defined by $$x_{2i}=1,x_{2i+1}=i$$Then, $x_{i}$ [[notation for clusters]] $1$, does not [[Converges (net)]] to $1$, and does not [[Clusters]] at any other point.

>[!note] 2.8.4
(a) The [[Equivalence Class]] of $x$ is $\{x\}$. The [[Quotient Map]] maps each element to the [[Set]] containing that element. The [[Quotient Space]] is the [[Collection]] of singletons.
>
(b) The [[Equivalence Class]] of $x$ is $x+\mathcal{M}$. The [[Quotient Map]] maps $x$ to $x+\mathcal{M}$. The [[Quotient Space]] is $$\{x+\mathcal{M}:x\in X\}$$
(d) The [[Equivalence Class]] of $x$ is the subset of $x$ that is mapped to $\{f(x)\}$. The [[Quotient Map]] is $$q(x)=f^{-1}(\{f(x)\})$$The [[Quotient Space]] is $$\{f^{-1}(\{f(x)\}:f(x)\in Y)\}$$
(e) The [[Equivalence Class]] of $x$ is $\{x\}$ if $x\in X-A$ and $A$ if $x\in A$. The [[Quotient Map]] is $$q(x)=\begin{cases}A  & \text{if }x\in A \\
\{x\} & \text{if }x\notin A\end{cases}$$The [[Quotient Space]] is $$\{A\}\cup\{\{x\}:x\in X-A\}$$

>[!note] 2.8.5
$\mathcal{U}$ is a [[Topology]] on $X/\sim$:
$q^{-1}(\emptyset )=\emptyset$ is [[Open Set]] in $X$, so $\emptyset \in \mathcal{U}$. For all $x\in X$, $q(x)\in X/\sim$, so $q^{-1}(X/\sim)=X$. As $X$ is [[Open Set]] in $X$, $X/\sim$ is [[Open Set]] in $X/\sim$.
>
Let $\mathcal{F}\subseteq \mathcal{U}$. Then, $$q^{-1}\left(\bigcup_{U\in \mathcal{F}}U\right)=\bigcup_{U\in \mathcal{F}}q^{-1}(U)$$by the [[Union Under Preimage]]. Since $U$ is [[Open Set]] in $X/\sim$ for all $U\in \mathcal{F}$, $q^{-1}(U)$ is [[Open Set]] in $X$. Therefore, the arbitrary [[Union]] $\bigcup\{q^{-1}(U):U\in \mathcal{F}\}$ is [[Open Set]] in $X$. So, $$\bigcup_{U\in \mathcal{F}}U\in \mathcal{U}$$
Let $U,V\in \mathcal{U}$. Then, $$q^{-1}(U\cap V)=q^{-1}(U)\cap q^{-1}(V)$$by the [[Intersection Under Preimage]]. Since $U,V$ are [[Open Set]] in $X/\sim$, $q^{-1}(U)$ and $q^{-1}(V)$ are [[Open Set]] in $X$. Therefore, the finite [[Intersection]] $q^{-1}(U)\cap q^{-1}(V)$ is [[Open Set]] in $X$, so $q^{-1}(U\cap V)$ is [[Open Set]] in $X$ and $U\cap V$ is [[Open Set]] in $X/\sim$. That all finite [[Intersection]]s of elements of $\mathcal{U}$ are in $\mathcal{U}$ follows from [[Principle of Mathematical Induction]].
>
That $q$ is [[Continuous]] is obvious from the definition of $\mathcal{U}$.