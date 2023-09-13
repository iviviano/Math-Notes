---
tag: topology
mathLink: pasting lemma
---
> [!thm]
> Let $X = A\cup B$, where $A$ and $B$ are [[Closed Set]] in $X$. Let $f:A\rightarrow Y$ and $g:B\rightarrow Y$ be [[Continuous]]. If $f(x) = g(x)$ for every $x\in A\cup B$, then, $f$ and $g$ combine to give a [[Continuous]] [[Function]] $h:X \rightarrow Y$, defined by setting $h(x) = f(x)$ if $x\in A$, and $h(x) = g(x)$ if $x\in B$.

> [!proof]
> Let $D$ be [[Closed Set]] in $Y$. Then, pick $C_a$ [[notation for subset]] $A$ with $C_a = f$[[notation for inverse]]$(D)$ with $C_a$ [[Closed Set]], and $C_a$ [[notation for subset]] $A$ with $C_b = f$[[notation for inverse]]$(D)$ with $C_b$ [[Closed Set]]. Let $x\in h$[[notation for inverse]]$(D)$. Then, if $x$ is in $A$, then, $h(x)= f(x)$, so $x\in C_a$. Otherwise, $x\in B$, so $g(x) = h(x)$, and $x\in C_b$. 
> [[therefore]] $h$[[notation for inverse]]$(D)\subseteq C_a\cup C_b$. 
> As $f^{-1}(D)\subseteq h^{-1}(D)$ and $g^{-1}(D)\subseteq h^{-1}(D)$ (trivially?), the [[Closed Set]] set $C_a\cup C_b = g^{-1}(D)$
