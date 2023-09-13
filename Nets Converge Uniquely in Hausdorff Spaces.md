---
tag: topology
mathLink: nets converge uniquely in Hausdorff spaces
---
>[!thm]
Let $X$ be a [[Topological Space]]. Let $\{x_{i}\}$ be a [[Net]] in $X$. Then,
>1. If $x_{i}$ [[Converges (net)]] to $x$ then $x_{i}$ [[Clusters]] at $x$
>2. If $X$ is a [[Hausdorff Space]], then if $x_{i}$ [[Converges (net)]]s, it [[Converges (net)]]s uniquely

>[!proof]
Suppose $x_{i}\rightarrow x$. Let $U$ be a [[Neighborhood]] of $x$ and pick $i_{0}\in I$ such that if $i≥i_{0}$ $x_{i}\in U$. Let $j\in I$ be given. Let $i\in I$ with $i≥j,i_{0}$. Then, $x_{i}\in U$, so $x_{i}$ [[notation for clusters]] $x$.
>
Suppose $x_{i}\rightarrow x$ and $x_{i}\rightarrow y$. Suppose $x≠y$. Then, pick [[Disjoint]] [[Neighborhood]]s $U$ and $V$ of $x$ and $y$, respectively. Pick $i_{1}\in I$ such that if $i_{1}≤i\in I$, $x_{i}\in U$. Pick $i_{2}\in I$ such that if $i_{2}≤i\in I$, $x_{i}\in V$. Then let $i≥i_{1},i_{2}$. $x_{i}\in U,V$ so $U$ and $V$ are not [[Disjoint]]. [[therefore]] $x=y$.
