---
tag: topology
mathLink: characterizations of regular spaces proposition
---
>[!prop]
Let $X$ be a [[Topological Space]]. Then the following are equivalent:
>1. $X$ is [[Regular]]
>2. If $G$ is an [[Open Set]] [[Set]] and $x\in G$, then there is an [[Open Set]] [[Set]] $U$ such that $x\in U\subseteq \text{cl }U\subseteq G$
>3. If $F$ is a [[Closed Set]] [[Set]] and $x\notin F$, then there is an [[Open Set]] set $V$ such that $F\subseteq V$ and $x\notin \text{cl }V$

>[!proof] Proof.
Suppose (1). Then let $G$ be [[Open Set]] and $x\in G$. Then, there are [[Disjoint]] [[Open Set]] sets $U,V$ such that $x\in U$ and $X-G\subseteq V$. As $U\cap V=\emptyset$, $V\cap\bar{U}=\emptyset$, since [[Open Sets Intersecting the Closure Intersect the Set Theorem]]. As $X-G\subseteq V,\text{cl }U\subseteq V$.
>
Suppose (2). Then let $F$ be [[Closed Set]] and $x\notin F$. 
>
Suppose (3). Then let $F$ be [[Closed Set]] and $x\notin F$. Then, pick an [[Open Set]] set $V$ such that $F\subseteq V$ and $x\notin \text{cl }V$. Let $U=X-\text{cl }V$. $U$ is [[Open Set]] as [[Closure]]s are closed. $U\cap V=\emptyset$ as $U=X-\text{cl V}\subseteq X-V$. $x\in U$ as $x\notin \text{cl }V$. [[therefore]] $X$ is [[Regular]].
