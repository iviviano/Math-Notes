---
tag: topology
mathLink: contructing continuous functions theorem
---
```ad-thm
Let $X$, $Y$, and $Z$ be [[Topology/Topological Space|Topological Space]]s.
1. (Constant [[Function]]) If $f:X\rightarrow Y$ maps all of $X$ into a single point $y_0\in Y$, $f$ is [[Continuous]].
2. (Inclusion) If $A$ is a [[Subspace]] of $X$, the [[Inclusion Map]] $j:A\rightarrow X$ is [[Continuous]]
3. ([[Set Theory/Composition|Composition]]) If $f:X\rightarrow Y$ and $g:Y\rightarrow Z$ are [[Continuous]], then the map $f$ [[Notation/composition|composition]] $g:X\rightarrow Z$ is [[Continuous]].
4. ([[Set Theory/Restriction|Restriction]] of the [[Domain]]) If $f:X\rightarrow Y$ is [[Continuous]], and if $A$ is a [[Subspace]] of $X$, then, the restricted function: $f|A: A\rightarrow Y$ is [[Continuous]].
5. (Restricting or expanding [[Range]]) Let $f:X\rightarrow Y$ be [[Continuous]]. If $Z$ is a [[Subspace]] of $Y$ containing the [[Image]] set $f(X)$, then the [[Function]] $g:X\rightarrow Z$ obtained by contained by restricting the range of $f$ is [[Continuous]]. If $Z$ is a [[Topology/Topological Space|Topological Space]] having $Y$ as a [[Subspace]], then the [[Function]] $h:X\rightarrow Z$ obtained by expanding the [[Range]] of $f$ to $Z$ is [[Continuous]].
6. (Local formulation of continuity) The map $f:X\rightarrow Y$ is [[Continuous]] if $X$ can be written as the [[Set Theory/Union|Union]] of [[Open Set]] sets $U_\alpha$ such that $f|U_\alpha$ is [[Continuous]] for each $\alpha$.
```

```ad-proof
1. Let $V$ be a [[Open Set]] [[Set Theory/Subset|Subset]] of $Y$. Then, if $y_0\in V$, $f$[[Notation/inverse|inverse]]$(V) = X$, which is [[Open Set]] in $X$. Otherwise, $f$[[Notation/inverse|inverse]]$(V) = \emptyset$, which is [[Open Set]] in $X$. [[therefore]] $f$ is [[Continuous]].
2. For any [[Set Theory/Subset|Subset]] $B$ of $X$, $j$[[Notation/inverse|inverse]]$(B) = B\cap A$. Therefore, if $V$ is [[Open Set]] in $X$, $j$[[Notation/inverse|inverse]]$(V) = A\cap V$ is [[Open Set]] in $A$, so $j$ is [[Continuous]].
3. Let $W$ be an [[Open Set]] in $Z$. Pick $V$ [[Open Set]] in $Y$ such that $g$[[Notation/inverse|inverse]]$(W) = V$. Pick $U$ [[Open Set]] in $X$ such that $f$[[Notation/inverse|inverse]]$(V) = U$. Then, $(f$[[Notation/composition|composition]]$g)$[[Notation/inverse|inverse]]$(W) = U$, so the [[Set Theory/Composition|Composition]] if [[Continuous]].
4. $f|A = f$ [[Notation/composition|composition]] $j$, which are both continuous (2.), so $f|A$ is [[Continuous]] by (3.)
5. Let $V$ be [[Open Set]] in $Y$. 
idea: preimage($V\cap Z$) = preimage($V$)
idea: preimage($V$) = preimage($V\cap Y$)
1. 
```
