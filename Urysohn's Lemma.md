---
tag: topology
mathLink: Urysohn's lemma
---
>[!thm]
Let $X$ be a [[Normal Topological Space]] [[Topological Space]], $A,B$ be [[Disjoint]], [[Closed Set]] [[Subset]]s of $X$. Then, there is a [[Continuous]] [[Function]] $f:X \rightarrow \mathbb{R}$ such that 
>1. $0≤f(x)≤1$ for all $x\in X$
>2. $f(x)=0$ for all $x\in A$
>3. $f(x)=1$ for all $x\in B$

>[!proof]
Let 
$$f(x)=\frac{\text{dist}(x,A)}{\text{dist}(x,A)+\text{dist}(x,B)}$$

