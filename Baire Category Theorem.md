---
tag: topology
mathLink: Baire category theorem
---
>[!thm]
>If $(X,d)$ is a [[Complete]] [[Metric Space]] and $\{U_{n}\}$ is a [[Sequence]] of [[Open Set]] [[Subset]]s of $X$, each of which is [[Dense]] in $X$, then
>$$\bigcap_{n=1}^{\infty}U_{n}$$
>is [[Dense]] in $X$

>[!thm]
>If $X$ is a [[Local Compactness]] [[Topological Space]] and $\{U_{n}\}$ is a [[Sequence]] of [[Open Set]] [[Subset]]s of $X$ each of which is [[Dense]] in $X$, then $$\bigcap_{n=1}^{\infty} U_{n}$$ is [[Dense]] in $X$.

>[!question]
>Is this not a logical equivalence?

>[!proof]
>As each $U_{n}$ is [[Dense]] in $X$,
>$$\text{cl }U_{n}=X$$
>for all $n$. 

Claim: 
$$\bigcap \text{cl }U_{n}=X=\text{cl }\bigcap U_{n}$$
To show $\bigcap U_n$ is dense, show that for any nonempty open subset $G$ of $X$,
$$G\cap\bigcap U_{n}≠\emptyset$$


As every [[Open Sets Intersecting the Closure Intersect the Set Theorem]], $G\cap U_{n}≠\emptyset$ for all $n$. [[therefore]] $G\cap\bigcap$

, if every nonempty [[Open Set]] set in $X$ intersects the [[Intersection]], the [[Closure]] of the intersection must be $X$. 

>[!prop] Corollary
>If $(X,d)$ is a [[Complete]] [[Metric Space]], and $\{F_{n}\}$ is a [[Sequence]] of [[Closed Set]] [[Subset]]s such that $X=\bigcup F_{n}$, then there is an $n$ such that $\text{int }F_{n}\ne \emptyset$.

Thoughts: what if for all $n$ there is no nonempty [[Open Set]] set contained in $F_{n}$. This might imply that $F_{n}$ is finite? And then the countable [[Union]] would be countable. But countable sets can't be complete?

Maybe a [[Closed Set]] set whose [[Compliment]] is [[Dense]] is countable. (Could come from [[Baire Category Theorem]]).