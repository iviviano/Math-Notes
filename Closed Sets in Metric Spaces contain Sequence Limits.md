---
tag: topology
mathLink: closed sets in metric spaces contain sequence limits
---
>[!prop]
>Let $(X,d)$ be a [[Metric Space]]. Then a [[Subset]] $F$ of $X$ is [[Closed Set]] [[iff]] whenever $\{x_{n}\}$ is a [[Sequence]] in $X$ and $x_{n}$ [[notation for converges]] $x$, $x\in F$.

>[!proof]
>This is a direct implication of the [[Closure Contains All Limit Points Theorem]] theorem. 

>[!proof] Proof Specific to Metric Spaces
>Let $F$ be a [[Closed Set]] [[Subset]] of $X$. Let $\{x_{n}\}$ be a [[Sequence]] in $X$ with $x_{n}\rightarrow x$. Suppose $x\in F^c$. Then, there is a [[Ball]] $B_{d}(x,\epsilon)$ [[notation for subset]] $F^c$. Particularly, for all $n$, $x_{n}\notin B_{d}(x,\epsilon)$. This contradicts that $x_{n}\rightarrow x$, so $x\notin F^c$ [[implies]] $x\in F$. 
>
>Let $x\in \text{cl }F$. Then, for all $\epsilon>0$, $B_{d}(x,\epsilon)\cap F≠\emptyset$ as all [[Open Sets Intersecting the Closure Intersect the Set Theorem]]. For each $n\in \mathbb{N}$, pick $x_{n}\in B_{d}(x,\frac{1}{n})\cap F$. Then, $x_{n}\rightarrow x$. As $x\in F$, $\text{cl }A=A$, so $A$ is [[Closed Set]] by the [[Interior, Closure, and Boundary Proposition]].
