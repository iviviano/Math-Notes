---
tag: topology
mathLink: one-point-compactification conditions
---
>[!prop]
If $X$ is a [[Local Compactness]] [[Topological Space]], then there is a [[Compactness]] space $X_{\infty}$ with:
>1. $X\subseteq X_\infty$ and $X_\infty-X$ is a single point denoted $\infty$
>2. A [[Subset]] $U$ of $X_{\infty}$ is [[Open Set]] [[iff]] both $U\cap X$ is [[Open Set]] in $X$ and if $\infty \in U$, then $X_{\infty}-U$ is a [[Compactness]] [[Subset]] of $X$.
>3. If $f\in$ [[Set of Continuous Functions that Vanish at Infinity]]$(X)$ and we define $f':X \mapsto \mathbb{R}$ with $f'(x)=f(x)$ when $x\in X$ and $f'(\infty)=0$, then $f'\in C(X_{\infty})$. 
>4. If $f\in$ [[Vector Space of Continuous Functions]]$(X)$ with $f(\infty)=0$, then the [[Restriction]]: $f|X\in C_{0}(X)$

>[!proof] Proof that $X_{\infty}$ is a [[Compactification]] of $X$
Let $\mathcal{U}$ be an [[Open Cover]] of $X_{\infty}$. Then, there exists an [[Open Set]] [[Set]] $U\in \mathcal{U}$ with $\infty \in U$. By definition, $$X_{\infty}-U\subseteq X$$ and is [[Compactness]] and [[Cover]]ed by $\mathcal{U}-\{U\}$. Let $\mathcal{U}'$ be a finite [[Subcover]]. Then, $\mathcal{U}'\cup V$ is a finite [[Subcover]] of $X_{\infty}$. So, $X_{\infty}$ is [[Compactness]].
>
Let $U$ be an [[Open Set]] [[Subset]] of $X_{\infty}$. If $U\cap X=\emptyset$, then $U=\{\infty\}$. Since $U$ is [[Open Set]], $$X_{\infty}-U=X_{\infty}-\{\infty\}=X$$But, $X_{\infty}-U$ is [[Compactness]]. This contradicts the assumption that $X$ is not compact. Therefore, $U\cap X≠\emptyset$. So, $X$ is [[Dense]] in $X_\infty$. 

