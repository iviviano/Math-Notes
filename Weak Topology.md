---
tag: topology
mathLink: weak topology
---
>[!prop]
Let $X$ be a [[Set]], and let $\{X_{i}:i\in I\}$ be a [[Collection]] of [[Topological Space]]s. If, for each $i\in I$, $f_{i}:X \rightarrow X_{i}$ is a [[Function]] such that for distinct points $x,y\in X$ there is at least one [[Function]] $f_{i}$ with $f_{i}(x)≠f_{i}(y)$, then $$\mathcal{S}=\{f_{i}^{-1}(G):i\in I \text{ and }G \text{ is open in }X_{i}\}$$is a [[Subbasis]] for the *weak topology* on $X$. The weak [[Topology]] is the smallest of all topologies $\mathcal{U}$ on $X$ such that $f_{i}:(X,\mathcal{U})\rightarrow X_{i}$ is [[Continuous]] for each $i$.

>[!proof]
For the first [[Subbasis]] condition, simply observe that $X_{i}$ in $X_{i}$ is [[Open Set]] and the [[Preimage]] $f^{-1}_{i}(X_{i})=X$. For the Hausdorff condition, let $x≠y\in X$. There is an $i\in I$ such that $f_{i}(x)≠f_{i}(y)$. Since $X_{i}$ is a [[Hausdorff Space]], there are [[Disjoint]] [[Neighborhood]]s $U$ of $f(x)$ and $V$ of $f(y)$. Then, $f^{-1}_{i}(U)$ and $f^{-1}_{i}(V)$ are nonempty, [[Disjoint]] in $S$ and separate $x,y$. So, $\mathcal{S}$ is a [[Subbasis]].
>
Let $\mathcal{U}$ be a [[Topology]] on $X$ for which all $f_{i}$ are [[Continuous]]. Then, $H$ [[Open Set]] in $X_i$ implies $f_{i}^{-1}(H)\in \mathcal{U}$. This implies $\mathcal{S}\subseteq \mathcal{U}$. Therefore, the weak topology is contained in $\mathcal{U}$.

>[!prop] Corollary
If $g:Z \rightarrow X$ is given, then $g$ is [[Continuous]] [[iff]] $f_{i}\circ g$ is [[Continuous]] for all $i\in I$.

>[!proof]
If $g$ is [[Continuous]], then the implication holds by the [[Constructing Continuous Functions Theorem]].
>
If $g\circ f_{i}$ is [[Continuous]] for all $i$, let $\mathcal{W}$ be the [[Topology]] on $Z$. Let $G$ be [[Open Set]] in $X_{i}$. Then, $(f_{i}\circ g)^{-1}(G)=W\in \mathcal{W}$. $f^{-1}_{i}(G)$ is an arbitrary [[Subbasis]] element. And $$(f_{i}^{-1}\circ g)^{-1}(G)=g^{-1}(f_{i}^{-1}(G))$$so, the [[Preimage]] under $g$ of every [[Subbasis]] element is [[Open Set]]. So, $g$ is [[Continuous]] by the [[Basis and Subbasis Formulation of Continuity]].


>[!note]
>The [[Product Topology]] is a special case using the [[Projection]] maps for $f_{i}$. 
