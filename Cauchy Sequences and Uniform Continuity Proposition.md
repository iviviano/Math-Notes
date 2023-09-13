---
tag: topology
mathLink: Cauchy sequences and uniform continuity proposition
---
>[!prop]
Let $(X,d_{X}),(Y,d_{Y})$ be [[Metric Space]]s.
>1. If $f:X \rightarrow Y$ is a [[Uniform Continuity]] [[Function]], and $\{x_{n}\}$ is a [[Cauchy Sequence]] [[Sequence]] in $X$, then $f(x_{n})$ is a [[Cauchy Sequence]] [[Sequence]] in $Y$.
>2. If $A\subseteq X$ and $Y$ is [[Complete]], and $f:A \rightarrow Y$ is [[Uniform Continuity]], then $f$ can be extended to a [[Uniform Continuity]] [[Function]] $f:\bar{A}\rightarrow Y$.

Let $\epsilon>0$ be given. Pick $\delta>0$ such that for all $x,y\in X$, $d_{X}(x,y)<\delta$ [[implies]] $d_{Y}(f(x),f(y))<\epsilon$. Then, pick $N\in \mathbb{N}$ such that for $n,m≥N$, $d_{X}(x_{n},x_{m})<\delta$. Clearly, if $n,m≥N$, $d_{Y}(f(x_{n}),f(x_{m}))<\epsilon$, so $f(x_{n})$ is [[Cauchy Sequence]].

If $x\in \bar{A}$, then there is a [[Sequence]] $\{a_{n}\}$ in $A$ such that $a_{n}\rightarrow x$. As any [[Sequence]] that [[Converges (Sequence)]]s is [[Cauchy Sequence]] ([[Convergent Sequences in Metric Spaces are Cauchy]]), $a_{n}$ is a [[Cauchy Sequence]] [[Sequence]]. By 1., $f(a_{n})$ is [[Cauchy Sequence]] in $Y$. As $Y$ is [[Complete]], $f(a_{n})\rightarrow y\in Y$. Set $f(x)=z$.
>[!note] Note: show $y$ is independent of which sequence $a_{n}$ is 

