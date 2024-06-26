---
tags:
  - topology
mathLink: pathwise connectedness in $\mathbb{R}^n$ theorem
---

>[!thm]
>If $X$ is an [[Open Set]] [[Subset]] of $\mathbb{R}^{n}$, then $X$ is [[Connected]] [[iff]] $X$ is [[Pathwise Connectedness]].

>[!proof]
Suppose that $X$ is [[Connected]]. Let $p\in X$. Let $U=\{x\in X:\text{there is a path from }x \text{ to p}\}$. Let $V=X-U$. $U$ is nonempty, since the constant [[Path]] from $p$ to $p$ is [[Continuous]] by the [[Constructing Continuous Functions Theorem]], so $p\in U$. 
>
($U$ is [[Open Set]]):
Let $q\in U$ so that there is a [[Path]] $f$ from $p$ to $q$. Since $X$ is [[Open Set]], there is a [[Neighborhood]] $B(q,\epsilon)\subseteq X$. For each $y\in B(q,\epsilon)$, there is a [[Path]] from $y$ to $q$ and a [[Path]] from $q$ to $p$, so there is a [[Path]] from $y$ to $p$ by the [[Product of Paths Proposition]]. So, $y\in U$ by definition. Since $y$ was an arbitrary element of $B(q,\epsilon)$, $B(q,\epsilon)\subseteq U$. So, $U$ is [[Open Set]]. 
>
($V$ is [[Open Set]]):
Let $q\in V$. Since $X$ is [[Open Set]], pick $\epsilon>0$, such that $B(q,\epsilon)\subseteq X$. If $y\in B(q,\epsilon)$ and $y\in U$, then there are [[Path]]s from $q$ to $y$ and from $y$ to $p$. So, there is a [[Path]] from $q$ to $p$. This contradicts that $q\notin U$, so $B(q,\epsilon)\subseteq V$. Therefore, $V$ is [[Open Set]].
>
$X=U\cup V$ and $U$ and $V$ are [[Disjoint]]. So, $X$ [[Connected]] implies $U$ is empty or $V$ is empty. Therefore, $V$ is empty and $U=X$. Then every point in $X$ can be connected by a [[Path]] to $p$. So, $X$ is [[Pathwise Connectedness]]. 
>
The reverse follows from [[Pathwise Connected Implies Connected]].
