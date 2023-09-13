---
tag: topology
mathLink: local connectedness and basis proposition
---
>[!prop]
A [[Topological Space]] $X$ is [[Locally Connected]] [[iff]] it has a [[Basis]] for its [[Topology]] consisting of [[Connected]] [[Set]]s.

>[!proof]
Suppose $X$ is [[Locally Connected]]. For each $x\in X$, and each [[Neighborhood]] $U$ of $X$, pick $C\subseteq U$ such that $x\in C$ and $C$ is [[Open Set]] and [[Connected]]. Let $\mathcal{B}$ be the [[Collection]] of all these $C$s. Then, it can easily be shown that $\mathcal{B}$ is a [[Basis]]. Suppose there is a [[Basis]] for the [[Topology]] on $X$ consisting of [[Connected]] sets. Then, let $x\in X$ and $U$ be a [[Neighborhood]] of $X$. As $U$ is [[Open Set]], there is a [[Basis]] element $B\in \mathcal{B}$ with $x\in B\subseteq U$. As $B$ is [[Connected]], $X$ is [[Locally Connected]].