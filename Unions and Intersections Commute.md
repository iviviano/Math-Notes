---
tag: set theory
mathLink: unions and intersections commute (when one is binary)
---
>[!prop]
Let $\mathcal{A}$ be a collection of [[Set]]s, let $B$ be a set. Then,
$$B\cap\bigcup_{A\in \mathcal{A}}A=\bigcup_{A\in \mathcal{A}}B\cap A$$
and
$$B\cup\bigcap_{A\in \mathcal{A}}A=\bigcap_{A\in \mathcal{A}}B\cup A$$

>[!proof]
Let $x\in B\cap\bigcup A$ be given. Then, pick $A_0\in \mathcal{A}$ such that $x\in A_{0}$. $x\in B$, so $x\in A_{0}\cap B$. As $A_{0}\in A$, 
$$x\in\bigcup_{A\in \mathcal{A}}B\cap A$$
Let $x\in\bigcup B\cap A$. Then, pick $A_{0}\in \mathcal{A}$ such that $x\in A_{0}\cap B$. As $x\in A_{0}$, $x\in \bigcup A$. As $x\in B$ as well,
$$x\in B\cap\bigcup_{A\in \mathcal{A}}A$$
$$\therefore B\cap\bigcup_{A\in \mathcal{A}}A=\bigcup_{A\in \mathcal{A}}B\cap A$$
Let $x\in B\cup\bigcap A$. Suppose $x\in B$. Then,
$$\forall A\in \mathcal{A}:x\in B\cup A$$
Suppose $x\in\bigcap A$. Then,
$$\forall A\in \mathcal{A}:x\in B\cup A$$
so,
$$x\in \bigcap_{A\in \mathcal{A}}B\cup A$$
Let $x\in \bigcap B\cup A$ be given. Then, $\forall A\in \mathcal{A}:x\in B\cup A$. Suppose $x\in B$. Then, $x\in B\cup\bigcap A$. Suppose $x\notin B$. Then, for all $A\in \mathcal{A}:x\in A$. [[therefore]] $x\in\bigcap A$, so $x\in B\cup\bigcap_{A\in \mathcal{A}}A$.
$$\therefore B\cup\bigcap_{A\in \mathcal{A}}A=\bigcap_{A\in \mathcal{A}}B\cup A$$
