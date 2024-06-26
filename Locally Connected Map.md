---
tag: topology
mathLink: locally connected map proposition
---
>[!prop]
>If $X,Y$ are [[Topological Space]]s with $X$ [[Locally Connected]] and $f:X \rightarrow Y$ [[Continuous]], [[Open Map]], and [[Surjective]], then $Y$ is [[Locally Connected]].

>[!proof]
Let $y\in Y$ and let $V$ be a [[Neighborhood]] of $Y$. Pick a point $x\in X$ with $f(x)=y$ ([[Surjective]]). Then $U=f^{-1}(V)$ is [[Open Set]], so there is a [[Connected]] [[Neighborhood]] $A$ of $x$. As $f$ is [[Open Map]], $f(A)$ is [[Open Set]], so $B=f(A)$ is a [[Neighborhood]] of $y$ contained in $V$. As [[Continuous]] [[Function]]s map [[Connected]] sets to [[Connected]] sets ([[Intermediate Value Theorem]]), $B$ is [[Connected]] in $Y$.

>[!note]
>Need [[Surjective]] so that every point of $Z$ in [[Image Set]] (to show [[Locally Connected]]).
