---
tag: topology
mathLink: partition of unity
---
>[!thm]
If $X$ is a [[Normal Topological Space]] [[Topological Space]] and $\{G_{1},\ldots,G_{n}\}$ is an [[Open Cover]] of $X$, then there are [[Continuous]] [[Function]]s $\phi_{1},\ldots,\phi_{n}$ from $X$ into $\mathbb{R}$ such that:
>1. $0≤\phi_{k}(x)≤1$ for $1≤k≤n$
>2. $\phi_{k}(x)=0$ when $x\notin G_{k}$ and $1≤k≤n$
>3. $\sum_{k=1}^{n}\phi(x)=1$ for all $x\in X$

>[!proof] Proof by Induction
Base Case:
Assume $n=2$. Let $X=G_{1}\cup G_{2}$. $X-G_{1}$ is a [[Closed Set]] [[Set]] that is contained in $G_{2}$, so $X-(G_{1})\cap(X-G_2)$ are [[Disjoint]] [[Closed Set]] sets. By [[Urysohn's Lemma]], pick $\phi_{1}:X \rightarrow \mathbb{R}$ such that $\phi_{1}(a)=0$ for all $a\in X-G_{1}$ and $\phi_{1}(b)=1$ for all $b\in X-G_{2}$. Let $\phi_{2}=1-\phi_{1}$. By the [[Constructing Continuous Functions Theorem]], $\phi_2$ is [[Continuous]]. Clearly, $\phi_{1},\phi_{2}$ satisfy the conditions.
