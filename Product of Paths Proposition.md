---
tag: topology
mathLink: product of paths proposition
---
>[!prop]
Let $X$ be a [[Topological Space]]. If $a,b,c\in X$, and $f$ is a [[Path]] from $a$ to $b$, and $g$ is a [[Path]] from $b$ to $c$, then $$h(t)=\left\{
\begin{align}
& f(2t)\text{ for } 0≤t< \frac{1}{2}\\
&g(2t-1) \text{ for } \frac{1}{2}<t≤1
\end{align}
\right.$$ is a [[Path]] in $X$ from $a$ to $c$, sometimes called the *product* path.

>[!proof]
>By the [[Pasting Lemma]], $h$ is [[Continuous]]. $h(0)=a$ and $h(1)=c$.
