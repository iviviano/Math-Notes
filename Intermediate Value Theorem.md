---
mathLink: generalized IVT
tag: topology, analysis
---
>[!thm]
>Let $X,Y$ be [[Topological Space]]s. Then if $f:X \rightarrow Y$ is [[Continuous]], then the [[Image]] under $f$ of a [[Connected]] [[Subset]] of $X$ is [[Connected]] in $Y$.

>[!proof]
Let $A$ be a [[Connected]] [[Subset]] of $X$. Then, let $B=f(A)$. Suppose $B$ is not [[Connected]]. Then, pick $U,V\subseteq Y$ with $U,V$ [[Open Set]] in $Y$, $B=U\cup V$, $U\cap V=\emptyset$, and $U,V$ nonempty. Then, 
$$A=f^{-1}(U\cup V)=f^{-1}(U)\cup f^{-1}(U)$$
by the [[Union Under Inverse Image]]. As $f$ is [[Continuous]], $f^{-1}(U)$ and $f^{-1}(V)$ are [[Open Set]] in $X$. 
$$\emptyset=f^{-1}(U\cap V)=f^{-1}(U)\cap f^{-1}(V)$$
by the [[Intersection Under Inverse Image]]. As $U$ and $V$ both contain elements of $B$ and $B=f(A)$, $f^{-1}(U)$ and $f^{-1}(V)$ are nonempty. So if $B$ is not [[Connected]], then $A$ cannot be connected. [[therefore]] $B$ is [[Connected]].

>[!thm] Corollary: Intermediate Value Theorem
>Let $f:[a,b]\rightarrow \mathbb{R}$ be [[Continuous]]. Then, 
>$$[\min\{f(a),f(b)\},\max\{f(a),f(b)\}]\subseteq f([a,b])$$


