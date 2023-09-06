---
tag: topology
mathLink: triangle identity for distance
---
>[!prop]
>If $(X,d)$ is a [[Metric Space]] and $A$ is a [[Subset]] of $X$, then
>$$|\text{dist}(x,A)-\text{dist}(y,A)|≤d(x,y)$$
>where $x,y\in X$ and $\text{dist}$ is the [[Distance]] of a point to a [[Set]].

>[!proof]
If $z\in A$, then $\text{dist}(x,A)≤d(x,z)$ and $\text{dist}(y,A)≤d(y,z)$. So,
$$\text{dist}(x,A)-\text{dist}(y,A)≤d(x,z)-d(y,z)≤d(x,y)$$
by the [[Reverse Triangle Inequality]] and similarly, 
$$\text{dist}(y,A)-\text{dist}(x,A)≤d(y,z)-d(x,y)≤d(x,y)$$
so,
$$|\text{dist}(x,A)-\text{dist}(y,A)|≤d(x,y)$$

>[!prop] Corollary
>If $A$ is a nonempty [[Subset]] of $X$, then $f:X \rightarrow \mathbb{R}$ defined by $f(x)=\text{dist}(x,A)$ is a [[Continuous]] [[Function]]. 
