---
tag: topology
mathLink: characterizations of local compactness proposition
---
>[!prop]
>1. If $X$ is a [[Topological Space]], then $X$ is [[Local Compactness]] [[iff]] for every point $x\in X$ there is a [[Neighborhood]] $G$ of $x$ such that $\text{cl }G$ is [[Compactness]].
>2. If $X$ is a [[Local Compactness]] [[Topological Space]] and $E\subseteq X$ such that $E$ is either [[Open Set]] or [[Closed Set]], then the [[Subspace]] $E$ is [[Local Compactness]].
>3. If $\{X_{i}\}$ is a [[Collection]] of [[Topological Space]]s and $X=\prod X_{i}$, then $X$ is [[Locally Connected]] [[Compactness]] [[iff]] each $X_{i}$ is [[Local Compactness]] and all but a finite number of spaces $X_{i}$ are [[Compactness]].
>4. If $(X,d)$ is a [[Metric Space]], then $X$ is [[Local Compactness]] [[iff]] for every $x\in X$ there is an $\epsilon>0$ such that $\text{cl }B_{d}(x,\epsilon)$ is [[Compactness]].
>5. If $X$ is a [[Local Compactness]] space, $K$ is a [[Compactness]] [[Subset]] of $X$ and $G$ is an [[Open Set]] [[Set]] that contains $K$, there is an [[Open Set]] set $U$ such that $K\subseteq U\subseteq \text{cl }U\subseteq G$ and $\text{cl }U$ is [[Compactness]].

>[!proof]
(1) Clearly, if $X$ is [[Local Compactness]], every point has a [[Neighborhood]] whose [[Closure]] is [[Compactness]].
>
Suppose the implication of 1. Let $x\in X$ be given. Pick a [[Neighborhood]] $G$ of $x$ such that $\text{cl }G$ is [[Compactness]]. Let $U$ be a [[Neighborhood]] of $x$. If $\text{cl }G\subseteq U$, then clearly $X$ is [[Local Compactness]]. Otherwise $U\subseteq G$. So, $\text{cl }U\subseteq \text{cl }G$. If $V$ is a [[Neighborhood]] of $x$ with $\text{cl }V\subseteq U$,  $\text{cl }V$ is [[Compactness]] as [[Closed Set]] [[Subset]]s of [[Compactness]] [[Set]]s are [[Compactness]] ([[Characterizations of Compactness]]) and $\text{cl }V\subseteq \text{cl }G$. ...
>
(2) Let $E$ be a [[Closed Set]] [[Subset]] of $X$. Let $x\in E$ be given. Pick a [[Neighborhood]] $G$ of $x$ such that $x\in G$ and $\text{cl }G$ is [[Compactness]]. Then, $E\cap \text{cl }G$ is a [[Closed Set]] [[Subset]] of a [[Compactness]] [[Set]], so it is [[Compactness]] by the [[Characterizations of Compactness]]. As $E\cap G$ is a [[Neighborhood]] of $x$ in $E$ and $E\cap \text{cl }G$ is [[Closed Set]] in $G$, $E$ is [[Local Compactness]] by (1).
>
Let $E$ be an [[Open Set]] [[Subset]] of $X$.
>
(3)
>
(4) Suppose the implication of 4. By (1), $x$ is [[Local Compactness]].
>
(5) Let $G$ be an [[Open Set]] set containing $K$. For each $x\in K$, pick a [[Neighborhood]] $U_{x}$ of $x$ such that $\text{cl }U$ is [[Compactness]] and contained in $G$. As $\{U_{x}\}$ is an [[Open Cover]] of $K$, pick a finite [[Subset]] of $K$, $D$ such that $\{U_{x}:x\in D\}$ is a [[Subcover]] of $K$. Then, $$\bigcup_{x\in D}\text{cl }U_{d}=\text{cl }\left(\bigcup_{x\in D}U_{d}\right)$$by the [[Interior, Closure, and Boundary Proposition]]. So if $U=\bigcup_{x\in D}U_{d}$, $K\subseteq U\subseteq \text{cl }U\subseteq G$. WHY IS U COMPACT?
