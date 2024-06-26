---
tag: topology
mathLink: finer metrics lemma
---
> [!prop]
> Let $d$ and $d'$ be two [[Metric]]s on the [[Set]] $X$; let $T$ and $T'$ be the [[Topology]]s they induce. Then, $T'$ is [[Finer]] than $T$ [[iff]] for each $x\in X$ and each $\epsilon > 0$, there exists a $\delta >0$ such that
> $B_{d'}(x, \delta)\subseteq B_d(x, \epsilon)$

> [!proof]
> Suppose $T'$ is [[Finer]] than $T$. Let $\epsilon, x\in$ [[ball]] be given. By the [[Finer Bases Lemma]], there exists a basis element $B$ of any [[Basis of a Topology]] for $T'$ such that $x\in B$ and $B\subseteq B_d(x, \epsilon)$. As $B$ is [[Open Set]] in $T'$, and $x\in B$, there exists a [[Ball]] of radius $\delta$ under the [[Metric]] $d'$ such that $B_{d'}(x, \delta)\subseteq B\subseteq B_d(x, \epsilon)$.
> 
> Suppose the implication above. Let $x\in X$. Let $B$ be [[Open Set]] in $T$ with $x\in B$. Pick $\epsilon>0$ such that [[ball]] [[subset]] $B$. Then, pick $\delta>0$ such that $B_{d'}(x, \delta)\subseteq B_d(x,\epsilon)$. As $x\in B_{d'}(x,\delta)\subseteq B$, there is a [[Basis of a Topology]] element of $T'$ in every [[Open Set]] of $T$, so $T'$ is [[Finer]] than $T$ by the [[Finer Bases Lemma]]. 
