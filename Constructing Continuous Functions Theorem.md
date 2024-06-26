---
tag: topology
mathLink: contructing continuous functions theorem
---
> [!thm]
> Let $X$, $Y$, and $Z$ be [[Topological Space]]s.
> 1. (Constant [[Function]]) If $f:X\rightarrow Y$ maps all of $X$ into a single point $y_0\in Y$, $f$ is [[Continuous]].
> 2. (Inclusion) If $A$ is a [[Subspace]] of $X$, the [[Inclusion Map]] $j:A\rightarrow X$ is [[Continuous]]
> 3. ([[Composition]]) If $f:X\rightarrow Y$ and $g:Y\rightarrow Z$ are [[Continuous]], then the map $f$ [[composition]] $g:X\rightarrow Z$ is [[Continuous]].
> 4. ([[Restriction]] of the [[Domain]]) If $f:X\rightarrow Y$ is [[Continuous]], and if $A$ is a [[Subspace]] of $X$, then, the restricted function: $f|A: A\rightarrow Y$ is [[Continuous]].
> 5. (Restricting or expanding [[Range]]) Let $f:X\rightarrow Y$ be [[Continuous]]. If $Z$ is a [[Subspace]] of $Y$ containing the [[Image]] set $f(X)$, then the [[Function]] $g:X\rightarrow Z$ obtained by contained by restricting the range of $f$ is [[Continuous]]. If $Z$ is a [[Topological Space]] having $Y$ as a [[Subspace]], then the [[Function]] $h:X\rightarrow Z$ obtained by expanding the [[Range]] of $f$ to $Z$ is [[Continuous]].
> 6. ([[Local]] formulation of continuity) The map $f:X\rightarrow Y$ is [[Continuous]] if $X$ can be written as the [[Union]] of [[Open Set]] sets $U_\alpha$ such that $f|U_\alpha$ is [[Continuous]] for each $\alpha$.
> If $f,g:X \rightarrow \mathbb{R}$, define:
> $$\begin{align}
> (f\lor g)(x)&=\max\{f(x),g(x)\} \\
> (g\land f)(x)&=\min\{f(x),g(x)\}\\
> |f|(x)&=|f(x)|
> \end{align}$$
> 7. If $f,g$ are [[Continuous]], then so are $f\lor g,g\land f,|f|$.
> 8. Expanding the [[Domain]]: [[Tietze's Expansion Theorem]]

> [!proof]
> 1. Let $V$ be a [[Open Set]] [[Subset]] of $Y$. Then, if $y_0\in V$, $f$[[inverse]]$(V) = X$, which is [[Open Set]] in $X$. Otherwise, $f$[[inverse]]$(V) = \emptyset$, which is [[Open Set]] in $X$. [[therefore]] $f$ is [[Continuous]].
> 2. For any [[Subset]] $B$ of $X$, $j$[[notation for inverse]]$(B) = B\cap A$. Therefore, if $V$ is [[Open Set]] in $X$, $j$[[notation for inverse]]$(V) = A\cap V$ is [[Open Set]] in $A$, so $j$ is [[Continuous]].
> 3. Let $W$ be an [[Open Set]] in $Z$. Pick $V$ [[Open Set]] in $Y$ such that $g$[[notation for inverse]]$(W) = V$. Pick $U$ [[Open Set]] in $X$ such that $f$[[notation for inverse]]$(V) = U$. Then, $(f$[[notation for composition]]$g)$[[notation for inverse]]$(W) = U$, so the [[Composition]] is [[Continuous]].
> 4. $f|A = f$ [[notation for composition]] $j$, which are both continuous (2.), so $f|A$ is [[Continuous]] by (3.)
> 5. Let $V$ be [[Open Set]] in $Y$. 
> idea: preimage($V\cap Z$) = preimage($V$)
> idea: preimage($V$) = preimage($V\cap Y$)
> 1. 
