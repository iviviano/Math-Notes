---
tag: topology
mathLink: pasting lemma
---
> [!thm]
> Let $X = A\cup B$, where $A$ and $B$ are both [[Closed Set]] or both open in $X$. Let $f:A\rightarrow Y$ and $g:B\rightarrow Y$ be [[Continuous]]. If $f(x) = g(x)$ for every $x\in A\cup B$, then, $f$ and $g$ combine to give a [[Continuous]] [[Function]] $h:X \rightarrow Y$, defined by setting $h(x) = f(x)$ if $x\in A$, and $h(x) = g(x)$ if $x\in B$.

>[!proof]
Suppose $A,B$ are both [[Closed Set]]. Let $V\subseteq Y$ be [[Closed Set]]. $$h^{-1}(V)=h^{-1}(V)\cap X=h^{-1}(V)\cap(A\cup B)=(h^{-1}(V)\cap A)\cup (h^{-1}(V\cap B))$$Now, $h^{-1}(V)\cap A=f^{-1}(V)$ and $h^{-1}(V)\cap B=g^{-1}(V)$. As these are each [[Closed Set]] by the [[Characterizations of Continuity Theorem]], $f^{-1}(V)$ is [[Closed Set]]. [[therefore]] $f$ is [[Continuous]] by the [[Characterizations of Continuity Theorem]].

Let $A_\alpha$ be a [[Collection]] of [[Closed Set]] [[Subset]]s of a [[Topological Space]] $X$. 