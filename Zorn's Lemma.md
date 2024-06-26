---
tag: set theory
mathLink: Zorn's lemma
---
>[!thm]
If $(S,≤)$ is a [[Partially Ordered Set]] [[Set]] such that every [[Chain]] in $S$ has an [[Upper Bound]], then $S$ has a [[Maximal]] element.

>[!prop] Corollary
Every [[Vector Space]] over $\mathbb{R}$ has a [[Basis of a Vector Space]]

>[!proof]
$\{v_{1},v_{2},\ldots,\}\subseteq V$ is [[Linearly Independent]] if for any finite subset $\{v_{i_{1}},\ldots,v_{i_{n}}\}$, the only scalars for which $$a_{1}v_{i_{1}}+\cdots+a_{n}v_{i_{n}}=0\iff \forall i:a_{i}=0$$A [[Basis of a Vector Space]] for $V$ is a [[Maximal]] [[Linearly Independent]] [[Set]] of [[Vector]]s. 
>
Let $M$ be the [[Collection]] of all [[Linearly Independent]] [[Subset]]s of $V$. So, $(M,\le)$ is a [[Partially Ordered Set]] set with respect to inclusion. Let $e$ be a [[Chain]] in $M$. Let $$B=\bigcup\{l\in e\}$$Let $v_{1},\ldots, v_{n}\in B$. Then, pick $A_{1},\ldots, A_{n}\in e$ such that $v_{i}\in A_{i}$ for all $i$. Since $e$ is a [[Chain]], $A_{k}$ contains all $A_{i}$. So, $v_{1},\ldots, v_{n}\in A_{k}$. But, $A_{k}\in e\subseteq M$, so $v_{1}\ldots,v_{n}$ are [[Linearly Independent]]. Therefore, $B$ is linearly independent. So, $B$ is an [[Upper Bound]] for the chain $e$ and $B\in M$. By Zorn's lemma, $M$ has a [[Maximal]] element. [[therefore]] there is a [[Basis of a Vector Space]] of $V$.
