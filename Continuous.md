---
tag: topology
mathLink: continuous
---
> [!def]
> Let $X$ and $Y$ be [[Topological Space]]s. A [[Function]] $f:X\rightarrow Y$ is said to be *continuous* if for each [[Open Set]] [[Subset]] $V$ of $Y$, the [[Set]] $U = f$[[notation for inverse]]$(V)$ is an [[Open Set]] [[Subset]] of $X$.

Note: 
- Continuity depends not only on $f$ but on the [[Topology]]s of its [[Domain]] and [[Range]]. 
- A function can also be [[Continuity at a Point]] $x\in X$.  
- Continuity can also be defined in terms of the [[Preimage|Preimage]]s of [[Basis of a Topology|Basis of a Topology]] elements: [[Basis and Subbasis Formulation of Continuity]]. 

>[!prop] 
>A [[Function]] is [[Continuous]] [[iff]] it is [[Continuity at a Point]] $x$ for all $x\in X$.
>>[!proof]
Let $x\in X$. Let $U\subseteq Y$ be a [[Neighborhood]] of $f(x)$. If $G=f^{-1}(U)$, then $G$ is [[Open Set]]. So, $f$ is [[Continuity at a Point]] $x$.
>>
Let $U\subseteq Y$ be [[Open Set]]. If $f^{-1}(U)=\emptyset$. Then, $f^{-1}(U)$ is [[Open Set]]. Otherwise let $x\in f^{-1}(U)$. As $f$ is [[Continuity at a Point]] $x$, there is a [[Neighborhood]] $G$ of $x$ such that $G\subseteq f^{-1}(U)$. So, $f^{-1}(U)$ is [[Open Set]]. 
