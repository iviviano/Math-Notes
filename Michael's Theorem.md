---
tag: topology
mathLink: Michael's theorem
---
>[!thm]
>If $X$ is a [[Regular]] [[Topological Space]] such that every [[Open Cover]] of $X$ has a [[Refinement]] [[Cover]] $\mathcal{A}=\bigcup_{n=1}^{\infty}\mathcal{A}_{n}$ where each $A_{n}$ is a [[Locally Finite]] [[Collection]], then $X$ is [[Paracompact]].

>[!prop] Corollary
>A [[Separable]] [[Metric Space]] is [[Paracompact]].
>>[!proof]
As $X$ is [[Separable]], it has a countable [[Dense]] [[Subset]]. Enumerate the elements: $\{q_{0},q_{1},\ldots\}$. Let $\mathcal{U}$ be an [[Open Cover]] of $X$. For each $n\in \mathbb{N}$, pick an element $U$ of $\mathcal{U}$ that is a [[Neighborhood]] of $q_{n}$. Pick $\epsilon_{n}>0$ such that $q\in B_{d}(q,\epsilon)\subseteq U$. Letting $\mathcal{A_{n}}=\{B_{d}(q_{n},\epsilon_{n})\}$, $\mathcal{A}=\bigcup_{n=1}^{\infty}\mathcal{A}_{n}$ is a [[Refinement]] [[Cover]] of $U$. Each $\mathcal{A_{n}}$ is a [[Locally Finite]] [[Collection]] as it contains only one element. [[therefore]] $X$ is [[Paracompact]].

>[!prop] Corollary
>If $X$ is a [[Regular]] [[Sigma-Compact]] [[Topological Space]], then $X$ is [[Paracompact]]. 

>[!prop] Lemma
>If $X$ is a [[Topological Space]] such that every [[Open Cover]] of $X$ has a [[Locally Finite]] [[Closed Set]] [[Cover]] that is a [[Refinement]], then $X$ is [[Paracompact]].
>>[!proof] Incomplete Proof
Let $\mathcal{U}$ be an [[Open Cover]] of $X$. Then, there is a [[Locally Finite]] [[Closed Set]] [[Cover]] $\mathcal{F}$ of $X$ that is a [[Refinement]]. So, for every $x\in X$, there is a [[Neighborhood]] $U_{x}$ of $x$ such that $U$ [[Intersects]] only finitely many elements of $\mathcal{F}$. Note: $\mathcal{W}=\{U_{x}\}$ is an [[Open Cover]] of $X$. Pick another [[Locally Finite]] [[Closed Set]] [[Cover]] $\mathcal{D}$ of $X$ that is a [[Refinement]] of $\mathcal{W}$. Now, for each $F\in \mathcal{F}$, $$V_{F}=X-\bigcup \{C:C\in \mathcal{D}\text{ and }C\cap F=\emptyset\}$$Note: $V_{F}$ is [[Open Set]] and $F\subseteq V_{F}$, so $\mathcal{V}=\{V_{f}:F\in \mathcal{F}\}$ is an [[Open Cover]] of $F$.

