<p align = center>
Topology<br>
Problem Set 10<br>
Isaac Viviano
</br>

>[!note] 2.6.2
Let $\mathcal{S}=\{f^{-1}(U):U \text{ is open in }\mathbb{R},f\in C(X)\}$. Let $x,y\in X$. Then, there is a [[Continuous]] [[Function]] $f:X \rightarrow \mathbb{R}$ mapping $x\mapsto 0$ and $y\mapsto1$ by [[Urysohn's Lemma]]. So, $f^{-1}(B(0,\frac{1}{2}))$ and $f^{-1}(B(1,\frac{1}{2}))$ are [[Disjoint]] [[Neighborhood]]s of $x$ and $y$. Therefore, $\mathcal{S}$ is a [[Subbasis]] for the [[Weak Topology]] on $X$.
>
Let $x_{0}\in X$ and $\epsilon>0$ be given. For each $x\in B_{d}(x_{0},\epsilon)$, construct $f_{x}$ with $f_{x}(y)=0$ on $$X-B_{d}\left(x_{0},\frac{d(x,x_{0})+\epsilon}{2}\right)$$(this is a [[Closed Set]] [[Subset]] of $X$ not containing $x$ and containing everything in $X$ outside of $B_{d}(x_{0},\epsilon)$) and $f_{x}(y)=1$ on $$\text{cl }B\left(x,\frac{\epsilon-d(x,x_{0})}{4}\right)$$(this is a [[Closed Set]] [[Subset]] of $X$ contained in $B_{d}(x_{0},\epsilon)$ and [[Disjoint]] from the other set). The by [[Urysohn's Lemma]] $f_{x}$ may be made [[Continuous]]. Let $U_{x}=\left(\frac{1}{2},\frac{3}{2}\right)$. Since $0\notin U$, $x\in f_{x}^{-1}(U)\subseteq B_{d}(x_{0},\epsilon)$. And $f_{x}^{-1}(U)$ is [[Open Set]] in the [[Weak Topology]] since $f_{x}$ is [[Continuous]].  So, $$\bigcup_{x\in B_{d}(x,\epsilon)}f_{x}^{-1}(U)=B_{d}(x_{0},\epsilon)$$As every [[Basis of a Topology]] element of the [[Metric Topology]] on $X$ is [[Open Set]] in the [[Weak Topology]], the [[Metric]] [[Topology]] is [[Finer]] than the [[Weak Topology]].
>
Let $U\in \mathcal{S}$. Then, there exists $f\in C(X)$, $V\subseteq \mathcal{\mathbb{R}}$ such that $U=f^{-1}(V)$ and $V$ is [[Open Set]]. As $f$ is [[Continuous]], $f^{-1}(V)$ is [[Open Set]] in the [[Metric Topology]] on $X$ by the definition of [[Continuous]]. So, $U$ is [[Open Set]] in the [[Metric Topology]] on $X$. Given an arbitrary $U$ in the [[Topology]] generated by $\mathcal{S}$, we could write $U$ as an arbitrary [[Union]] of finite [[Intersection]]s of elements of $\mathcal{S}$. Each of these are [[Open Set]] in the [[Metric Topology]] on $X$. So, the [[Set]] $U$ is [[Open Set]] in the [[Metric Space]] $X$ by the [[Topology]] axioms. 
>
This double containment shows the equality of the [[Weak Topology]] on $X$ generated by the [[Function]]s in $C(X)$ and the [[Metric Topology]] on $X$.

>[!note] 2.6.4
Let $X_{i}=\mathbb{R}$ for $i\in \mathbb{N}$. Let $$A=\{(x_{1},x_{2},\ldots):\text{the sequence }\{x_{n}\}\text{ is bounded}\}$$$A$ is [[Open Set]]: let $x\in A$ be given. Then, $$U=(x_{1}-1,x_{1}+1)\times(x_{2}-1,x_{2}+1)\times\cdots$$is a [[Neighborhood]] of $x$ in $X$. Let $M$ be a bound for the sequence $x_{n}$. Then, if $y\in U$, $M+1$ is a bound for the [[Sequence]] $y_{n}$. So, $U\subseteq A$.
>
$A$ is [[Closed Set]]: let $x\in X-A$ be given. So, the [[Sequence]] $\{x_{n}\}$ is not bounded. Let $M>0$ be given and let $$y\in(x_{1}-1,x_{1}+1)\times(x_{2}-1,x_{2}+1)\times\cdots$$Pick $n$ such that $x_{n}>M+1$ since $\{x_n\}$ is not bounded. Then, $y_{n}>M$, so $\{y_{n}\}$ is also not bounded. This shows that $X-A$ is [[Open Set]].
>
As $X$ has a proper [[Subset]] that is [[Closed Set]], [[Open Set]], and nonempty, $X$ is not [[Connected]].

>[!note] 2.7.2
(a) Suppose $(x,I)$ [[Converges (net)]]s to $x_{0}$. Let $U$ be a [[Neighborhood]] of $x_0$ and let $j\in \mathbb{N}$ be given. Pick $i_{0}$ such that if $i\in I$ and $i≥i_{0}$, $x_{i}\in U$. Let $i=\max\{i_{0},j\}$. Then, $i≥j$ and $x_{i}\in U$, so $x_{i}$ [[notation for clusters]] $x_{0}$.
>
(b) Suppose $(x, I)$ [[Converges (net)]]s to two unique points $x_{0},y_{0}$. Let $U,V$ be [[Disjoint]] [[Neighborhood]]s of $x_{0},y_{0}$. Pick $i_{x},i_{y}$ such that if $i\in I$ and $i≥i_{x}$, $x_{i}\in U$, and $i\in I$ and $i≥i_{y}$ [[implies]] $x_{i}\in V$. Pick $i≥i_{x},i_{y}$. Then, $x_{i}\in U,V$, contradicting that $U,V$ are [[Disjoint]]. So, [[Net]]s [[Converges (net)]] uniquely in [[Hausdorff Space]]s.