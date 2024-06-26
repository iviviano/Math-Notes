---
tags:
  - topology
mathLink: basis characterization of compactness
---
>[!prop]
>If $\mathcal{B}$ is a [[Basis of a Topology]] for $X$, then $K$ is [[Compactness]] [[iff]] every [[Subset]] of $\mathcal{B}$ that [[Cover]]s $A$ omits a finite [[Subcover]].

>[!proof] Proof of Equivalence
>If $K$ is [[Compactness]], as $\mathcal{B}\subseteq T$, any [[Subset]] of $\mathcal{B}$ that [[Cover]]s $K$ is an [[Open Cover]] and must omit a finite [[Subcover]]. 
>
>Suppose any subset of $\mathcal{B}$ that [[Cover]]s $K$ omits a finite [[Subcover]]. Let $\mathcal{U}$ be an [[Open Cover]] of $K$. As $\mathcal{B}$ is a [[Basis of a Topology]], for each $U\in \mathcal{U}$ there is a [[Subset]] $\mathcal{B}_{U}$ of $\mathcal{B}$ such that $$U=\bigcup\{B:B\in \mathcal{B}_U\}$$ 
Let 
$$\mathcal{B}'=\{B\in \mathcal{B}_U|U\in \mathcal{U}\}$$ 
Clearly, $\mathcal{B}'$ [[Cover]]s $K$. So by assumption, there is a finite [[Subset]] of $\mathcal{B}'$ that [[Cover]]s $K$, as $\mathcal{B}'\subseteq \mathcal{B}$. Let $B_{1},\ldots,B_{k}\in \mathcal{B}'$ be an [[Open Cover]] of $K$. Then, there are $U_{1},\ldots,U_{k}\in \mathcal{U}$ such that $B_{k}\subseteq U_{k}$, so $U_{1},\ldots, U_{k}$ is a finite [[Subcover]] of $K$.
