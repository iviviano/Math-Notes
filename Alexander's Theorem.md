---
tag: topology
mathLink: Alexander's theorem
---
>[!thm]
>If $X$ is a [[Topological Space]] and $\mathcal{S}$ is a [[Subbasis]] for the [[Topology]] on $X$, then $X$ is [[Compactness]] [[iff]] every [[Cover]] by [[Set]]s from $\mathcal{S}$ has a finite [[Subcover]].

>[!proof]
The proof of the forward implication follows trivially from the definition of [[Compactness]].
>
Assume $X$ is not compact. Let $\Gamma$ be the [[Collection]] of all [[Open Cover]]s of $X$ with no finite [[Subcover]]. Then, $\Gamma$ is a [[Partially Ordered Set]] [[Set]] with respect to inclusion. If $\Lambda$ is a [[Chain]] in $\Gamma$, then $V=\bigcup\{W\in \Lambda\}$ is an [[Open Cover]] of $X$ with no finite [[Subcover]] (see proof of vector space result). Thus, $V$ is an [[Upper Bound]] for $\Lambda$. By [[Zorn's Lemma]], $\Gamma$ has a [[Maximal]] element $\mathcal{C}$. If $G$ is a nonempty, [[Open Set]] set and $G\notin \mathcal{C}$, then $\mathcal{C}\cup\{G\}$ is a larger [[Open Set]] [[Cover]]. Hence, must have a finite [[Subcover]] by maximality of $\mathcal{C}$. Let $\mathcal{W}=\mathcal{C}\cap \mathcal{S}$. $\mathcal{W}$ cannot [[Cover]] $X$, since this would yield a finite [[Subcover]]. Hence there is an $$x\in X-\bigcup\{W\in \mathcal{W}\}\quad(*)$$and $C\in \mathcal{C}$ with $x\in C$. Since $\mathcal{S}$ is a [[Subbasis]], there exist $S_{1},\ldots,S_{n}$ such that $x\in\bigcap_{i=1}^{n}S_{i}\subseteq C$. By $(*)$, none of the [[Set]]s $S_{i}$ can [[Cover]] $C$. Hence, for each $k$, $C\cup \{S_{k}\}$ as a [[Cover]] of $X$ with a finite [[Subcover]]. Let $H_{1}^{k},\ldots,H_{M_{k}}^{k}\in \mathcal{C}$ such that $$X=S_{k}\cup\bigcup H_{j}^{k}$$Then, $$X=\bigcap_{r=1}^{n}\left[S_{r}\cup\bigcup_{k=1}^{n}\bigcup_{j=1}^{m_{k}}H^{k}_{j}\subseteq\right](\bigcup_{i=1}^{r}S_{r})\cup\left[\bigcup\bigcup H_{j}^{k}\right]\subseteq C\cup \bigcup\bigcup H^{k}_{j}$$But, this implies that $C\sup\{H^{k}_{j}\}$ is a finite [[Subcover]] of $\mathcal{C}$.
