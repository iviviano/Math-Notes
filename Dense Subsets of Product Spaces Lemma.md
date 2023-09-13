---
tag: topology
mathLink: dense subsets of product spaces lemma
---
>[!prop] Lemma
If $X$ is the [[Cartesian Product]] of [[Topological Space]]s $\{X_{i}:i\in I\}$ and $a\in X$, then $$D=\{x\in X:x(i)=a(i)\text{ for all but finitely many } i\}$$ is [[Dense]] in $X$.

>[!proof]
Let $x\in X$ be given. Let $G$ be an [[Neighborhood]] of $x$. Then, there are [[Open Set]] [[Set]]s $G_{i_1},\ldots,G_{i_n}$ such that $x\in\bigcap_{k=1}^{n}\pi^{-1}(G_{i_{k}})\subseteq G$. Let $y\in X$ with $y(i)=a(i)$ for $i\notin\{i_1,\ldots,i_n\}$ and $y(i)\in G_{i_k}$ otherwise. Then, $y\in D$ and $y\in G$, so $D$ is [[Dense]] in $X$. 
