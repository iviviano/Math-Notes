---
tag: topology
mathLink: metric space
---
> [!def]
> A *metric space* is a [[Metrizable]] [[Topological Space]] $X$ together with a specific [[Metric]] $d$ that induces the [[Metric Topology]] of $X$.

Examples:
1. $X=\mathbb{R}$, $d(x, y) = |x - y|$
	1. $|x-y|=|y-x|$
	2. $|x-y|=0$ [[implies]] $x - y=0, x=y$; if $x=y$, then $x-y=0$, and $y-x=0$, so $|x-y|=\max(x-y, y-x)=\max(0,0)=0$
	4. $|x-y|\le |x-z|+|z-y|$ by cases:
		1. Suppose $x>z$, $z>y$. Then, $|x-z|+|z-y|=x-z+z-y=x-y$. 
Therefore, $d$ is a [[Metric]] on $\mathbb{R}$, so $(\mathbb{R},d)$ is a [[Metric Space]] 
1. 

Lemma: The Triangle Inequality $$\forall x,y,z\in \mathbb{R}:|x-y|\le|x-z|+|y-z|$$
Proof:
Case 1: $x\ge y$: $$|x-y|=x-y=x-z+z-y\le|x-z|+|z-y|=|x-z|+|y-z|$$
Case 2: $x<y$: $$|x-y|=y-x=z-x+y-z\le|z-x|+|y-z|=|x-z|+|y-z|$$
Corollary: $$\begin{equation}
|A+B|\le|A|+|B|
\end{equation}$$
Proof: simply apply the triangle inequality with $x=A,y=-B,z=0$.