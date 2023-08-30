---
tag: topology
mathLink: subspace and product topology theorem
---
```ad-thm
If $A$ is a [[Subspace]] of $X$ and $B$ is a [[Subspace]] of $Y$, then the [[Product Topoplogy]] on $A$ [[Notation/cartesian product|cartesian product]] $B$ is the same as the [[Topology]] $A\times B$ inherits as a [[Subspace]] of $X\times Y$.
```

Note: A similar result does not hold when considering $X$ under the [[Order Topology]]. If $A$ is a [[Subset|Subset]] of $X$, the [[Order Topology]] on $A$ is not necessarily the same as the [[Subspace Topology]] on $A$.

```ad-proof
Let $U$ [[Notation/cartesian product|cartesian product]] $V$ be an arbitrary [[Topology/Basis|Basis]] element of the [[Product Topoplogy]] on $X$ [[Notation/cartesian product|cartesian product]] $Y$. Then, $(U\times V)\cap(A\times B)$ is an arbitrary [[Topology/Basis|Basis]] element of the [[Subspace Topology]] of $A$ [[Notation/cartesian product|cartesian product]] $B$. 
$$(U\times V)\cap(A\times B) = (U\cap A)\times(V\cap B)$$

which is an arbitrary [[Topology/Basis|Basis]] element of the [[Product Topoplogy]] on $A$ [[Notation/cartesian product|cartesian product]] $B$. As these two [[Topology]]s have the same [[Topology/Basis|Basis]], they are the same [[Topology]] by the [[Finer Bases Lemma]].
```
