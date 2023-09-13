---
tag: topology
mathLink: Hausdorff spaces are nice
---
> [!thm]
> Every [[Simply Ordered Set]] [[Set]] is a [[Hausdorff Space]] in the [[Order Topology]]. The [[Cartesian Product]] of two [[Hausdorff Space]]s is a [[Hausdorff Space]]. A [[Subspace]] of a [[Hausdorff Space]] is a [[Hausdorff Space]].

> [!proof]
> Let $X$ be a [[Simply Ordered Set]] [[Set]] under the [[Order Topology]]. Let $x_0 < x_1\in X$. Let $c\in X$ with $x_0 < c < x_1$ (why is a simply ordered set infinite and dense?). Then, the [[Open Set]] [[Rays]] $U_0 = (-\infty, c)$ and $U_1 = (c, \infty)$ are [[Neighborhood]]s of $x_0$ and $x_1$, respectively. Additionally, $U_0$ and $U_1$ are [[Disjoint]]. [[therefore]] $X$ satisfies the [[Hausdorff Axiom]].
> 
> Let $X$, $Y$ be [[Hausdorff Space]]s. Let $(x_0, y_0), (x_1, y_1)\in X$ [[cartesian product]] $Y$ be given. Pick [[Disjoint]] [[Neighborhood]]s $U_0, U_1$ of $x_0, x_1$ in $X$ and $V_0, V_1$ of $y_0, y_1$ in $Y$. Then, $U_0\times V_0$ and $U_1\times V_1$ are [[Disjoint]] [[Neighborhood]]s of $(x_0, y_0)$ and $(x_1, y_1)$. [[therefore]] the [[Product Topology]] on $X\times Y$ is a [[Hausdorff Space]].
> 
> Let $X$ be a [[Hausdorff Space]]. Let $Y$ be a [[Subspace]] of $X$. Let $y_0, y_1\in Y$ be given. Then, pick [[Neighborhood]]s $U_0, U_1$ of $y_0, y_1$ in $X$ with $U_0$ and $U_1$ [[Disjoint]]. Then, $U_0\cap Y$ is a [[Neighborhood]] of $y_0$ in $Y$, and $U_1\cap Y$ is a [[Neighborhood]] of $y_1$ in $Y$. Additionally, these two neighborhoods must be [[Disjoint]]. [[therefore]] $Y$ is a [[Hausdorff Space]].

