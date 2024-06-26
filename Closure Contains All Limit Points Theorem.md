---
tag: topology
mathLink: closure contains all limit points
---
> [!thm]
> Let $A$ be a [[Subset]] of the [[Topological Space]] $X$; let $A'$ be the [[Set]] of all [[Limit Point]]s of $A$. Then
> $$\bar{A} = A\cup A'$$

> [!proof]
> Let $x\in$ [[notation for closure]] be given. Then, any [[Neighborhood]]s of $x$ [[Intersects]] $A$ as [[Open Sets Intersecting the Closure Intersect the Set Theorem]]. Suppose $x\in A$. Then, $x\in A\cup A'$. Otherwise, $A - \{x\} = A$, so any neighborhood of $x$ [[Intersects]] $A$ at a point besides $x$, making $x$ a [[Limit Point]] of $A$, so $x\in A'$ and $x\in A\cup A'$.
> 
> Let $x\in A\cup A'$ be given. Suppose $x\in A$. Then, $x\in A$ [[notation for subset]] [[notation for closure]]. Suppose $x\in A'$. Then, any [[Neighborhood]] of $x$ [[Intersects]] $A$, so $x\in\bar{A}$ as [[Open Sets Intersecting the Closure Intersect the Set Theorem]].
> 
> [[therefore]] $\bar{A} = A\cup A'$

