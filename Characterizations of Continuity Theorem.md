---
tag: topology
mathLink: characterizations of continuity theorem
---
> [!thm]
> Let $X$ and $Y$ be [[Topological Space]]s; let $f:X\rightarrow Y$. Then, the following statements are equivalent:
> 1. $f$ is [[Continuous]]
> 2. For every [[Subset]] $A$ of $X$, $f($[[notation for closure]]$)$[[notation for subset]] $\overline{f(A)}$
> 3. For every [[Closed Set]] [[Set]] $B$ of $Y$, the [[Set]] $f$[[notation for inverse]]$(B)$ is [[Closed Set]] in $X$.
> 4. For each $x\in X$ and each [[Neighborhood]] $V$ of $f(x)$, there is a [[Neighborhood]] $U$ of $x$ such that $f(U)$ [[notation for subset]] $V$.

> [!proof]
$1\implies 3$
Let $C\subseteq Y$ be [[Closed Set]]. Then, $Y-C$ is [[Open Set]], so $f^{-1}(Y-C)$ is [[Open Set]]. So, $X-f^{-1}(C)$ is [[Open Set]] and $f^{-1}(C)$ is [[Closed Set]].
>
$3\implies 1$
Let $C\subseteq Y$ be [[Open Set]]. Then, $Y-C$ is [[Closed Set]], so $f^{-1}(Y-C)$ is [[Closed Set]]. So, $X-f^{-1}(C)$ is [[Closed Set]] and $f^{-1}(C)$ is [[Open Set]].

