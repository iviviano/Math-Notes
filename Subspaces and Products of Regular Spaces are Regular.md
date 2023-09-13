---
tag: topology
mathLink: subspaces and products of regular topologies are regular
---
>[!prop]
>1. If $X$ is [[Regular]] and $A\subseteq X$ is given the [[Subspace Topology]], $A$ is [[Regular]].
>2. If $X=\prod X_{i}$ then $X$ is [[Regular]] under the [[Product Topology]] [[iff]] each $X_{i}$ is [[Regular]]

>[!proof]

(1) Let $X$ be a [[Regular]] [[Topological Space]], let $A\subseteq X$. Let $F$ be a [[Closed Set]] in $A$. Then, there is a [[Closed Set]] set $F'\subseteq X$ such that $F=F'\cap A$. Let $x\in A-F'$ be given. Pick $U,V$ [[Open Set]] in $X$ such that if $x\in U$ and $F'\subseteq V$. Then, $x\in U\cap A$, which is [[Open Set]] in $A$. $F=F'\cap A\subseteq V\cap A$ which is [[Open Set]] in $A$. [[therefore]] $A$ is [[Regular]].

(2) Let $X$ be a [[Regular]] 