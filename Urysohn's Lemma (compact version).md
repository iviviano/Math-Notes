---
tag: topology
mathLink: Urysohn's lemma (compact version)
---
>[!thm]
>If $X$ is a [[Local Compactness]] [[Topological Space]], $K$ is a [[Compactness]] [[Subset]] of $X$, and $G$ is an [[Open Set]] [[Set]] that contains $K$, then there is a [[Continuous]] [[Function]] $f:X \mapsto [0,1]$ such that $f(x)=1$ for $x\in K$ and $f(x)=0$ for $x\notin G$.

>[!prop] Corollary
>A [[Local Compactness]] space is [[Completely Regular]]

>[!proof]
By the [[Characterizations of Local Compactness]], pick an [[Open Set]] $U$ such that $K\subseteq U\subseteq \text{cl }U\subseteq G$ with $\text{cl }U$ [[Compactness]]. As $\text{cl }U$ is a [[Compactness]] space, it is [[Normal Topological Space]] as [[Metric, Compact, and Sub- Spaces are Normal]]. Note that the [[Boundary]] $\partial U$ is [[Closed Set]] in $\text{cl }U$ as $\partial U=\text{cl }U-\text{int }U$ by the [[Interior, Closure, and Boundary Proposition]] and the [[Interior]] is [[Open Set]]. Note also that $K$ is [[Closed Set]] in $\text{cl }U$ as it is [[Compactness]] and [[Compactness]] sets are [[Closed Set]] by the [[Characterizations of Compactness]]. So, [[Urysohn's Lemma]] [[implies]] that there is a [[Continuous]] [[Function]] $f:\text{cl }U \mapsto [0,1]$ such that $f(x)=0$ for $x\in K$ and $f(x)=1$ for $x\in\partial U$. Letting $h:X-U \mapsto \mathbb{R}$ be identically $0$, the [[Pasting Lemma]] lets us construct the [[Continuous]] [[Function]] we wanted.