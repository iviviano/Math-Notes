From Section 1.1: 7
From Section 1.2: 5, 6

>[!note] 7: Prove the [[Interior, Closure, and Boundary Proposition]] for [[Metric Space]]s
>>[!proof] Proof of 1.
>>Let $A$ be [[Closed Set]]. Let $x\in A$. As $x\in A$ and $A$ is [[Closed Set]], $x$ is in all [[Closed Set]] [[Set]]s containing $A$, so $x\in\bar{A}$. Let $x\in\bar{A}$. Then, $x$ is in all [[Closed Set]] sets containing $A$. As $A$ is a [[Closed Set]] set containing $A$, $x\in A$. [[therefore]] $A=\bar{A}$
>>Let $A=\bar{A}$. $\bar{A}$ is an [[Intersection]] of [[Closed Set]] sets, so it is [[Closed Set]]. [[therefore]] $A$ is [[Closed Set]].
>
>>[!proof] Proof of 2.
>>Let $A$ be [[Open Set]] in $X$. Let $x\in A$. As $x\in A$ and $A$ is [[Open Set]], $X$ is in an [[Open Set]] [[Set]] contained in $A$, so $x\in \text{int } A$. Let $x\in \text{int }A$. Then, $x$ is in an [[Open Set]] set contained in $A$, so $x\in A$. [[therefore]] $A=\text{int }A$.
>>Let $A=\text{int }A$. $\text{int }A$ is a [[Union]] of [[Open Set]] sets. [[therefore]] $A$ is [[Open Set]].
>
>>[!proof] Proof of 3.
>>Let $\mathcal{C}=\{C\supseteq A:C\text{ is closed in }X\}$
>>Apply [[DeMorgan's Laws]]:
>>$$\bar{A}=\bigcap_{C\in \mathcal{C}}C=X-\bigcup_{C\in \mathcal{C}}(X-C)$$
>>As $X-C$ is [[Open Set]], this is the [[Compliment]] of the [[Interior]] of the [[Compliment]] of $A$, since $A\subseteq C$ [[iff]] $X-C\in X-A$. So,
>>$$\bar{A}=X-\bigcup_{C\in \mathcal{C}}(X-C)=X-\text{ int}(X-A)$$
>>
>>Let $\mathcal{O}=\{A\subseteq A:O\text{ is open in }X\}$
>>Apply [[DeMorgan's Laws]]:
>>$$\text{int }A=\bigcup_{O\in \mathcal{O}}O=X-\bigcap_{O\in \mathcal{O}}(X-O)$$
>>As $X-O$ is [[closed Set]], this is the [[Compliment]] of the [[Closure]] of the [[Compliment]] of $A$, since $O\subseteq A$ [[iff]] $X-A\in X-O$. So,
>>$$\text{int }A=X-\bigcap_{O\in \mathcal{O}}(X-O)=X-\text{cl}(X-O)$$
>>
>>Let $x\in \partial A$. Then, $X\in \text{cl }A$ and $x\in \text{cl }(X-A)$.
>>Claim:
>>$$X-\text{cl}(X-A)\supseteq \text{int }A$$ 
>>Let $y\in \text{int }A$ be given. Then, if $U$ is any [[Open Set]] set contained in $A$, $X-U$ is a [[Closed Set]] set containing $X-A$. If $y\in U$, then $y\notin X-U$, so if $y\in \text{int }A$, then $y\notin \text{cl }(X-A)\implies y\in X-\text{cl}(X-A)$.
>>As $x\in \text{cl }(X-A)$, then $x\notin X-\text{cl}(X-A)$. So, $x\notin \text{int }A$. $$\therefore \partial A\subseteq \text{cl }A-\text{int }A$$
>>Claim: 
>>$$X-\text{cl}(X-A)\subseteq \text{int }A$$ 
>>Let $y\in X-\text{cl}(X-A)$. Then, if $C$ is any [[Closed Set]] [[Set]] containing $A$, then $y\notin C$, so $y\in X-C$, which is an [[Open Set]] contained in $A$. [[therefore]] $y\in \text{int }A$
>> 
>>Let $x\in \text{cl }A-\text{int }A$. Then, $x\in \text{cl }A$ and $x\notin \text{int }A$. [[therefore]] $x\notin X-\text{cl }(X-A)$, so $x\in \text{cl}(X-A)$. [[therefore]] $x\in \text{cl }A\cap \text{cl}(X-A)$.
>>$$\therefore \text{cl }A-\text{int }A\subseteq\partial A$$
>>
>
>>[!proof] Proof of 4.
>>Let $x\in \text{cl }[\bigcup A_{k}]$. Then, $x$ is in every [[Closed Set]] set containing $\bigcup A_{k}$. If $C_{k}$ are [[Closed Set]] for each $k$ and $A_{k}\subseteq C_{k}$, then $\bigcup C_{k}$ is [[Closed Set]] and contains $\bigcup A_{k}$, so $x\in\bigcup C_{k}$.
>>[[therefore]] $x\in\bigcup \text{cl }A_{k}$. 
>>Let $x\in \text{cl }A_{k}$ be given. Then, if $C$ is a [[Closed Set]] set containing $\bigcup A_k$, then for each $k$, $A_{k}\subseteq C$. So, $x\in C$
>>[[therefore]] $x\in \text{cl }\bigcup A_k$

>[!note] 5
>(a) Prove that $x\in \text{cl }A$ [[iff]] $x$ is either a [[Limit Point]] of $A$ or an isolate point of $A$.
>>[!proof]
>>Suppose $x\in \text{cl }A$. Then, for all $\epsilon>0$, $B_{d}(x,\epsilon)$ [[Intersects]] $A$ by the [[Open Sets Intersecting the Closure Intersect the Set Theorem]]. Suppose additionally that for all $\epsilon>0$
>>$$B_{d}(x,\epsilon)\cap (A-\{x\})≠\emptyset$$
>>Then, $x$ is a [[Limit Point]] of $A$. Otherwise, pick $\epsilon>0$ such that $B_{d}(x,\epsilon)\cap(A-\{x\})=\emptyset$. As $B_{d}(x,\epsilon)\cap A≠\emptyset$, $x\in A$. but is not a limit point. 
>>[[therefore]] $x$ is a [[Limit Point]] of $A$ or $x$ is an [[Isolated Point]] of $A$.
>>
>>Suppose $x$ is a limit point of $A$. Then, for all $\epsilon>0$, 
>>$$B_{d}(x,\epsilon)\cap (A-\{x\})\ne\emptyset$$
>>Let $U$ be any [[Neighborhood]] of $x$. Then, there exists an $\epsilon>0$ such that $B_{d}(x,\epsilon)\subseteq U$. So any [[Neighborhood]] of $x$ [[Intersects]] $A$ at some point besides $x$. [[therefore]] $x\in U$ by the [[Open Sets Intersecting the Closure Intersect the Set Theorem]].
>>Suppose $x$ is an [[Isolated Point]] of $A$. Then, $x\in A$, so $x\in\bar{A}$.
>
>
>(b) Show that a set having no [[Limit Point]]s is [[Closed Set]]:
>Let $A$ be a set of only [[Isolated Point]]s. Then, for all $x\in \bar{A}$, $x\in A$. So, $\bar{A}\subseteq A$. As $A\subseteq \bar{A}$, $A=\bar{A}$, so $A$ is [[Closed Set]] by the [[Interior, Closure, and Boundary Proposition]].
>(c) $\mathbb{N}$ is an infinite [[Subset]] of $\mathbb{R}$ with no [[Limit Point]]s

>[!note] 6: Prove that [[Subsequences of Convergent Sequences Converge]]
>>[!prop] Lemma
>>If $\{x_{n}\}$ is a [[Sequence]] and $\{x_{n_{k}}\}$ is a [[Subsequence]] of $x_n$, then $$n_{k}≥k$$
>
>>[!proof] Prove Lemma
>Base case: $k=0$
>$n_0≥0$ as $n_{0}\in \mathbb{N}$
>Inductive step: 
>Suppose $n_{k}≥k$ for some $k≥0$. Then, $n_{k+1}≥n_{k}+1≥k+1$
>So, by the [[Principle of Mathematical Induction]], $n_{k}≥k$ for all $k\in \mathbb{N}$.
> 
>>[!proof]
>Let $\epsilon>0$ be given. Pick $N\in \mathbb{N}$ such that if $n≥N$, 
>$$d(x,x_{n})<\epsilon$$
>Then, if $k≥N$, $n_{k}≥k≥N$, 
>$$d(x,x_{n_{k}})<\epsilon$$
>so $x_{n_{k}}\rightarrow x$.
