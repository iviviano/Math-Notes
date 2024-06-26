From 1.4: 1, 2, and 8

>[!note] 1
Let $\{K_{n}\}$ be a finite collection of [[Compactness]] [[Set]]s, let $K=\bigcup K_{n}$, let $\mathcal{U}$ be an [[Open Cover]] of $K$. For each $n$, pick a finite [[Subcover]] $\mathcal{U}_{n}$ of $\mathcal{U}$ such that $\mathcal{U_{n}}$ [[Cover]]s $K_{n}$. Then, $$\mathcal{U}'=\bigcup \mathcal{U}_{n}$$is an [[Open Cover]] of $K$. It is finite as it is a finite [[Union]] of finite [[Set]]s, and it is a [[Subcover]] of $\mathcal{U}$ as each $\mathcal{U}_{n}$ is. [[therefore]] $K$ is [[Compactness]].

>[!note] 2
Suppose $K$ is [[Compactness]] and let $\mathcal{U}$ be a relatively [[Open Cover]] of $K$. Then, for each $U\in \mathcal{U}$, there is a $U'\subseteq X$ that is [[Open Set]] in $X$ and $U=K\cap U'$. Let $\mathcal{U}'$ be the [[Collection]] of these $U'$ for each $U\in \mathcal{U}$. Pick a finite [[Subcover]] $\mathcal{U}^{*}$ of $\mathcal{U}$ that [[Cover]]s $K$. For each $U\in \mathcal{U}^{*}$, $U\cap K\in \mathcal{U}$. So, $\{U\cap K:U\in \mathcal{U}^*\}\subseteq \mathcal{U}$. Additionally, $$\bigcup_{U\in \mathcal{U}^{*}}U\cap K=K\cap \bigcup\{U:U\in \mathcal{U}^*\}$$as [[Unions and Intersections Commute]]. As $K$ is [[Cover]]ed by $\bigcup \{U\in \mathcal{U}^{*}\}$, $\{U\cap K:U\in \mathcal{U}^{*}\}$ is an finite [[Subcover]] of $\mathcal{U}$.
>
Suppose that every relatively [[Open Cover]] of $K$ omits a finite [[Subcover]]. Let $\mathcal{U}$ be an [[Open Cover]] of $K$. Let $$\mathcal{U}^{'}=\{U\cap K:U\in \mathcal{U} \}$$As each element of $\mathcal{U}'$ is [[Open Set]] in $K$ and $$\bigcup_{U'\in \mathcal{U}'}U'=\bigcup_{U\in \mathcal{U}}U\cap K=K\cap \bigcup \{U\in \mathcal{U}\}\supseteq K$$[[therefore]] $\mathcal{U}^{'}$ is a relatively [[Open Cover]] of $K$. So, $\mathcal{U}'$ omits a finite [[Subcover]]: $\{U_{n}\cap K: U\in \mathcal{U},1≤n≤k\}$ for some $k$ of $K$. Note that this implies $\{U_{n}:U\in \mathcal{U}\}$ is also a finite [[Subcover]] of $K$, so $K$ is [[Compactness]].

>[!note] 8
Suppose that $X_{1}\times X_{2}$ is [[Compactness]]. Let $\pi_{1}:X_{1}\times X_{2}\mapsto X_{1}$ be the [[Projection]] map. Clearly, $\pi_{1}(X_{1}\times X_{2})=X_{1}$. By [[9-14 Problems]], $\pi_{1}$ is [[Continuous]]. By the [[Characterizations of Compactness]], $X_{1}$ is [[Compactness]]. Similarly, $X_{2}$ is [[Compactness]].
>
Suppose that $X_{1}$ and $X_{2}$ are [[Compactness]]. Let $\mathcal{U}$ be an [[Open Cover]] of $X_{1}\times X_{2}$. Then, $$\mathcal{U_{1}}=\{\pi_{1}(U):U\in \mathcal{U}\},\mathcal{U_2}=\{\pi_{2}(U):U\in \mathcal{U}\}$$are [[Open Cover]]s of $X_{1}$ and $X_{2}$, respectively. Let $x_{1}\in X_{1}$ be given. Then, there exists an $x_{2}\in X_{2}$ such that there is a [[Neighborhood]] $U\in \mathcal{U}$ of $(x_{1},x_{2})$. As $\pi_{1}(x_{1},x_{2})=x_{1}$,$x_{1}\in \pi(U)\in \mathcal{U}_{1}$, so $\mathcal{U_{1}}$ is an [[Open Cover]] of $X_{1}$. Similarly, $\mathcal{U}_{2}$ is an [[Open Cover]] of $X_{2}$. 
>
Let $\mathcal{U}_1',\mathcal{U}_2'$ be finite [[Subcover]]s of $X_{1}$, $X_{2}$. Construct a [[Subcover]] $\mathcal{U}'$ of $X$ as follows:
>1. For each $U'\in \mathcal{U}_{1}'$, Pick $U\in \mathcal{U}$ such that $U'\subseteq \pi_{1}(U)$. Add $U$ to $\mathcal{U}'$
>2. For each $U'\in \mathcal{U}_{2}'$, Pick $U\in \mathcal{U}$ such that $U'\subseteq \pi_{2}(U)$. Add $U$ to $\mathcal{U}'$
>
Note: $\mathcal{U}$ has finitely many elements as both $\mathcal{U}_1'$ and $\mathcal{U}_{2}'$ do. Clearly it is a [[Subcover]] of $\mathcal{U}$, as each element came from $\mathcal{U}$. Now we must show that $\mathcal{U}$ is actually a [[Cover]] of $X_{1}\times X_{2}$. Let $(x_{1},x_{2})\in X_{1}\times X_{2}$ be given. As $\mathcal{U}_1'$ is a [[Cover]] of $X_{1}$, there is a [[Neighborhood]] $U_1$ of $\mathcal{U}$ such that some [[Subset]] of $\pi(U_{1})$ containing $x$ and contained in $\mathcal{U}'_1$. There is a similar [[Neighborhood]] $U_{2}$ for $x_{2}$. [[therefore]] $(x_{1},x_{2})\in U_{1}\cup U_{2}$. So, $\mathcal{U}'$ [[Cover]]s $X_{1}\times X_{2}$. [[therefore]] $X_{1}\times X_{2}$ is [[Compactness]].


>[!note] 8
Suppose that $X_{1},X_{2}$ are [[Totally Bounded]]. Let $\epsilon>0$ be given. Then, pick $x^{1}_{1},\ldots,x^{1}_{n}$ such that $$X_{1}\subseteq\bigcup_{i=1}^{n}B_{d_{1}}\left(x^{1}_{i},\frac{\epsilon}{2}\right)$$and similarly pick $x_{1}^{2},\ldots,x_{k}^{2}$ such that $$X_{2}\subseteq\bigcup_{j=1}^{k}B_{d_{1}}\left(x_{j}^{2},\frac{\epsilon}{2}\right)$$
>
Then, let $x_{1},\ldots,x_{nk}$ such that $$x_{1}=(x_{1}^{1},x_{1}^{2}),...,x_{k}=(x_{1}^{1},x_{k}^{2}),x_{nk}=(x_{n}^{1},x_{k}^{2})$$Then, $$X\subseteq\bigcup_{i=1}^{nk}B_{d}(x_{k},\epsilon)$$since if $y=(y_{1},y_{2})\in X_{1}\times X_{2}$, then there is an $i,j$ such that $$d_{1}(y_{1},x_{i}^{1})<\frac{\epsilon}{2}\text{ and }d_{2}(y_{2},x_{j}^{2})<\frac{\epsilon}{2}$$Then, $$d(y,(x_{i}^{1},x_{j}^{2}))=d_{1}(y_{1},x_{i}^{1})+d_{2}(y_{2},x_{j}^{2})=\frac{\epsilon}{2}+ \frac{\epsilon}{2}=\epsilon$$so, $y\in B_{d}((x_{i}^{1},x_{j}^{2}),\epsilon)$. [[therefore]] $X_{1}\times X_{2}$ is [[Totally Bounded]].
>
>>[!prop] Lemma
A [[Sequence]] $(x_{n}^{1},x_{n}^{2})$ in $X_{1}\times X_{2}$ [[Converges (Sequence)]] to $(x_{1},x_{2})$ if $x_{n}^{1}\rightarrow x_{1}$ in $X_{1}$ and $x_{n}^{2}\rightarrow x_{2}$ in $X_{2}$. 
>>>[!proof]
Let $\epsilon>0$ be given. Pick $N_{1},N_{2}\in \mathbb{N}$ such that if $n_{1}≥N_{1},n_{2}≥N_{2}$, then $$d_{1}(x_{1},x_{n_{1}}^{1})<\frac{\epsilon}{2}\text{ and }d_{2}(x_{2},x_{n_{2}}^{2})< \frac{\epsilon}{2}$$Let $N=\max\{N_{1},N_2\}$. Then, if $n≥N$, $$d((x_{1},x_{2}),(x_{n}^{1},x_{n}^{2}))=d_{1}(x_{1},x_{n}^{1})+d_{2}(x_{2},x_{n}^{2})< \frac{\epsilon}{2} + \frac{\epsilon}{2}=\epsilon$$so, $(x_{n}^{1},x_{n}^{2})\rightarrow (x_{1},x_{2})$ in $X_1\times X_{2}$.
>
Suppose that $X_{1},X_{2}$ are [[Complete]]. Let $(x_{n}^{1},x_{n}^{2})$ be [[Cauchy Sequence]] in $X_{1}\times X_{2}$. Then, $x_n^1,x_n^2$ are [[Cauchy Sequence]] in $X_{1},X_{2}$, respectively ([[9-12 Problems]]). [[therefore]] $x_{n}^{1}\rightarrow x_{1}\in X_{1}$ and $x_{n}^{2}\rightarrow x_{2}\in X_{2}$ by [[Complete]]ness. By the lemma, $(x_{n}^{1},x_{n}^{2})\rightarrow (x_{1},x_{2})$. So, every [[Cauchy Sequence]] [[Sequence]] in $X_{1}\times X_{2}$ [[Converges (Sequence)]] in $X_{1}\times X_{2}$ so, $X_{1}\times X_{2}$ is [[Complete]]. 
>
So, the [[Characterizations of Compactness]] implies that $X_{1}\times X_{2}$ is [[Compactness]].
