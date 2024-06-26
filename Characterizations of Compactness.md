---
tag: topology
mathLink: characterizations of compactness theorem
---
>[!thm]
>Let $X$ be a [[Topological Space]] satisfying the [[Hausdorff Axiom]], let $K$ be a [[Subset]] of $X$. Then,
>1. If $K$ is [[Compactness]], then $K$ is [[Closed Set]].
>2. If $K$ is [[Compactness]] and $F\subseteq K$ is [[Closed Set]], $F$ is [[Compactness]].
>3. The [[Continuous]] [[Image]] of a [[Compactness]] [[Set]] is [[Compactness]] ([[Extreme Value Theorem]])
>4. $K$ is [[Compactness]] [[iff]] every collection of [[Closed Set]] [[Subset]]s of $K$ having the [[Finite Intersection Property]] has a nonempty [[Intersection]].

>[!proof]
(1) Let $x\in X-K$. If there is a [[Neighborhood]] $U$ of $x$ contained in $X-K$, then, $X-K$ is [[Open Set]]. For each $z\in K$, let $V_{z},U_{z}$ such that $V_{z}\cap U=\emptyset$ by the [[Hausdorff Axiom]] and $x\in U_{x},z\in V_{z}$. Then, $$\mathcal{V}=\{V_{z}:z\in K\}$$is an [[Open Cover]] of $K$. This has a finite [[Subcover]] $\mathcal{V}'=\{V_{z_{i}}:1≤i≤n\}$. Then take $$U=\bigcap_{i=1}^{n}U_{z_{i}}\ni x$$is a finite [[Intersection]] of [[Open Set]] sets. As $$K\subseteq\bigcup_{i=1}^{n}V_{z_{i}}=X-\bigcap_{i=1}^{n}U_{z_{i}}=X-U$$As $x\in U$ and $U\subseteq X-K$, $K$ is [[Closed Set]]
>
(2) Let $\mathcal{U}$ be a [[Open Cover]] of $F$. As $\mathcal{U}\cup\{X-F\}$ is an [[Open Cover]] of $K$. Pick a finite [[Subcover]]: $\mathcal{U}'\cup\{X-F\}$. So, $\mathcal{U}'$ is a finite [[Subcover]] of $F$.
>
(3) Let $f:X \mapsto Y$ be [[Continuous]], $K$ [[Compactness]]. Let $\mathcal{U}$ be an [[Open Cover]] of $f(K)$. Then, $$\mathcal{W}=\{f^{-1}(U):U\in \mathcal{U}\}$$is an [[Open Cover]] of $K$. Since $K$ is [[Compactness]], there is a finite [[Subcover]] $\mathcal{W}'$ of $K$. Then, $$\mathcal{U'}=\{f(U):U\in \mathcal{W}'\}$$is a finite [[Subcover]] of $f(K)$.
>
(4) Let $\mathcal{F}$ be a [[Collection]] of [[Subset]]s with the [[Finite Intersection Property]]. Suppose that $\bigcap F=\emptyset$. Let $\mathcal{G}=\{X-F:F\in \mathcal{F}\}$. $\mathcal{G}$ is an [[Open Cover]] of $X$, so it is an [[Open Cover]] of $K$: $$\bigcap_{F\in \mathcal{F}}=X-\bigcup_{F\in \mathcal{F}}X-F=X-\bigcup_{U\in \mathcal{G}}U=\emptyset$$By the [[Compactness]]ness of $K$, there are [[Open Set]] sets $G_{1},\ldots,G_{n}\in \mathcal{G}$ such that $$K\subseteq\bigcup_{k=1}^{n}G_{k}=X-\bigcap_{k=1}^{n}X-G_{k}=X-\bigcap_{k=1}^{n}F_{k}\not\supseteq X$$Since $F\subseteq K$ for all $F\in \mathcal{F}$, this contradicts the [[Finite Intersection Property]] of $\mathcal{F}$. So, $K$ is [[Compactness]].
>
Let $\mathcal{U}$ be an [[Open Cover]] of $K$. Let $\mathcal{F}=\{K-U:U\in \mathcal{U}\}$. Since $\mathcal{U}$ [[Cover]]s $K$, $\bigcap_{U\in \mathcal{U}}=\emptyset$, so $\mathcal{F}$ does not have the [[Finite Intersection Property]]. Therefore, there are sets $U_{1},\ldots,U_{n}$ such that $\bigcap_{i=1}^{n}K-U_{i}=\emptyset$. This implies by [[DeMorgan's Laws]], that $\{U_{1},\ldots,U_{n}\}$ is a finite [[Subcover]] of $K$, so $K$ is [[Compactness]].

>[!thm]
Let $(X,d)$ be a [[Metric Space]], let $K$ be a [[Closed Set]] [[Subset]] of $X$. Then the following are equivalent:
>1. $K$ is [[Compactness]].
>2. If $\mathcal{F}$ is a collection of [[Subset]]s of $K$ having the [[Finite Intersection Property]], then $\bigcap_{F\in \mathcal{F}}F\ne \emptyset$
>3. Every [[Sequence]] in $K$ has a [[Converges (Sequence)]]nt [[Subsequence]].
>4. Every infinite [[Subset]] of $K$ has a [[Limit Point]].
>5. $(K,d)$ is a [[Complete]] [[Metric Space]] that is [[Totally Bounded]].
>
Also, $K$ compact [[implies]] $K$ is [[Bounded Metric Space]]

>[!proof]
($1\iff 2$) from above.
>
($3\implies 4$) If $S$ is an infinite [[Subset]] of $K$, then $S$ contains an infinite [[Sequence]] of unique points. This [[Sequence]] has a [[Converges (Sequence)]]nt [[Subsequence]], whose [[Limit of a Sequence]] is a [[Limit Point]] of $S$.
>
($4\implies 3$) Assume that $\{x_{n}\}$ is a [[Sequence]] of distinct points. [[therefore]] $S=\{x_{n}\}$ has a [[Limit Point]] $x$. For each $k$, let $x_{n_{k}}\in S\cap B_{d}\left(x,\frac{1}{k}\right)$. Then, $x_{n_{k}}\rightarrow x$ and is a [[Subsequence]] of $x_{n}$. (Need something to maintain order of sequence terms but this is not hard to add)
>
($1,2\implies 4,3$) Suppose that 4 is false and let $S\subseteq K$ be infinite with no [[Limit Point]]. Then there is an infinite [[Sequence]] $\{x_{n}\}$ with no limit point. So for each $n≥1$, let $F_{n}=\{x_{k}:k≥n\}$. $F_{n}$ contains all its limit points so it it closed. Also, $\bigcap F_{n}=\emptyset$, so $K$ is not [[Compactness]], as $\mathcal{F}=\{F_{n}:n\in \mathbb{N}\}$ has the [[Finite Intersection Property]]. 
>
($3\implies 5$) If $\{x_{n}\}$ is [[Cauchy Sequence]], then it has a [[Converges (Sequence)]] [[Subsequence]]. If a [[Subsequence]] of $x_{n}$ [[Converges (Sequence)]]s, $x_{n}$ converges by [[Subsequence of Cauchy Sequence Converges implies Sequence Converges]]. So, $K$ is [[Complete]].
>
Let $\epsilon>0$ be given. Let $x_{1}\in K$. If $K\subseteq B_{d}(x_{1},\epsilon)$, then done. Let $x_{2}\in K-B_{d}(x_{1},\epsilon)$. If $K\subseteq B_d(x_{1},\epsilon)\cup B_{d}(x_{2},\epsilon)$, then done. Continue... If this never terminates, then $x_{n}$ has no [[Converges (Sequence)]]nt [[Subsequence]], since if $n≠m$, then $d(x_{m},x_{n})≥\epsilon$. Therefore, this must terminate, giving a [[Totally Bounded]] [[Metric Space]]?
>
($5\implies a$) (supposing that $(5\implies3$)
Claim: if $K$ satisfies $3$ and $\mathcal{U}$ is an [[Open Cover]] of $K$, then there exists an $\epsilon>0$ such that for all $x\in K$, there is a $U\in \mathcal{U}$ such that $B_{d}(x, \epsilon)\subseteq U$.
>
For an [[Open Cover]] $\mathcal{U}$ of $K$, let the claim give us $\epsilon$. Let $x_{1},\ldots,x_{n}$ be such that $K\subseteq\bigcup B_{d}(x_{i},\epsilon)$ as $K$ is [[Totally Bounded]]. Let $G_{k}\in \mathcal{U}$ such that $B_{d}(x_{k},\epsilon)\subseteq G_{k}$. Then $G_{1},\ldots, G_{n}$ is a finite [[Subcover]]. [[therefore]] $K$ is [[Compactness]].
