From 2.7: 1, 2

>[!note] 1
Suppose $x_{n}\rightarrow x$ as a [[Sequence]]. Note: $(x,\mathbb{N})$ is a [[Net]]. Let $U$ be a [[Neighborhood]] of $x$. Pick $N\in$ $\mathbb{N}$ such that if $n≥N$, $x_{n}\in U$. Let $i_{0}=N$. If $i\in \mathbb{N}$ and $i≥i_{0}$, then $i≥N$. So, $x_{i}\in U$. Therefore, $x_{i}\rightarrow x$ as net.
>
Suppose $x_{i}\rightarrow x$ as a [[Net]]. Let $U$ be a [[Neighborhood]] of $x$. Pick $i_{0}$ such that if $i\in \mathbb{N}$ and $i≥i_0$, $x_{i}\in U$. Let $N=i_{0}$. If $n\in \mathbb{N}$ and $n≥N$, then $n≥i_{0}$. So, $x_{n}\in U$. Therefore, $x_{n}\rightarrow x$ as a [[Sequence]].
>
Let $X=\{x_{n}:n\in \mathbb{N}\}$
>
Suppose $x_{n}$ [[notation for clusters]] $x$. Let $U$ be a [[Neighborhood]] of $x$ and let $j\in \mathbb{N}$ be given. Pick $i\in \mathbb{N}$ such that $x_{i}\in U$ and $i≥j$. Then, $x_{i}\in U\cap X$, so $x$ is a [[Limit Point]] of $X$. 
>
Suppose $x$ is a [[Limit Point]] of $X$. Let a [[Neighborhood]] $U$ of $x$ and $j\in \mathbb{N}$ be given. By the Hausdorff property, pick a [[Neighborhood]] $V\subseteq U$ of $x$ with $x_{i}\notin U$ for all $i≤j$ (can do this pairwise and with induction, since finite [[Intersection]]s of [[Open Set]] [[Set]]s are [[Open Set]]). There must be some element of $X$ in $V$ besides $X$ by the definition of [[Limit Point]]. So, there exists $i≥j$ such that $x_{i}\in V$. Therefore, $x$ is a [[Clusters]] point of $X$.


>[!note] 2
(a) Suppose $(x,I)$ [[Converges (net)]]s to $x_{0}$. Let $U$ be a [[Neighborhood]] of $x_0$ and let $j\in \mathbb{N}$ be given. Pick $i_{0}$ such that if $i\in I$ and $i≥i_{0}$, $x_{i}\in U$. Let $i=\max\{i_{0},j\}$. Then, $i≥j$ and $x_{i}\in U$, so $x_{i}$ [[notation for clusters]] $x_{0}$.
>
(b) Suppose $(x, I)$ [[Converges (net)]]s to two unique points $x_{0},y_{0}$. Let $U,V$ be [[Disjoint]] [[Neighborhood]]s of $x_{0},y_{0}$. Pick $i_{x},i_{y}$ such that if $i\in I$ and $i≥i_{x}$, $x_{i}\in U$, and $i\in I$ and $i≥i_{y}$ [[implies]] $x_{i}\in V$. Pick $i≥i_{x},i_{y}$. Then, $x_{i}\in U,V$, contradicting that $U,V$ are [[Disjoint]]. So, [[Net]]s [[Converges (net)]] uniquely in [[Hausdorff Space]]s.
