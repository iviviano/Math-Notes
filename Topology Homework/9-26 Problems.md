From 1.4: 9 and 10

>[!note] 9
Let $X=\mathbb{R}$. Let $Z=\{1\}$. Let $f:X \mapsto Z$ have the [[Rule of Assignment]] $f(x)=1$. Clearly, $Z$ is [[Compactness]] and $f(X)=Z$.

>[!note] 10
(a) Clearly $\text{dist }(A,B)=\text{dist }(B,A)$ as $d$ is a [[Metric]]. Clearly, $\text{dist }(B,A)≥\text{dist }(\text{cl }A,\text{cl }B)$ as $A\subseteq \text{cl }A$ and $B\subseteq \text{cl }B$. Assume that $x=\text{dist }(B,A)>\text{dist }(\text{cl }A,\text{cl }B)=y$. Then, $x$ is not a lower bound for $\{d(a,b):a\in \text{cl }A,b\in \text{cl }B\}$, so there exist points $a'\in \text{cl }A,b'\in \text{cl }B$ such that $d(a',b')<x$. Note: for all $\epsilon>0$, there exists $a\in A,b\in B$ with $d(a,a')<\frac{\epsilon}{2}$ and $d(b,b')<\frac{\epsilon}{2}$. This gives $$d(a,b)≤d(a,a')+d(a',b')+d(b,b')<x+\epsilon$$So, for all $\epsilon>0,d(a,b)-x<\epsilon$. [[therefore]] $d(a,b)-x<0\implies d(a,b)<x$. This contradicts the assumption that $x$ is a lower bound for $\{d(a,b):a\in A,b\in B\}$, so $\text{dist }(B,A)>\text{dist }(\text{cl }A,\text{cl }B)$ is false. Together with the first observation, $\text{dist }(A,B)=\text{dist }(\text{cl }A,\text{cl }B)$.



Let $A,B$ be [[Disjoint]] [[Closed Set]] [[Subset]]s of $X$ and let $B$ be [[Compactness]]. Let $x=\text{dist }(A,B)$. Let $\epsilon>0$ be given. Pick $a\in A,b\in B$ such that $d(a,b)<x+\epsilon$ (as $x$ is the [[infinum]]). 

For $a\in A,b\in B$, $d(a,b)≥x$. Also, for $b'\in B\cap B_{d}(b,\epsilon)$ $d(a,b')≥x$, $d(a,b)≤$

Suppose that $\text{dist }(A,B)=0$ and $A,B$ are [[Closed Set]] and [[Disjoint]]. Then, for all $\epsilon>0$ we can pick $a\in A,b\in B$ such that $d(a,b)<\epsilon$. Suppose that $B$ is [[Totally Bounded]]. Then, there is a finite collection of points $b_{1},\ldots,b_{n}$ such that $$B\subseteq\bigcup_{k=1}^{n}B_{d}(b_{k},\epsilon)$$
Pick $k$ such that $b\in B_{d}(b_{k},\epsilon)$. Then, 


(b) Let $A,B$ be [[Disjoint]], [[Closed Set]] [[Subset]]s of $X$ and let $B$ be [[Compactness]]. Use the result of (7). As $X-A$ is an [[Open Set]] [[Set]] containing $B$, there exists a $\delta>0$ such that $$\{x:\text{dist }(x,B)<\delta\}\subseteq G$$So, for all $a\in A,b\in B$, $\delta≤d(a,b)$. [[therefore]] $\text{dist }(A,B)>0$.

(c) $A=\mathbb{N}\times\{0\}$, $B=\{n- \frac{1}{n}:n\in \mathbb{N}\}\times\{0\}$. 

(d) Definitely.


7 (a)

For each $x\in K$, pick $\epsilon_{x}$ such that $B_{d}(x,\epsilon_x)\subseteq U$. Then, $$\mathcal{U}=\{B_{d}(x,\epsilon_{x}):x\in K\}$$is an [[Open Cover]] of $K$. Let $\mathcal{U}$ omit the finite [[Subcover]] given by $\{x_{1},\ldots,x_{n}\}$. 

Claim: for some $1≤i≤n$, $x_{i}\notin B_{d}(x_{i},\epsilon_{x_{i}})-K≠\emptyset$ (JUSTIFY). Suppose not: $$\bigcup_{i=1}^{n}(B_{d}(x_{i},\epsilon_{x_{i}})-K)=\left(\bigcup_{i=1}^{n}B_{d}(x_{i},\epsilon_{x_{i}})\right)-K=\emptyset$$(JUSTIFY FIRST EQUALITY). This implies that $K=$ the union as it also covers $K$.

Let $$\delta=\frac{1}{2}\min\{\sup\{d(x_{i},x):x\in B_{d}(x_{i},\epsilon_{{x}_{i}})-K\}>0|1≤i≤n\}$$Note: this implies that $\delta<\min\{\epsilon_{x_{i}}\}$. Then, $\delta>0$ and exists. Suppose $\text{dist }(x,K)<\delta$. If $x\in K$, then $x\in G$. If $x\notin K$, then there is an $i$ such that $x\in B_{d}(x_{i},\epsilon_{x_{i}})$ (JUSTIFY). As $B_{d}(x_{i},\epsilon_{x_{i}})\subseteq G$, $x\in G$.

(NOTE: Inner sup is [[Diameter]]?)