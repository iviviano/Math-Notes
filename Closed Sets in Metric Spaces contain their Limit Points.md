---
tag: topology
mathLink: closed sets in metric spaces contain their limit points
---
>[!prop]
>Let $(X,d)$ be a [[Metric Space]]. Then a [[Subset]] $F$ of $X$ is [[Closed Set]] [[iff]] whenever $\{x_{n}\}$ is a [[Sequence]] in $X$ and $x_{n}$ [[notation for converges]] $x$, $x\in F$.

>[!proof]
>This is a direct implication of the [[Closure Contains All Limit Points Theorem]] theorem. 

>[!proof] Proof Specific to Metric Spaces
>Let $F$ be a [[Closed Set]] [[Subset]] of $X$. Let $\{x_{n}\}$ be a [[Sequence]] in $X$ with $x_{n}\rightarrow x$. Suppose $x\in F^c$. Then, there is a [[Ball]] $B_{d}(x,\epsilon)$ [[notation for subset]] $F^c$. Particularly, for all $n$, $x_{n}\notin B_{d}(x,\epsilon)$. This contradicts that $x_{n}\rightarrow x$, so $x\notin F^c$ [[implies]] $x\in F$. 
>Let $\{x_{n}\}$ be a [[Sequence]] in $X$. Suppose $x_{n}\rightarrow x\in X$. Then, 
