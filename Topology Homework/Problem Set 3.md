<p align=center>
Topology <br>
Problem Set 3 <br>
Isaac Viviano
</p>

---

>[!note] 1.3.12
Let $(X,d_{X}),(Y,d_{Y}),(Z,d_{Z})$ be [[Metric Space]]s. Let $f:X \rightarrow Y,g:Y \rightarrow Z$ be [[Uniform Continuity]] [[Function]]s. Let $\epsilon>0$ be given. Pick $\delta_{1}>0$ such that for all $y_{0}\in Y$, $$y\in B_{d_{Y}}(y,\delta_{1})\implies g(y)\in B_{d_{Z}}(g(y_{0})\epsilon)$$Now pick $\delta_{0}$ such that for all $x_{0}\in X$,$$x\in B_{d_{X}}(x_{0},\delta_{0})\implies f(x)\in B_{d_{X}}(f(x_{0},\delta_{1}))$$Then, for all $x_{0}\in X$, $$x\in B_{d_{X}}(x_{0},\delta_{0})\implies g\circ f(x)\in B_{d_{Z}}(g\circ f(x_{0}),\epsilon)$$so, $g\circ f:X \rightarrow Z$ is [[Uniform Continuity]].

>[!prop] Lemma
>Finite [[Set]]s in [[Metric Space]]s are [[Closed Set]]
>>[!proof]
>>I will show that all singletons are closed. It follows from the fact that finite [[Union]]s of [[Closed Set]] [[Set]]s are [[Closed Set]] that all finite sets are [[Closed Set]].
Let $x\in X$, $y\in X-\{x\}$ be given. Pick $\epsilon<d(x,y)$. Then, $$x\notin B_{d}(y,\epsilon)\subseteq X-\{x\}$$so $X-\{x\}$ is [[Open Set]] and $\{x\}$ is [[Closed Set]]

>[!note] 1.3.13
Note: For any [[Metric Space]] $(X,d)$, $C(X)$ is a [[Vector Space]], which follows from the [[Constructing Continuous Functions Theorem]].
>
Suppose $X$ is finite. For each $x\in X$, if $A=\{x\}$ and $B=X-A$, then $A$ and $B$ are [[Closed Set]] as all [[Set]]s are [[Closed Set]] by the lemma. Note: $A$ and $B$ are [[Disjoint]]. So, by [[Urysohn's Lemma]], there is a [[Continuous]] [[Function]] $f_{x}:X \rightarrow\mathbb{R}$ such that $f(x)=1$ and $f(y)=0$ for all $y\in B$. 
Claim: $\mathcal{B}=\{f_{x}:x\in X\}$ is a basis for the [[Vector Space]] [[Vector Space of Continuous Functions]]$(X)$. Clearly, the elements of $\mathcal{B}$ are [[Linearly Independent]] of each other. Let $f:X \rightarrow \mathbb{R}$ be a [[Function]]. Enumerate the elements of $X:\{x_{1},\ldots,x_{n}\}$. Then, $$f(x)=\sum_{i=1}^{n}f(x_{i})f_{x_{i}}(x)$$ which is a [[Linear Combination]] of elements of $\mathcal{B}$. As the [[Cardinality]] of $\mathcal{B}$ is $n$, the [[Dimension]] of $C(X)$ is $n$.
>
Suppose $X$ is infinite. Let $\{x_{1},\ldots,x_{n}\}\in X$ be $n$ distinct points. For each $1≤i≤n$, pick a [[Continuous]] [[Function]] $f_{i}:X \rightarrow \mathbb{R}$ such that $f_{i}(x_{i})=1$, $f_{i}(x_{j})=0$ for $j≠i$, and $0≤f_{i}(x)≤1$ for all $x\in X$ (by [[Urysohn's Lemma]]. Then, pick $x\notin\{x_{1},\ldots,x_{n}\}$. Let $f:X \rightarrow \mathbb{R}$ be a [[Continuous]] [[Function]] such that $f(x)=1$ and $f(x_{i})=0$ for all $1≤i≤n$ again with [[Urysohn's Lemma]] and the lemma that finite sets are closed. Suppose there exist constants $c_{1},\ldots,c_{n}$ such that $$f=c_{1}f_{1}+\ldots c_{n}f_{n}$$Clearly the [[Constructing Continuous Functions Theorem]] implies that $f$ is [[Continuous]]. Then, for each $1≤i≤n$, $$f(x_{i})=0=c_{i}f(x_{i})=c_{i}1=c_{i}$$So $f=0$. But $f(x)=1$. As this is a contradiction, $f$ is [[Linearly Independent]] from $f_{1},\ldots,f_{n}$. [[therefore]] that $C(X)$ is $n$ dimensional [[implies]] $C(X)$ is $n+1$ dimensional, so it must have infinite dimension.

>[!note] 1.4.1
Let $\{K_{n}\}$ be a finite collection of [[Compactness]] [[Set]]s, let $K=\bigcup K_{n}$, let $\mathcal{U}$ be an [[Open Cover]] of $K$. For each $n$, pick a finite [[Subcover]] $\mathcal{U}_{n}$ of $\mathcal{U}$ such that $\mathcal{U_{n}}$ [[Cover]]s $K_{n}$. Then, $$\mathcal{U}'=\bigcup \mathcal{U}_{n}$$is an [[Open Cover]] of $K$. It is finite as it is a finite [[Union]] of finite [[Set]]s, and it is a [[Subcover]] of $\mathcal{U}$ as each $\mathcal{U}_{n}$ is. [[therefore]] $K$ is [[Compactness]].

>[!note] 1.4.2
Suppose $K$ is [[Compactness]] and let $\mathcal{U}$ be a relatively [[Open Cover]] of $K$. Then, for each $U\in \mathcal{U}$, there is a $U'\subseteq X$ that is [[Open Set]] in $X$ and $U=K\cap U'$. Let $\mathcal{U}'$ be the [[Collection]] of these $U'$ for each $U\in \mathcal{U}$. Pick a finite [[Subcover]] $\mathcal{U}^{*}$ of $\mathcal{U}$ that [[Cover]]s $K$. For each $U\in \mathcal{U}^{*}$, $U\cap K\in \mathcal{U}$. So, $\{U\cap K:U\in \mathcal{U}^*\}\subseteq \mathcal{U}$. Additionally, $$\bigcup_{U\in \mathcal{U}^{*}}U\cap K=K\cap \bigcup\{U:U\in \mathcal{U}^*\}$$as [[Unions and Intersections Commute]]. As $K$ is [[Cover]]ed by $\bigcup \{U\in \mathcal{U}^{*}\}$, $\{U\cap K:U\in \mathcal{U}^{*}\}$ is an finite [[Subcover]] of $\mathcal{U}$.
>
Suppose that every relatively [[Open Cover]] of $K$ omits a finite [[Subcover]]. Let $\mathcal{U}$ be an [[Open Cover]] of $K$. Let $$\mathcal{U}^{'}=\{U\cap K:U\in \mathcal{U} \}$$As each element of $\mathcal{U}'$ is [[Open Set]] in $K$ and $$\bigcup_{U'\in \mathcal{U}'}U'=\bigcup_{U\in \mathcal{U}}U\cap K=K\cap \bigcup \{U\in \mathcal{U}\}\supseteq K$$[[therefore]] $\mathcal{U}^{'}$ is a relatively [[Open Cover]] of $K$. So, $\mathcal{U}'$ omits a finite [[Subcover]]: $\{U_{n}\cap K: U\in \mathcal{U},1≤n≤k\}$ for some $k$ of $K$. Note that this implies $\{U_{n}:U\in \mathcal{U}\}$ is also a finite [[Subcover]] of $K$, so $K$ is [[Compactness]].

>[!note] 1.4.8
Suppose that $X_{1}\times X_{2}$ is [[Compactness]]. Let $\pi_{1}:X_{1}\times X_{2}\mapsto X_{1}$ be the [[Projection]] map. Clearly, $\pi_{1}(X_{1}\times X_{2})=X_{1}$. By [[9-14 Problems]], $\pi_{1}$ is [[Continuous]]. By the [[Characterizations of Compactness]], $X_{1}$ is [[Compactness]]. Similarly, $X_{2}$ is [[Compactness]].
>
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
So, the [[Characterizations of Compactness]] implies that $X_{1}\times X_{2}$ is [[Compactness]] if $X_{1},X_{2}$ are [[Compactness]].

