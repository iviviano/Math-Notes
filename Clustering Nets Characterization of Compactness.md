---
tag: topology
mathLink: clustering nets characterization of compactness
---
>[!thm]
>A [[Topological Space]] $X$ is [[Compactness]] [[iff]] every [[Net]] in $X$ has a [[Clusters]] point.

>[!proof]
Let $X$ be [[Compactness]] and let $x_{i}$ be a [[Net]] in $X$. Given $j\in I$, let $F_{j}=\text{cl }\{x_{i}:i≥j\}$. If $j_{1},\ldots,j_{n}\in I$, then there exists $i≥j_{k}$ for all $k=1,\ldots,n$. For this $i$, $$x_{i}\in\bigcap_{k=1}^{n}F_{j_{k}}$$So, $\{F_{i}:i\in I\}$ has the [[Finite Intersection Property]]. Since $X$ is [[Compactness]], there exists $x\in \bigcap\{F_{i}\}$. If $U$ is a [[Neighborhood]] of $x$ and $i_{0}\in I$ and $x\in F_{i_{0}}$, hence $U\cap\{x_{i}:i≥i_{0}\}≠\emptyset$ since [[Open Sets Intersecting the Closure Intersect the Set Theorem]]. So, there exists $i≥i_{0}$ and $x_{i}\in U$. Therefore, $x_{i}$ [[notation for clusters]] $x$.
>
Assume every [[Net]] in $X$ has a [[Clusters]] point. Suppose $X$ is not [[Compactness]] and let $\mathcal{U}$ be an [[Open Cover]] of $X$ with no finite [[Subcover]]. Let $I$ be the [[Set]] of all finite [[Subset]]s of $\mathcal{U}$ [[Directed Set]] by inclusion. By assumption, for all $i\in I$, there exists $x_{i}\in X$ such that $x_{i}\notin$ the [[Subcover]] $i$. $x_{i}$ is a [[Net]]. If $x$ is a [[Clusters]] point of $x_i$, then there exists $U\in \mathcal{U}$ such that $x\in U$ by the definition of a [[Cover]]. However, $\{U\}\in I$. So, if $j=i\cup\{U\}$, $x_{i}\notin$ the [[Subcover]] $j$. This is a contradiction, so $X$ must be [[Compactness]]
