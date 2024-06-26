---
tags:
  - topology
mathLink: pathwise connected implies connected
---

>[!prop]
>(a) If $X$ is a [[Pathwise Connectedness]] [[Topological Space]], then $X$ is [[Connected]]
>(b) If $X$ is [[Pathwise Connectedness]] and $f:X \rightarrow Y$ is a [[Continuous]] [[Surjective]] [[Function]], then $Y$ is [[Pathwise Connectedness]].

>[!proof]
(a) If $X$ is not [[Connected]], there are [[Disjoint]] [[Open Set]] [[Set]]s $A,B$ such that $X=A\cup B$. Let $a\in A$ and $b\in B$. If $f:[0,1]\rightarrow X$ is a [[Path]] from $a$ to $b$, then $f^{-1}(A)$ and $f^{-1}(B)$ are [[Open Set]] [[Set]]s with [[Union]] $[0,1]$. This contradicts the [[Connected]]ness of the interval ([[Intervals are Connected in R]]). Therefore, $X$ is [[Connected]].