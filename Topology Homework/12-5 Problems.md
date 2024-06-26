From 3.1: 1, 2, and 3

>[!note] 1
>
>>[!prop] Lemma
>If $f:\mathbb{N}\rightarrow \mathbb{R}$ is a [[Function]], then $f$ is [[Continuous]]. 
>
>>[!proof]
Give $\mathbb{N}$ the [[Discrete Topology]] and let $U\subseteq \mathbb{R}$ be [[Open Set]]. Then, $f^{-1}(U)$ is [[Open Set]] in $\mathbb{N}$, since all sets are [[Open Set]] in the [[Discrete Topology]]. Therefore, $f$ is [[Continuous]].
>
Clearly, $l^{\infty}\subseteq C_{b}(\mathbb{N})$, since [[Sequence]]s on $\mathbb{R}$ are just [[Function]]s from $\mathbb{N}\rightarrow \mathbb{R}$ and all such [[Function]]s are [[Continuous]]. Let $f\in C_{b}(\mathbb{N})$. Define $\{x_{n}\}$ by $x_{n}=f(n)$. Pick $M\in \mathbb{R}$ such that for all $n\in \mathbb{N}$, $f(n)\le M$. Then, $x_{n}=f(n)\le M$ for all $n$, so $x_{n}$ is a [[Bounded Function into R]] [[Sequence]]. Therefore, $\{x_{n}\}\in l^\infty$. 

>[!note] 2
Suppose $\{f_{n}\}$ is a [[Sequence]] in $C_b(X)$ such that there are constants $\{M_{n}\}$ with $|f_{n}(x)|≤M_{n}$ for all $n≥1$ and $\sum_{n=1}^{\infty}M_{n}<\infty$. 
>
Let $s_{n}=\sum_{k=1}^{n}M_{k}$. By assumption, $s_{n}$ [[Converges (net)]]s. So, $s_{n}$ is [[Cauchy Sequence]], since [[Convergent Sequences in Metric Spaces are Cauchy]]. 
>
Let $\epsilon>0$ be given. Pick $N$ such that for all $n,m≥N$, $|s_{n}-s_{m}|<\epsilon$. 
>
Let $n>m≥N$ be given. Then, $$|u_{n}(x)-u_{m}(x)|=\left|\sum_{k=m+1}^{n}f_{k}(x)\right|\le\sum_{k=m+1}^{n}|f_{k}(x)|\le\sum_{k=m+1}^{n}M_{k}=s_{n}-s_{m}<\epsilon$$
>
Since $u_{n}$ is a [[Uniformly Cauchy Sequence]], $u_{n}$ is [[Cauchy Sequence]] in $C_{b}(X)$. Since $C_{b}(X)$ is [[Complete]] ([[C_b(X) is Complete]]) and $u_{n}$ is [[Cauchy Sequence]], $u_{n}\rightarrow f\in C_{b}(X)$.

>[!note] 3
If $X$ is not [[Compactness]], it must have infinitely many elements. Otherwise, any [[Cover]] is finite, so it is a finite [[Subcover]]. Let $\{x_{1},x_{2},\ldots\}\subseteq X$ be an infinite set. Pick a [[Continuous]] [[Function]] $f:X \rightarrow \mathbb{R}$ such that $f(x_{i})=i\mod 1$ for all $i$ by [[Urysohn's Lemma]]. Continuously deform $f$ so that $f(x_{i})=i$ for odd $i$ (not sure how to formalize this). 

By the [[Characterizations of Compactness]], $X$ has an infinite [[Subset]] $A$ with no [[Limit Point]]s. Pick a [[Sequence]] $\{x_{n}\}\subseteq A$ with no [[Limit Point]]. For each $n$, pick $\epsilon_{n}$ such that $$B_{d}(x_{n},\epsilon_{n})\cap\{x_{n}:n\in \mathbb{N}\}=\{x_{n}\}$$and $$B_{d}(x_{n},\epsilon_{n})\cap B_{d}(x_{m},\epsilon_{m})=\emptyset $$For all $n$, $\text{cl }(B_{d}(x_{n},\frac{\epsilon_{n}}{2}))$ and $X-B_{d}(x_{n},\epsilon_{n})$ are [[Disjoint]] [[Closed Set]] [[Subset]]s. By [[Urysohn's Lemma]], there exist [[Continuous]] [[Function]]s $f_{n}:X \rightarrow \mathbb{R}$ such that $$f_{n}(x)=\begin{cases}1 & \text{if }x\in \text{cl }(B_{d}(x_{n},\frac{\epsilon_{n}}{2})) \\
0 & \text{if }x\in X-B_{d}(x_{n},\epsilon_{n})\end{cases}$$Define $f:x \rightarrow \mathbb{R}$ by $$f(x)=\begin{cases}nf_{n}(x) & \text{if }\exists n\in \mathbb{N}\text{ with }B_{d}(x_{n},\epsilon_{n}) \\
0 & \text{ otherwise }\end{cases}$$
$f$ is [[Continuous]] by the [[Pasting Lemma]].

