---
tag: topology
mathLink: weak topology
---
>[!prop]
Let $X$ be a [[Set]], and let $\{X_{i}:i\in I\}$ be a [[Collection]] of [[Topological Space]]s. If, for each $i\in I$, $f_{i}:X \rightarrow X_{i}$ is a [[Function]] such that for distinct points $x,y\in X$ there is at least one [[Function]] $f_{i}$ with $f_{i}(x)≠f_{i}(y)$, then $$\mathcal{S}=\{f_{i}^{-1}(G):i\in I \text{ and }G \text{ is open in }X_{i}\}$$is a [[Subbasis]] for the *weak topology* on $X$. The weak [[Topology]] is the smallest of all topologies $\mathcal{U}$ on $X$ such that $f_{i}:(X,\mathcal{U})\rightarrow X_{i}$ is [[Continuous]] for each $i$.

>[!note]
>The [[Product Topology]] is a special case using the [[Projection]] maps for $f_{i}$. 