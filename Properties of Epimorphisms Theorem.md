---
tag: algebra
mathLink: properties of epimorphisms theorem
---
>[!thm]
>Let $\theta$ be an [[Epimorphism]] from the [[Groupoid]] $G$ to $H$. Then
>1. If $G$ has an [[Identity of a Groupoid]] $1$, then the [[Identity of a Groupoid]] of $H$ is $1\theta$. If $f$ is an [[Inverse of a Groupoid Element]] of $g$ in $G$, then $f \theta$ is an [[Inverse of a Groupoid Element]] of $g \theta$ in $H$.
>2. If $G$ is [[Commutative]], then so is $H$
>3. If $G$ is a [[Semigroup]], then so is $H$.

>[!proof]
(1) Let $h\in H$. As $\theta$ is [[Surjective]], there is a $g\in G:g \theta= h$. Then, $$g \theta=(g1)\theta=g \theta 1\theta=h1\theta=h$$and $$g \theta=(1g)\theta=1\theta g \theta=1\theta h=h$$so $1\theta$ is an [[Identity of a Groupoid]] of $H$. Suppose $f$ is an [[Inverse of a Groupoid Element]] of $g$. Then $$1\theta=(gf)\theta=g \theta f \theta=hf \theta$$and $$1\theta=(fg)\theta=f \theta g \theta=f \theta h$$so $f \theta$ is an [[Inverse of a Groupoid Element]] of $h$.
>
(2) Assume $G$ is [[Commutative]]. Let $h_{1},h_{2}\in H$ be given. Pick $g_{1},g_{2}\in G$ such that $g_{1}\theta=h_{1}$ and $g_{2}\theta=h_{2}$. Then, $$h_{1}h_{2}=g_{1}\theta g_{2}\theta=(g_{1}g_{2})\theta$$As $G$ is [[Commutative]], $g_{1}g_{2}=g_{2}g_{1}$, so$$h_{1}h_{2}=(g_{2}g_{1})\theta=g_{2}\theta g_{1}\theta=h_{2}h_{1}$$so $H$ is [[Commutative]].

(3) Assume $G$ is a [[Semigroup]]. Let $h_{1},h_{2},h_{3}\in H$ be given. Pick $g_{1},g_{2},g_{3}\in G$ such that $g_{1}\theta=h_{1},g_{2}\theta=h_{2},$ and $g_{3}\theta=h_{3}$. Then, $$h_{1}(h_{2}h_{3})=g_{1}\theta((g_{2}g_{3})\theta)=g_{1}\theta(g_{2}\theta g_{3}\theta)$$
