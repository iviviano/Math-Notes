---
tag: topology
mathLink: Tikhonov's theorem
---
>[!thm]
>If $\{X_{i}:i\in I\}$ is a [[Collection]] of [[Topological Space]]s and their [[Cartesian Product]] $X$ is given the [[Product Topology]], then $X$ is [[Compactness]] [[iff]] $X_{i}$ is [[Compactness]] for each $i\in I$.

>[!proof]
As each projection map is [[Continuous]], when $X$ is [[Compactness]], so is $X_{i}$ for all $i$ by the [[Extreme Value Theorem]]. 
>
Let $\mathcal{S}$ be the standard [[Subbasis]] for the [[Product Topology]] on $X$ ([[Subbasis for the Product Topology Theorem]]). Suppose each $X_{i}$ is [[Compactness]], and let $\mathcal{U}\subseteq \mathcal{S}$ be an [[Open Cover]] of $X$. By [[Alexander's Theorem]], we must only find a finite [[Subcover]] of $\mathcal{U}$. For each $i\in I$, set $\mathcal{U}_{i}=\{U\in T_{i}:\pi_{i}^{-1}(U)\in \mathcal{U}\}$. By definition, $$\mathcal{U}=\bigcup_{i\in I}\{\pi_{i}(U):U\in\mathcal{U_i}\}$$
>
Claim: there exists $i\in I$ such that $\mathcal{U}_i$ is a [[Cover]] of $X_i$
If not for all $i$, there is an $x_{i}\in X_i$ such that $x_{i}\in X_{i}-\{U:U\in \mathcal{U_i}\}$. Define $x\in X$ by $x(i)=x_i$. Then, $x\notin \pi_{i}^{-1}(U)$ for an $U\in \mathcal{U_i}$. So, $x\notin$ any element of $\mathcal{U}$, contradicting that $\mathcal{U}$ [[Cover]]s $X$.
>
Let $i\in I$ such that $\mathcal{U_i}$ [[Cover]]s $X_i$. Then, there is a finite [[Subcover]] $\mathcal{U_{i}'}$ of $X_i$. Then, $$X=\bigcup_{U\in \mathcal{U_i}'}\pi_{i}^{-1}(U)$$by the [[Union Under Preimage]], so, $\{\pi_{i}^{-1}(U):U\in \mathcal{U}_i'\}$ is the finite [[Subcover]].

