---
tag: algebra
mathLink: subgroup lemma
---
>[!prop] Lemma
Let $(G,\cdot)$ be a [[Group]]. Then a [[Subset]] $H$ of $G$ is a [[Subgroup]] of $G$ [[iff]]
>1. $H≠\emptyset$
>2. $a,b\in H\implies a\cdot b^{-1}\in H$

>[!proof]
Suppose $H$ is a [[Subgroup]]. Clearly $H≠\emptyset$. Let $1$ be the [[Identity of a Groupoid]] of $H$. Let $a,b\in H$ be given. Then, $b$ has an [[Inverse of a Groupoid Element]] as $H$ is a [[Group]]. As $\cdot :H\times H \rightarrow H$ is a [[Binary Operation]], $a\cdot b^{-1}\in H$. 
>
Suppose (1) and (2). Let $a\in H$ be given ($H$ is nonempty). Then, $a\cdot a^{-1}=1\in H$, so $H$ has an [[Identity of a Groupoid]]. If $b\in H$, then $1b^{-1}=b^{-1}\in H$. Then, $a,b\in H\implies a(b^{-1})^{-1}=ab\in H$. That $H$ is [[Associativity]] follows from $G$ being a [[Group]]. [[therefore]] $H$ is a [[Subgroup]].

