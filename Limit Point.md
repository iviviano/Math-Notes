---
tag: topology
mathLink: limit point
---
> [!def]
> If [[topological space]] is a [[Topological Space]] and $x\in X$, we say $x$ is a *limit point* of $A$ if every [[Neighborhood]] of $x$ [[Intersects]] $A$ at some point other than $x$ itself:
> $$\forall U\in T: x\in U: (A - \{x\})\cap U \ne \emptyset$$
> 
> Equivalently, $x$ is a limit point of $A$ if it belongs to the [[Closure]] of $A - \{x\}$.

>[!prop] Sequential Characterization of Limit Points
>Let $(X,d)$ be a [[Metric Space]], let $A\subseteq X$. Then, $x$ is a [[Limit Point]] of $A$ [[iff]] there is a [[Sequence]] of points in $A$ [[Converges (Sequence)]]ing to $x$.

>[!proof]
Suppose $x$ is a [[Limit Point]] of $A$. For each $n\in \mathbb{N}$, pick $x_{n}\in B_{d}(x,{\epsilon_{n}})\cap A$ where $\epsilon_{1}=1$ and $\epsilon_{n}=\frac{d(x,x_{n-1})}{n}$ for $n≥2$. Then $x_{n}\rightarrow x$. Suppose there is a [[Sequence]] $\{x_{n}\}$ of distinct points in $X$ such that $x_{n}\rightarrow x$. Then, for all $\epsilon>0$, $\exists N\in \mathbb{N}$ such that if $n≥N$, $d(x_{n},x)<\epsilon$, so $x_{n}\in B_{d}(x,\epsilon)$. [[therefore]] $x$ is a limit point of $F$.


Examples:
1. $X=\mathbb{R}$, $A=(0,1)\cup\{2\}$. Then the limit points of $A$ are $[0,1]$. Note: $2$ is an [[Isolated Point]]
2. $X=\mathbb{R}$, $A=\mathbb{Q}$. Then the [[Limit Point]]s of $A$ are $\mathbb{R}$. $\text{int }A=\emptyset$. $\text{cl }A=\mathbb{R}$.
3. $X=\mathbb{R},A=\{\frac{1}{n}:n\in \mathbb{N}\}$. Then the limit points of $A$ are $\{0\}$. $\text{int }A=\emptyset$. $\text{cl }A=A\cup\{0\}$
4. 