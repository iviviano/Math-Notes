---
tag: topology
mathLink: characterizations of normal spaces theorem
---
>[!prop]
If $X$ is a [[Topological Space]], then the following statements are equivalent.
>1. $X$ is [[Normal Topological Space]].
>2. If $A$ is a [[Closed Set]] and $G$ is an [[Open Set]] [[Set]] with $A\subseteq G$, then there is an [[Open Set]] [[Set]] $U$ such that $A\subseteq U\subseteq \text{cl }U\subseteq G$.
>3. If $A,B$ are [[Disjoint]] [[Closed Set]] sets, then there is an [[Open Set]] [[Set]] $V$ such that $B\subseteq V$ and $A\cap \text{cl }V=\emptyset$.

>[!proof]
Assume (1). Then let $A$ be [[Closed Set]] and let $G$ be [[Open Set]] with $A\subseteq G$. $X-G$ is [[Closed Set]] and [[Disjoint]] from $A$, so there is an [[Open Set]] set $U$ such that $U\cap G=\emptyset$ and $X-G\subseteq U$. Then, $X-U\subseteq G$ is a [[Closed Set]] [[Set]]. As $U\cap G=\emptyset$ and $A\subseteq G$, $A\subseteq X-U$. As $A$ is an [[Open Set]] [[Set]] contained in $X-U$, $A\subseteq \text{int }(X_U)$. So, (2) by the [[Interior, Closure, and Boundary Proposition]].
>
Assume (2). Let $A, B$ be [[Disjoint]] [[Closed Set]] sets. Then the [[Open Set]] set $X-B$ contains $A$. Pick $U$ [[Open Set]] such that $A\subseteq U\subseteq \text{cl }U\subseteq X-B$. Then, $B\cap \text{cl }U=\emptyset$, so (3).
>
Assume (1). Let $A, B$ be [[Disjoint]] [[Closed Set]] sets. Pick an [[Open Set]] set $V$ such that $B\subseteq V$ and $A\cap \text{cl }V=\emptyset$. Then, the [[Open Set]] [[Set]] $X-\text{cl }V$ contains $A$ and is [[Disjoint]] from $V$ so. (1).
