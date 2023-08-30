---
tag: topology
mathLink: closure contains all limit points
---
```ad-thm
Let $A$ be a [[Set Theory/Subset|Subset]] of the [[Topology/Topological Space|Topological Space]] $X$; let $A'$ be the [[Set]] of all [[Limit Point]]s of $A$ Then
$$\bar{A} = A\cup A'$$
```

```ad-proof
Let $x\in$ [[Notation/closure|closure]] be given. Then, any [[Neighborhood]]s of $x$ [[Intersects]] $A$ by the [[Open Sets Intersecting the Closure Intersect the Set Theorem]]. Suppose $x\in A$. Then, $x\in A\cup A'$. Otherwise, $A - \{x\} = A$, so any neighborhood of $x$ [[Intersects]] $A$ at a point besides $x$, making $x$ a [[Limit Point]] of $A$, so $x\in A'$ and $x\in A\cup A'$.

Let $x\in A\cup A'$ be given. Suppose $x\in A$. Then, $x\in A$ [[Notation/subset|subset]] [[Notation/closure|closure]]. Suppose $x\in A'$. Then, any [[Neighborhood]] of $x$ [[Intersects]] $A$, so $x\in\bar{A}$ by the [[Open Sets Intersecting the Closure Intersect the Set Theorem]].

[[therefore]] $\bar{A} = A\cup A'$
```

