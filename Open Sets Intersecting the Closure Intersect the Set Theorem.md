---
tag: topology
mathLink: open sets intersecting the closure intersect the set theorem
---
```ad-thm
Let $A$ be a [[Set Theory/Subset|Subset]] of the [[Topology/Topological Space|Topological Space]] $X$.
1. Then $x\in$ [[Notation/closure|closure]] [[iff]] every [[Open Set]] set $U$ containing $x$ [[Intersects]] $A$ (Every [[Neighborhood]] of $x$ [[Intersects]] $A$)
2. Supposing the [[Topology]] of $X$ is given by a [[Topology/Basis|Basis]], then $x\in$ [[Notation/closure|closure]] [[iff]] every [[Topology/Basis|Basis]] element $B$ containing $x$ [[Intersects]] $A$.
```

```ad-proof
1. Suppose $x\in\bar{A}$. Then $x$ is in every [[Closed Set]] set containing $A$. So, if an [[Open Set]] set $U$ contains $x$, its [[Set Theory/Compliment|Compliment]] does not contain $A$, so $U$ [[Intersects]] $A$.
Suppose every [[Open Set]] set containing $x$ [[Intersects]] $A$. Then, no [[Closed Set]] set containing $A$ does not contain $x$. Therefore, $x\in$ [[Notation/closure|closure]]

2. Suppose $x\in\bar{A}$. Then, every [[Topology/Basis|Basis]] element containing $x$ is an [[Open Set]] set containing $x$, so it [[Intersects]] $A$ by (1). Suppose every [[Topology/Basis|Basis]] element $B$ containing $x$ [[Intersects]] $A$. Every open set containing $x$ contains a [[Topology/Basis|Basis]] element $B$ containing $x$. Therefore, every [[Open Set]] set containing $x$ [[Intersects]] $A$, so $x\in\bar{A}$ by (1)
```

