---
tag: topology
mathLink: path
---
>[!def]
>Let $X$ be a [[Topological Space]] and $p,q\in X$. A *path* or *arc* in $X$ from $p$ to $q$ is a [[Continuous]] [[Function]] $f:[0,1]\rightarrow X$ such that $f(0)=p$ and $f(1)=q$. 

>[!note]
>The use of the unit interval as the [[Domain]] of the path is arbitrary as there are [[Homeomorphism]]s between any [[Closed Set]] interval in $\mathbb{R}$ and the unit interval. 

Example:
1. If $p,q\in \mathbb{R}^n$, define $f:[0,1]\rightarrow \mathbb{R}^{n}$ by $f(t)=(1-t)p+tq$. This is the straight line path from $p$ to $q$
2. If $g:[0,1]\rightarrow X$ is any path, then $f:[0,1]\rightarrow \mathbb{R}\times X$ given by $f(t)=(t,g(t))$ is a path called the graph of $g$
