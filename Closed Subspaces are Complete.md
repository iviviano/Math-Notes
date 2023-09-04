---
tag: topology
mathLink: closed subspaces are complete
---
>[!prop]
>Let $(X,d)$ be a [[Complete]] [[Metric Space]], $Y\subseteq X$. Then, the [[Subspace]] $Y$ is [[Complete]] [[iff]] $Y$ is [[Closed Set]] in $X$. 

>[!proof]
>Suppose $Y$ is [[Complete]]. Then, every [[Cauchy Sequence]] [[Sequence]] in $Y$ [[Converges]] in $Y$. Let $x\in X$ be a [[Limit Point]] of $Y$. Then, there is a [[Sequence]] in $Y$: $\{y_n\}$ such that $y_{n}\rightarrow x$. As $y_{n}$ [[Converges]], $y_{n}$ is [[Cauchy Sequence]] as [[Convergent Sequences in Metric Spaces are Cauchy]]. 
>[[therefore]] $x\in Y$, so $Y$ contains all its [[Limit Point]]s and is [[Closed Set]] as [[Closed Sets in Metric Spaces contain their Limit Points]].
>
>Suppose $Y$ is [[Closed Set]] in $X$. Let $\{y_{n}\}$ be a [[Cauchy Sequence]] sequence in $Y$. Then $y_{n}\rightarrow x\in X$. As $Y$ is [[Closed Set]] and $x$ is a [[Limit Point]] of $Y$, $y\in Y$ as [[Closed Sets in Metric Spaces contain their Limit Points]].
>[[therefore]] $Y$ is [[Complete]]
