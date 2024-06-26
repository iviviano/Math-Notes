---
tag: topology
mathLink: $\epsilon-\delta$ formulation of continuity
---
> [!thm]
> Let $f:X\rightarrow Y$; let $X$ and $Y$ be [[Metrizable]] with [[Metric]]s $d_X$ and $d_Y$. Then $f$ is [[Continuous]] [[iff]] $\forall x\in X:\forall \epsilon>0:\exists \delta>0$ such that
> $$d_X(x,y)<\delta\implies d_Y(f(x),f(y))<\epsilon$$

> [!proof]
> Suppose $f$ is [[Continuous]]. Let $\epsilon>0,x\in X$, be given. Then, $U=f^{-1}(B_{d_{Y}}(f(x)),\epsilon)$ is [[Open Set]] in $X$. As $x\in U$, pick $\delta>0$ such that $B_{d_X}(x,\delta)\subseteq U$. If $y\in X$ and $d_X(x,y)<\delta$, $y\in B_{d_{X}}(x,\delta)$, so $y\in U$ and $f(y)\in B_{d_Y}(f(x),\epsilon)$. [[therefore]] $d_Y(f(x),f(y))<\epsilon$
> 
> Suppose the $\epsilon-\delta$ definition holds. Let $V$ be [[Open Set]] in $Y$. For each $x\in f^{-1}(V)$, pick $\epsilon>0$ such that $B_{d_Y}(f(x),\epsilon_x)\subseteq V$. Then, for each $x\in f^{-1}(V)$, pick $\delta_x>0$ such that 
> $$d_X(x,y) < \delta_x\implies d_Y(f(x),f(y))<\epsilon_x$$
> Then, 
> $$\bigcup_{x\in f^{-1}(V)} B_{d_{X}}(x,\delta_{x})=f^{-1}(V)$$
> This [[Union]] is certainly [[Open Set]], as each [[Ball]] is [[Open Set]]. Proof of [[Subset]] relation: Let $x\in f^{-1}(V)$ be given. Then, if $y\in f(B_{d_{X}}(x, \delta_{x}))$, $d_Y(f(x), f(y))<\epsilon_x$, so $y\in B_{d_{Y}}(f(x), \epsilon_x)\subseteq V$. [[therefore]] the $\epsilon-\delta$ definition implies the topological definition of continuity for [[Metric Space]]s.
