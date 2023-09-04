---
tag: topology
mathLink: closure is the set of distance 0 points
---
>[!prop]
>Let $(X,d)$ be a [[Metric Space]], $A$ [[notation for subset]] $X$, then,
>$$\bar{A}=\{x\in X:\text{ dist }(x,A)=0\}$$

I really like this characterization: the [[closure]] is all points that are arbitrarily close to the set. A [[Closed Set]] [[Set]] contains all points that are arbitrarily close to it, while an [[Open Set]] [[Set]] has some points arbitrarily close to it that it doesn't contain. For any space with a conception of geometry, this characterization is very intuitive.

>[!proof]
>Let $x\in$ [[notation for closure]] be given. Then, for all $\epsilon>0$,  $B_{d}(x,\epsilon)$ [[Intersects]] $A$. [[therefore]] for all $\epsilon>0$, there is a point $a\in A$ such that $$d(x,a)<\epsilon$$
>[[therefore]] $\text{dist }(x, A)=0$
>Let $x\in X$ with $d(x, A)=0$. Then, there is a [[Sequence]] $a_{n}\in A$ such that $d(x,a_{n})\rightarrow0$, so $a_{n}\rightarrow x$. 
>[[therefore]] $x\in \bar{A}$ by the [[Closure Contains All Limit Points Theorem]]

