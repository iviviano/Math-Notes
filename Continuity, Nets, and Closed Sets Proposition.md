---
tag: topology
mathLink: continuity, nets, closed sets proposition
---
>[!prop]
>Let $X$, $Y$ be [[Topological Space]]s. 
>1. If $f:X \rightarrow Y$ and $x\in X$, then $f$ is [[Continuity at a Point]] $x$ [[iff]] whenever $\{x_{i}\}$ is a [[Net]] in $X$ and $x_{i}\rightarrow x$, $f(x_{i})\rightarrow f(x)$. ([[Net-Sequential Formulation of Continuity]])
>2.  If $f:X \rightarrow Y$ and $x\in X$, if $f$ is [[Continuity at a Point]] $x$, then whenever  $\{x_{i}\}$ is a [[Net]] in $X$ and $x_{i}$ [[notation for clusters]] $x$, $f(x_{i})$ [[notation for clusters]] $f(x)$.
>3. A [[Subset]] $F$ of $X$ is [[Closed Set]] [[iff]] whenever a [[Net]] in $F$ [[Converges (net)]]s to a point $x$, then $x\in F$.

>[!proof]
(a) Suppose $f$ is [[Continuity at a Point]] $x$ and that $x_{i}\rightarrow x$. If $V$ is a [[Neighborhood]] of $f(x)$ in $Y$, then there exists a [[Neighborhood]] $U$ of $x$ with $U\subseteq f^{-1}(V)$. Pick $i_{0}$ such that for all $i≥i_0$, $x_{i}\in U$. Then, $f(x_{i})\in V$ for all $i≥i_{0}$. Therefore, $f(x_{i})\rightarrow f(x)$.
>
Suppose that $x_{i}\rightarrow x$ [[implies]] $f(x_{i})\rightarrow f(x)$. Suppose $f$ is not [[Continuity at a Point]] $x$. Then pick a [[Neighborhood]] $V$ of $f(x)$ such that $U-f^{-1}(V)≠\emptyset$ for all [[Neighborhood]]s $U$ of $x$. Let $\mathcal{T_x}$ be the [[Collection]] of [[Neighborhood]]s of $x$ [[Directed Set]] with respect to inclusion. For $U\in \mathcal{T_x}$, let $x_{U}\in U-f^{-1}(U)$. This is a [[Net]] in $X$ with $x_{U}\rightarrow x$. However, $f(x_{U})\not \rightarrow f(x)$ since $x_{U}\notin f^{-1}(U)$ for all [[Neighborhood]]s $U$ of $x$. By contradiction, $f$ is [[Continuity at a Point]] $x$.
>
(b) Let $f:X \rightarrow Y$ be [[Continuity at a Point]] $x\in X$ and let $(x,I)$ be a [[Net]] in $X$ with $x_{i}$ [[notation for clusters]] $x$. Let $V$ be a [[Neighborhood]] of $f(x)$ and let $j\in I$. Then, $f^{-1}(V)$ is [[Open Set]] in $X$, since $f$ is [[Continuous]] at $x$. Pick $i≥j$ such that $x_{i}\in f^{-1}(V)$. Then, $f(x_{i})\in V$, so $f(x_{i})\rightarrow _\text{cl}x$.
>
(c) Suppose $F$ is [[Closed Set]]. Let $x_{i}$ be a [[Net]] in $F$ [[Converges (net)]]ing to $x$. If $U$ is a [[Neighborhood]] of $x$, then there exists $i_{U}$ such that $x_{i}\in U$ for all $i≥i_{U}$. So, $U\cap F≠\emptyset$. Therefore, $x\in F$ since [[Open Sets Intersecting the Closure Intersect the Set Theorem]].
>
Suppose that $x_{i}\rightarrow x\implies x\in F$. Let $x\in \text{cl }F$. Let $\mathcal{T_x}$ be the [[Set]] of all [[Neighborhood]]s of $x$ [[Directed Set]] by inclusion. Since $x\in \text{cl }F$, for all $U\in \mathcal{T_x}$, there exists $x_{U}\in U\cap F$, since [[Open Sets Intersecting the Closure Intersect the Set Theorem]]. Then, $x_U$ is a [[Net]] in $X$ with $x_{U}\rightarrow x$. So, $x\in F$.
