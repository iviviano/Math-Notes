---
tag: topology
mathLink: limit points in $T_1$ spaces theorem
---
```ad-thm
Let $X$ be a [[Topology/Topological Space|Topological Space]] satisfying the [[T1 Axiom]]; let $A$ be a [[Set Theory/Subset|Subset]] of $X$. Then the point $x$ is a [[Limit Point]] of $A$ [[iff]] every [[Neighborhood]] of $x$ contains infinitely many points of $A$.
```

```ad-proof
Suppose every [[Neighborhood]] of $x$ contains infinitely mainy points of $A$. Then it [[Intersects]] $A$ at some point other than $x$, and $x$ is a [[Limit Point]] of $A$.
Suppose $x$ is a limit point of $A$ and there is a [[Neighborhood]] $U$ of $x$ that [[Intersects]] $A$ at finitely many points. Then $U$ also [[Intersects]] $A - \{x\}$ at finitely many points: $C$. As $C$ is finite, it is closed. $X - C$ is [[Open Set]], so $U$ [[Notation/intersection|intersection]] $X - C$ is [[Open Set]] and contains $x$ but no other points of $A$. So $x$ is not a [[Limit Point]] of $A$.
```

