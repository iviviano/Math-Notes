From 2.6: 5

>[!note] 5
I believe that assumption that $I$ is countable is not needed to show that $X_{i}$ are each countable.
>
Suppose $X$ is [[Separable]]. Let $E$ be a countable [[Dense]] [[Subset]] of $X$. Then, $\pi_{i}(E)$ is countable. Let $U$ be [[Open Set]] in $X_i$. Then, $\pi_{i}^{-1}(U)$ is [[Open Set]] in $X$. So, $\pi^{-1}(U)$ [[Intersects]] $E$, since $E$ is [[Dense]]. Therefore, $$\pi_{i}(E\cap \pi^{-1}_{i}(U))≠\emptyset $$Additionally, since the [[Intersection Under Image]], $$\pi_{i}(E\cap \pi^{-1}_{i}(U))\subseteq \pi_{i}(E)\cap \pi_{i}(\pi_{i}^{-1}(U))=\pi_{i}(E)\cap U$$So every [[Open Set]] [[Subset]] of $X_{i}$ [[Intersects]] $\pi_{i}(E)$. Therefore, $\pi_{i}(E)$ is a [[Dense]] [[Subset]] of $X_{i}$, so $X_{i}$ is [[Separable]].
>
Suppose each $X_{i}$ is [[Separable]] and let $I=\mathbb{N}$. Let $E_{i}$ be a countable [[Dense]] [[Subset]] of $X_{i}$ for each $i\in \mathbb{N}$. 
>
For each $i\in \mathbb{N}$, pick $x_{i}\in E_{i}$. Let $$E=\bigcup_{i=1}^{\infty}\left(\prod_{j=1}^{i-1}\{x_{j}\}\times E_{i}\times\prod_{j=i+1}^{\infty}\{x_{j}\}\right)$$
>
Claim: $E$ is a countable [[Dense]] [[Subset]] of $X$. Clearly, $E$ is countable, since countable [[Union]]s of countable [[Set]]s are countable. Let $U$ be [[Open Set]] in $X$, and suppose there is an $i$ such that $\pi_{i}(U)≠X_{i}$. Then, $\pi_{i}(U)$ is [[Open Set]] in $X_{i}$, since [[Projection]] maps are [[Open Map]]. As $\pi_{i}(U)$ is [[Open Set]] and $E_{i}$ is [[Dense]], $\pi_{i}(U)\cap E_{i}≠\emptyset$. Let $y_{i}\in \pi_{i}(U)\cap E_{i}$. Then, $$(x_{1},x_{2},\ldots,x_{i-1},y_{i},x_{i+1},\ldots)\in E$$so, $U$ [[Intersects]] $E$. 
>
Therefore, $E$ is [[Dense]] in $X$. So, $X$ is [[Separable]].

Consider $I$ finite as well