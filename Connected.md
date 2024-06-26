---
tag: topology
mathLink: connected
---
>[!def]
>Let $X$ be a [[Topological Space]]. Then, $X$ is *connected* if only $\emptyset$ and $X$ are both [[Open Set]] and [[Closed Set]] in $X$. A [[Subset]] $A$ of $X$ is *connected* if the [[Subspace]] $A$ is connected.

>[!def]
>$X$ is *connected* whenever $X=A\cup B$, where $A$ and $B$ are both [[Open Set]] or both [[Closed Set]], and $A\cap B=\emptyset$, then $A=\emptyset$ or $B=\emptyset$.

Examples:
1. $X=[0,1]\cup(2,3)\subseteq \mathbb{R}$. Not connected: $A=[0,1],B=(2,3)$
2. $\mathbb{Q}\subseteq \mathbb{R}$. Not connected: $A=(-\infty,\sqrt{2}),B=(\sqrt{2},\infty)$
3. $\text{GL}_{n}(\mathbb{R})=\{\text{invertible }n\times n \text{ matrices over }\mathbb{R}\}$ is not connected. $\text{GL}_{n}(\mathbb{R})\subseteq \mathbb{R}^{n^{2}}$. Define $\text{det}:GL_{n}(\mathbb{R})\mapsto \mathbb{R}$ to be the [[Determinant]]. Note: $\text{det}$ is [[Continuous]]. Let $A=\det^{-1}((0,\infty)),B=\det((-\infty),0)$. Also, $\text{GL}_{n}(\mathbb{R})=A\cup B$ as a [[Matrix]] is [[Invertible Matrix]] [[iff]] it's determinant is nonzero. $A,B$ are both [[Open Set]] as $\det$ is [[Continuous]]. 
4. $\text{O}_{n}(\mathbb{R})=\{n\times n \text{ orthogonal matrices }\}=\{A:AA^{T}=I\}$. $\text{O}_{n}(\mathbb{R})\subseteq \mathbb{R}^{n^{2}}$ is [[Bounded Metric Space]] as its columns are an [[Orthonormal Basis]]. $\text{O}_{n}(\mathbb{R})$ is [[Closed Set]]. [[therefore]] $\text{O}_{n}(\mathbb{R})$ is [[Compactness]] by the [[Heine-Borel Theorem]].
