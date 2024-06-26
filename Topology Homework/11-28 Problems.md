From 2.7: 3, 8

>[!note] 3
Let $f:X \rightarrow Y$ be [[Continuity at a Point]] $x\in X$ and let $(x,I)$ be a [[Net]] in $X$ with $x_{i}$ [[notation for clusters]] $x$. Let $V$ be a [[Neighborhood]] of $f(x)$ and let $j\in I$. Then, $f^{-1}(V)$ is [[Open Set]] in $X$, since $f$ is [[Continuous]] at $x$. Pick $i≥j$ such that $x_{i}\in f^{-1}(V)$. Then, $f(x_{i})\in V$, so $f(x_{i})\rightarrow _\text{cl}x$.
>
The converse is not true. Let $f:\mathbb{R}\rightarrow \{0\}$ and let $\{x_{i}:i\in \mathbb{N}\}$ be a [[Net]] defined by $x_{i}=i$. Then, $f$ is [[Continuous]] on $\mathbb{R}$, $f(x_{i})\rightarrow _\text{cl }0$, but $x_{i}$ does not have a [[Clusters]] point.


I am taking the converse to be the statement: let $f$ be a [[Continuous]] [[Function]]; then whenever $\{x_{i}\}$ is [[Net]] in $X$, if $f(x_{i})$ [[notation for clusters]] $f(x)$ for some $x\in X$, then $x_{i}\rightarrow _\text{cl }x$. 

Explain what the statement is that I am viewing as the converse


>[!note] 8
Let $X=\mathbb{N}$ with the [[Discrete Topology]] and let $I=\mathbb{N}$. Let $(x,I)$ be a [[Net]] defined by $$x_{2i}=1,x_{2i+1}=i$$Then, $x_{i}$ [[notation for clusters]] $1$, does not [[Converges (net)]] to $1$, and does not [[Clusters]] at any other point.
