---
tag: topology
mathLink: closed sets in subspaces theorem
---
```ad-def
Let $Y$ be a [[Subspace]] of $X$. We say that a set $A$ is **closed** in $Y$ [[iff]] $A$ [[Notation/subset|subset]] of $Y$ and $A$ is [[Closed Set]] in the [[Subspace Topology]] of $Y$ ($Y - A$ is [[Open Set]] in $Y$)
```

```ad-thm
Let $Y$ be a [[Subspace]] of $X$. Then a set $A$ is closed in $Y$ [[iff]] it equals the [[Set Theory/Intersection|Intersection]] of a [[Closed Set]] set of $X$ with $Y$.
```

```ad-proof
Let $A$ be closed in $Y$. Then $Y - A$ is [[Open Set]] in $Y$. So $\exists U$ [[Notation/subset|subset]] $X$ with $U$ [[Open Set]] in $X$ such that $Y - A = Y\cap U$. 
$$Y \cap (X - U) = (Y\cap X) - (Y \cap U) = Y - (Y - A) = A$$
so, $A$ can be written as the [[Set Theory/Intersection|Intersection]] of a [[Closed Set]] in $X$ with $Y$.
Now suppose the previous conclusion is true. Pick $U$ [[Notation/subset|subset]] $X$ such that $A = U^c$ [[Notation/intersection|intersection]] $Y$. Then, 
$$Y - A = Y - (Y \cap (X - U)) = (Y - Y) \cup (Y - (X - U)) = \emptyset\cup(Y - (X - U) $$
$X - U$ contains nothing in $X$ not in $U$, so Y - (X - U) contains only elements of $Y$, and only elements of $X$ that are not in $U$ of which, all are in $Y$. 
[[therefore]] $Y - (X - U) = Y\cap U$
```

