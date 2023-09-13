---
tag: topology
mathLink: completely regular subspaces proposition
---
>[!prop]
If $X$ is [[Completely Regular]] and $Y$ is a [[Subset]] of $X$ and has the [[Subspace Topology]], then $Y$ is a [[Completely Regular]].

>[!proof]
Let $D$ be a [[Closed Set]] [[Subset]] of $Y$, and let $y\in Y-D$. There is a [[Closed Set]] [[Subset]] $F$ of $X$ such that $D=F\cap Y$. So, $y\notin F$. As $X$ is [[Completely Regular]], there is a [[Continuous]] [[Function]] $f:X \rightarrow \mathbb{R}$ such that $f(y)=0$ and $f(x)=1$ for all $x\in F$. So, $f|Y$ is [[Continuous]] by the [[Constructing Continuous Functions Theorem]]. Additionally, $f|Y(x)=1$ for all $x\in D$. So, $Y$ is [[Completely Regular]].
