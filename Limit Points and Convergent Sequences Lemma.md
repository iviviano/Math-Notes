---
tag: topology
mathLink: 
---
>[!prop]
>Let $(X, d)$ be a [[Metric Space]], let $A$ [[notation for subset]] $X$. Then,
>1. A point $x$ is a [[Limit Point]] of $A$ [[iff]] there is a [[Sequence]] of distinct points in $A$ that [[Converges (Sequence)]] to $x$.
>2. $A$ is a [[Closed Set]] [[Set]] [[iff]] $A$ contains all its [[Limit Point]]s ([[Closed Sets in Metric Spaces contain Sequence Limits]])
>3. [[notation for closure]] $=A\cup\{x:x \text{ is a a limit point of }A\}$. ([[Closure Contains All Limit Points Theorem]])

>[!proof]
>Let $x$ be a [[Limit Point]] of $A$. Then pick $\epsilon>0$ such that 
>$$B_{d}(x,\epsilon)\cap(A-x)\ne \emptyset$$
>Then, pick $\epsilon_{0}\in B_{d}(x,\epsilon)\cap (A-x)$. Similarly, for each $n\in \mathbb{N}-\{0\}$, pick $\epsilon_{n}>0$ such that
>$$\epsilon_{n}+x\in B_{d}(x,\epsilon_{n-1})\cap(A-x)$$
>Then, for each $n$, $\epsilon_{n}+x\in A$ and $\epsilon_n$ is unique. As $\epsilon_{n} \rightarrow0$, if $x_{n}=x+\epsilon_{n}$, $x_{n}\rightarrow x$, and $x_{n}$ is unique.
>Suppose $x_{n}$ is a [[Sequence]] of unique points with $x_{n}\rightarrow x$. Then, for each $n$, there is a [[Neighborhood]] of $x_{n}$ that contains $x$. So for all $\epsilon>0$, there is an $n$ such that $B_{d}(x,\epsilon)$ contains $x_{n}\in A$. [[therefore]] $x$ is a [[Limit Point]] of $A$ (needs work)
>
