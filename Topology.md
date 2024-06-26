---
tag: topology
mathLink: topology
---

``` ad-def
Let X be a nonempty [[Set]]. Then $T$ is a *topology* on X [[iff]] 
1. $\emptyset\in T$ and $X\in T$
2. Any [[Union]] of elements of $T$ is in $T$
3. Any finite [[Intersection]] of elements of $T$ is in $T$

Then [[notation for topological space]] is a [[Topological Space]]. 
```

Note: A topology can be described by a [[Basis of a Topology|Basis of a Topology]] or [[Subbasis|Subbasis]]. 

Examples:
1. $(X,d)$ is any [[Metric Space]]. $T=\{U\subseteq X:\forall x\in U:\exists \epsilon>0:B_{d}(x,\epsilon)\subseteq U\}$ is the [[Metric Topology]] induced by the [[Metric]] $d$ on $X$
2. $X$ is any [[Set]]. $T=\{\emptyset ,X\}$ is the [[Indiscrete Topology]]
3. $X$ is any [[Set]]. $T=2^{X}$ is the [[Discrete Topology]] on $X$.
4. 