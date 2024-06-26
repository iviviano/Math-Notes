---
tag: topology
mathLink: Tietze's expansion theorem (compact version)
---
>[!thm]
>If $X$ is a [[Local Compactness]] [[Topological Space]], $K$ is a [[Compactness]] [[Subset]] of $X$, $G$ is an [[Open Set]] [[Set]] containing $K$, and $f:K \mapsto [0,1]$ is a [[Continuous]] [[Function]], then there is a [[Continuous]] [[Function]] $F:X \mapsto [0,1]$ such that $F(x)=f(x)$ for $x\in K$ and $F(x)=0$ when $x\notin G$.

>[!proof]
Pick an [[Open Set]] set $U$ such that $K\subseteq U\subseteq \text{cl }U\subseteq G$ and $\text{cl }U$ is [[Compactness]] by the [[Characterizations of Local Compactness]]. As $\text{cl }U$ is [[Compactness]], it is a [[Normal Topological Space]] as [[Metric, Compact, and Sub- Spaces are Normal]]. Additionally, $K$ is a [[Closed Set]] [[Subset]] of $\text{cl }U$ as [[Compactness]] [[Set]]s are [[Closed Set]] ([[Characterizations of Compactness]]). By [[Tietze's Expansion Theorem]], pick a [[Continuous]] [[Function]] $F':\text{cl }U \mapsto [0,1]$ such that $F'(x)=f(x)$ for all $x\in K$ and $F'(x)=0$ when $x\in\partial U$ (WHY?), a [[Closed Set]] [[Set]] by the [[Interior, Closure, and Boundary Proposition]]. The [[Pasting Lemma]] ...