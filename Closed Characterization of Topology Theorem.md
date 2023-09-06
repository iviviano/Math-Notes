---
tag: topology
mathLink: closed characterization of a topology theorem
---
> [!thm]
> Let $X$ be a [[Topological Space]]. Then 
> 1. $\emptyset$ and $X$ are [[Closed Set]]
> 2. Arbitrary [[Intersection]]s of [[Closed Set]] sets are [[Closed Set]]
> 3. Finite [[Union]]s of [[Closed Set]] [[Set]]s are [[Closed Set]]
> 

>[!note]
There is nothing special about defining [[Topology]] in terms of [[Open Set]] sets. It could just as easily be defined in terms of [[Closed Set]] sets.

> [!proof]
> Let $X$ be a [[Topological Space]]. $X$ is [[Open Set]], so $\emptyset$ is [[Closed Set]], and $\emptyset$ is [[Open Set]], so $X$ is [[Closed Set]]. [[therefore]] 1.
> let $\mathcal{A}$ be a collection of [[Open Set]] sets in $X$. Then:
> $\left(\bigcup_{A\in\mathcal{A}}A\right)^c = \bigcap_{A\in\mathcal{A}}A^c$
> by [[DeMorgan's Laws]]. Both are [[Closed Set]] in $X$. [[therefore]] 2.
> Let $\mathcal{B}$ be a finite collection of [[Open Set]] sets in $X$. Then:
> $\left(\bigcap_{B\in\mathcal{B}}B\right)^c = \bigcup_{B\in\mathcal{B}}B^c$
> by [[DeMorgan's Laws]]. Both are [[Closed Set]] in $X$. [[therefore]] 3.
