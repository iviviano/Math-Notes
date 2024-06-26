---
tag: topology, analysis
mathLink: Heine-Borel
---
>[!thm]
A [[Subset]] of $\mathbb{R}^{n}$ is [[Compactness]] [[iff]] it is [[Closed Set]] and [[Bounded Metric Space]].

>[!prop] Lemma
The [[Closed Set]] interval $[a,b]$ is [[Compactness]]. 
>>[!proof]
As a [[Closed Set]] [[Subset]] of a [[Complete]] [[Metric Space]] is [[Complete]] ([[Closed Subspaces are Complete]]), $[a,b]$ is [[Complete]]. It is clearly [[Totally Bounded]] and hence [[Compactness]] by the [[Characterizations of Compactness]].

>[!proof]
The forward implication is a special case of the [[Characterizations of Compactness]].

Let $K\subseteq \mathbb{R}^{n}$ be [[Closed Set]] and [[Bounded Metric Space]]. Let $a_{1},b_{1},a_{2},b_{2},\ldots,a_{n},b_{n}$ be such that $$K\subseteq[a_{1},b_{1}]\times[a_{2},b_{2}]\times\cdots\times[a_{n},b_{n}]$$Let $x_{n}\subseteq K$ be a [[Sequence]] with $x_{k}=(x_{k}^{1},x_{k}^{2},\ldots,x_{k}^{n})$. $\{x_{k}^{1}\}\in K$. Since $[a,b]$ is [[Compactness]], there is a [[Converges (Sequence)]]nt [[Subsequence]] $\{x_{k}^{1}:k\in\mathbb{N}_{1}\}$. Now consider 

Similarly, for each $i\in [n]$, pick a [[Converges (Sequence)]]nt [[Subsequence]] $\{x_{k}^{i}:k\in \mathbb{N}_{i}\}$. Let $$\mathbb{N}'=\bigcap_{i=1}^{n}\mathbb{N}_{i}$$
(Not correct )
Then, $\{x_{k}:k\in \mathbb{N}'\}$ is a [[Converges (Sequence)]]nt [[Subsequence]] of $x_{k}$ with [[Limit of a Sequence]] $x$ ([[9-7 Problems]]). Since $K$ is [[Closed Set]] and $x_{n}$ is contained in $K$, $x$ is a [[Limit Point]] of $K$, $x\in K$. So every [[Sequence]] in $K$ has a [[Converges (Sequence)]]nt [[Subsequence]]. [[therefore]] $K$ is [[Compactness]] by the [[Characterizations of Compactness]].