---
tag: topology
mathLink: metric, compact, and closed sub- spaces are normal
---
>[!prop]
>1. Every [[Metric Space]] is [[Normal Topological Space]].
>2. Every [[Compactness]] [[Topological Space]] is [[Normal Topological Space]].
>3. If $X$ is a [[Normal Topological Space]] [[Topological Space]] and $F\subseteq X$ is [[Closed Set]], then $F$ is [[Normal Topological Space]] when given the [[Subspace Topology]].

>[!proof]
(1) Let $(X,d)$ be a [[Metric Space]]. Let $A,B$ be [[Disjoint]] [[Closed Set]] [[Subset]]s of $X$. Pick $f:X \rightarrow \mathbb{R}$ [[Continuous]] such that $f(a)=0,f(b)=1$ for all $a\in A,b\in B$ by [[Urysohn's Lemma]]. Then, let $\epsilon<\frac{1}{2}$. As $f$ is [[Continuous]], the [[Ep-de Formulation of Continuity]] [[implies]] for each $a\in A$, there is a $\delta_{a}>0$ such that for all $x\in X$, $$d(x,a)<\delta_{a}\implies|f(a)-f(x)|<\epsilon$$Taking the [[Union]] over these $\delta_{a}$ balls gives us an [[Open Set]] [[Set]] containing $A$. We can find a similar open set containing $B$ such that these two open sets are [[Disjoint]] as $\epsilon<\frac{1}{2}$.
>
(2) Let $(X)$ be a [[Compactness]] [[Topological Space]]. Let $A,B\subseteq X$. 
>
(3) Let $A,B\subseteq F$ be [[Closed Set]]. Then, pick $A',B'\in X$ such that $A',B'$ are [[Closed Set]] and $A'\cap F=A,B'\cap F=B$. Then, pick $U,V\subseteq X$ [[Open Set]] and [[Disjoint]] with $A'\subseteq U$ and $B'\subseteq V$. Then, $$A=A'\cap F\subseteq U\cap F=U'$$
which is [[Open Set]] in $F$. And, $$B=B'\cap F\subseteq V\cap F=V'$$which is [[Open Set]] in $F$. Additionally, $U',V'$ are [[Disjoint]] as $U,V$ are [[Disjoint]]. So, $F$ is [[Regular]].
