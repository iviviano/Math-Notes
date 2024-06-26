From 1.3: 12, 13

>[!note] 12
Let $(X,d_{X}),(Y,d_{Y}),(Z,d_{Z})$ be [[Metric Space]]s. Let $f:X \rightarrow Y,g:Y \rightarrow Z$ be [[Uniform Continuity]] [[Function]]s. Let $\epsilon>0$ be given. Pick $\delta_{1}>0$ such that for all $y_{0}\in Y$, $$y\in B_{d_{Y}}(y,\delta_{1})\implies g(y)\in B_{d_{Z}}(g(y_{0})\epsilon)$$Now pick $\delta_{0}$ such that for all $x_{0}\in X$,$$x\in B_{d_{X}}(x_{0},\delta_{0})\implies f(x)\in B_{d_{X}}(f(x_{0},\delta_{1}))$$Then, for all $x_{0}\in X$, $$x\in B_{d_{X}}(x_{0},\delta_{0})\implies g\circ f(x)\in B_{d_{Z}}(g\circ f(x_{0}),\epsilon)$$so, $g\circ f:X \rightarrow Z$ is [[Uniform Continuity]].



>[!prop] Lemma
>Finite [[Set]]s in [[Metric Space]]s are [[Closed Set]]
>>[!proof]
>>I will show that all singletons are closed. It follows from [[Principle of Mathematical Induction]] and the fact that finite [[Union]]s of [[Closed Set]] [[Set]]s are [[Closed Set]] that all finite sets are [[Closed Set]].
Let $x\in X$, $y\in X-\{x\}$ be given. Pick $\epsilon<d(x,y)$. Then, $$x\notin B_{d}(y,\epsilon)\subseteq X-\{x\}$$so $X-\{x\}$ is [[Open Set]] and $\{x\}$ is [[Closed Set]]

>[!note] 13
Note: For any [[Metric Space]] $(X,d)$, $C(X)$ is a [[Vector Space]], which follows from the [[Constructing Continuous Functions Theorem]].
>
Suppose $X$ is finite. For each $x\in X$, if $A=\{x\}$ and $B=X-A$, then $A$ and $B$ are [[Closed Set]] as all [[Set]]s are [[Closed Set]] by the lemma. Note: $A$ and $B$ are [[Disjoint]]. So, by [[Urysohn's Lemma]], there is a [[Continuous]] [[Function]] $f_{x}:X \rightarrow\mathbb{R}$ such that $f(x)=1$ and $f(y)=0$ for all $y\in B$. 
Claim: $\mathcal{B}=\{f_{x}:x\in X\}$ is a basis for the [[Vector Space]] [[Vector Space of Continuous Functions]]$(X)$. Clearly, the elements of $\mathcal{B}$ are [[Linearly Independent]] of each other. Let $f:X \rightarrow \mathbb{R}$ be a [[Function]]. Enumerate the elements of $X:\{x_{1},\ldots,x_{n}\}$. Then, $$f(x)=\sum_{i=1}^{n}f(x_{i})f_{x_{i}}(x)$$ which is a [[Linear Combination]] of elements of $\mathcal{B}$. As the [[Cardinality]] of $\mathcal{B}$ is $n$, the [[Dimension]] of $C(X)$ is $n$.
>
Suppose $X$ is infinite. Let $\{x_{1},\ldots,x_{n}\}\in X$ be $n$ distinct points. For each $1≤i≤n$, pick a [[Continuous]] [[Function]] $f_{i}:X \rightarrow \mathbb{R}$ such that $f_{i}(x_{i})=1$, $f_{i}(x_{j})=0$ for $j≠i$, and $0≤f_{i}(x)≤1$ for all $x\in X$ (by [[Urysohn's Lemma]]. Then, pick $x\notin\{x_{1},\ldots,x_{n}\}$. Let $f:X \rightarrow \mathbb{R}$ be a [[Continuous]] [[Function]] such that $f(x)=1$ and $f(x_{i})=0$ for all $1≤i≤n$ again with [[Urysohn's Lemma]] and the lemma that finite sets are closed. Suppose there exist constants $c_{1},\ldots,c_{n}$ such that $$f=c_{1}f_{1}+\ldots c_{n}f_{n}$$Clearly the [[Constructing Continuous Functions Theorem]] implies that $f$ is [[Continuous]]. Then, for each $1≤i≤n$, $$f(x_{i})=0=c_{i}f(x_{i})=c_{i}1=c_{i}$$So $f=0$. But $f(x)=1$. As this is a contradiction, $f$ is [[Linearly Independent]] from $f_{1},\ldots,f_{n}$. [[therefore]] that $C(X)$ is $n$ dimensional [[implies]] $C(X)$ is $n+1$ dimensional, so it must have infinite dimension.
