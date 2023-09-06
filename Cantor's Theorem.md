---
tag: topology
mathLink: Cantor's theorem
---
>[!thm]
>A [[Metric Space]] $(X,d)$ is [[Complete]] [[iff]] whenever $\{F_{n}\}$ is a [[Sequence]] of nonempty [[Subset]]s of $X$ satisfying:
>- $F_{n}$ is [[Closed Set]] for $n\in \mathbb{N}$
>- $F_{n}$ [[notation for subset]] $F_{n-1}$ for $n≥1$
>- $\text{diam}(F_n)\rightarrow0$ 
> 
>the [[Intersection]]:
>$$\bigcap_{n\in \mathbb{N}}F_{n}$$
>is a single point in $X$.

>[!proof]
>Suppose $X$ is [[Complete]], and let $\{F_{n}\}$ be a [[Sequence]] satisfying the conditions above. Let $x,y\in\cap F_{n}$. Then, if $x\ne y$, $d(x,y)=\epsilon>0$, as $d$ is a [[Metric]]. But, there exists $N\in \mathbb{N}$ such that if $n≥N$, $\text{diam}(F_{n})<\epsilon$. Therefore, $x\notin F_{N}$ or $y\notin F_\mathbb{N}$.
>[[therefore]] there can be no more than one point in the [[Intersection]]. 
>Let $\{x_{n}\}$ be a [[Sequence]] in $X$ with $x_{n}\in F_{n}$. Then, $x_{n}$ is [[Cauchy Sequence]] (PROOF!). As $X$ is [[Complete]], $x_{n}\rightarrow x\in X$. As $F_{n}\subseteq F_{n-1}$, $\{x_k\}_{k=n}^\infty$ is a [[Subsequence]] in $F_{n}$. As $x_{n}\rightarrow x$, $\{x_k\}_{k=n}^\infty$ [[Converges]]s to $x$ as [[Subsequences of Convergent Sequences Converge]]. Since $x$ is the [[Limit of a Sequence]] of a [[Sequence]] in $F_n$, $x$ is a [[Limit Point]] of $F_{n}$ by the [[Limit Points and Convergent Sequences Lemma]]. 
>[[therefore]] $x\in F_{n}$ for all $n\in \mathbb{N}$ as [[Closed Sets in Metric Spaces contain their Limit Points]]. 
>[[therefore]] The [[Intersection]] $\cap F_{n}$ is a single point in $X$.
> 
>Suppose every [[Sequence]] $F_{n}$ satisfies the conditions above. Let $\{x_n\}$ be a [[Cauchy Sequence]] [[Sequence]] in $X$. Then, let 
>$$\epsilon_{n}=\sup\{d(x_{n},x_{m}):m≥n\}$$
>and 
>$$F_{n}=\text{cl}(B_{d}(x_{n},\epsilon_{n}))$$
>Then, each $F_{n}$ is nonempty, [[Closed Set]], and contains $x_{n}$. Additionally, $F_{n}\subseteq F_{n-1}$. (PROOF!). 
>













