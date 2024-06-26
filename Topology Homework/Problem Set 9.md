<p align=center>
Topology <br>
Problem Set 9 <br>
Isaac Viviano
</p>

---

>[!note] 2.5.2
Let $p=(p_x,p_y),q=(q_x,q_y)\in C$. Let $f:[0,1]\rightarrow C$ be defined by $$f(t)=\left(p_{x},1-\frac{t}{p_{y}}\right)$$Then, $f$ is a [[Path]] from $p$ to $(p_{x},0)$. Let $g:[0,1]\rightarrow C$ be defined by $$g(t)=\left(\frac{t}{q_{x}-p_{x}},0\right)$$Then, $g$ is a path from $(p_{x},0)$ to $(q_{x},0)$. Let $h:[0,1]\rightarrow C$ be defined by $$h(t)=\left(q_{x},\frac{1-t}{q_{y}}\right)$$Then, $h$ is a [[Path]] from $(q_{x},0)$ to $q$. So, $f\cdot g\cdot h$ is a [[Path]] from $p$ to $q$ in $C$ by the [[Product of Paths Proposition]]. So, $C$ is [[Pathwise Connectedness]], and therefore [[Connected]]

>[!note] 2.5.3
The same argument from $2$ may be used to show that $X-\{(0,1)\}$ is [[Pathwise Connectedness]] and thus [[Connected]]. $B_{X}((0,1), \frac{1}{n})\ni(\frac{1}{n+1},1)\in X-\{(0,1)\}$, so $(0,1)$ is a [[Limit Point]] of $X-\{0,1\}$. Therefore, $X-\{(0,1)\}\subseteq X\subseteq \text{cl }X$, so $X$ is [[Connected]] by the [[Closure of Connected Sets Proposition]].
>
Suppose there was a [[Continuous]] [[Function]] $f:[0,1]\rightarrow X$ with $f(0)=(0,1)$ and $f(1)=(1,0)$. Then, $f([0,1])$ is [[Connected]] by the [[Intermediate Value Theorem]]. But $f([0,1])$ may be covered by two [[Disjoint]] [[Open Set]] [[Subset]]s of $\mathbb{R}^{2}$: 
![[IMG_1305.jpg|400]]
So, $U\cap f([0,1])$ and $V\cap f([0,1])$ are relatively [[Open Set]] [[Subset]]s of $f([0,1])$. But this implies $f([0,1])$ is not [[Connected]], contradicting the assumption that there is a [[Path]] from $(0,1)$ to $(1,0)$.

>[!note] 2.6.1
Note: I think there is a typo in the text. I believe the question should ask us to show $\phi:X_{j}\rightarrow X$ is a [[Homeomorphism]] of $X_{j}$ onto $\phi(X_{j})$. 
>
Fix $j$ and $y\in X$. 
>
Clearly, $\phi:X_{j}\rightarrow \phi(X_{i})$ is [[Surjective]]. Let $a,b\in X$. Note: $\phi(a)_{j}=a$ and $\phi(b)_{j}=b$. If $\phi(a)=\phi(b)$, then $\phi(a)_{j}=\phi(b)_{j}$ and thus $a=b$. Therefore, $\phi$ is [[Injective]]. So, $\phi:X_{j}\rightarrow \phi(X_{j})$ is [[Bijective]].
>
Let $U\subseteq X_{j}$ be [[Open Set]]. Let$$V=\prod_{i≠j}X_{i}\times \pi_{j}(\phi(U))$$Then, $\phi(U)=V\cap \phi(X_{j})$: for all $i≠j$, $\phi(U)_{i}=\{y_{i}\}=\phi(X_{j})_{i}$ and $\phi(U)_{j}=\pi_{j}(\phi(U))$. As $V$ is a [[Subbasis]] element of $X$, it is [[Open Set]] in the [[Product Topology]] on $X$ by [[10-31 Problems]]. So, $V\cap \phi(X_{j})$ is [[Open Set]] in the [[Subspace]] $\phi(X_{j})$. Therefore, $\phi$ is an [[Open Map]]. 
>
Let $U\subseteq \phi(X_{j})$ be [[Open Set]]. Pick $V\subseteq X$ [[Open Set]] such that $U=V\cap \phi(X_{j})$. Then, $$\phi^{-1}(U)=\phi^{-1}(V)$$For all $x\in V$, $x_{j}\in \phi^{-1}(V)$. So, $\phi^{-1}(V)=\pi_{j}(V)$. As [[Projection]] maps are [[Open Map]], $\phi^{-1}$ is [[Open Set]].
>
As $\phi$ and $\phi^{-1}$ are [[Open Map]] maps, $\phi$ is a [[Homomorphism]]. 

>[!note] 3
(a) Let $U\subseteq \mathbb{R}$ be [[Open Set]]. Fix $i\in \mathbb{N}$. Then, $$\pi_{i}^{-1}(U)=\mathbb{R}^{i-1}\times U\times \mathbb{R}\times \mathbb{R}\times\cdots$$If $f(x)\in \pi_{i}^{-1}(U)$, then $x\in \pi_{j}^{-1}(U)$ for all $j$. Therefore, $x\in U$. So, $(f^{-1}\circ \pi_{i}^{-1})(U)=U$. As $U$ was an arbitrary [[Open Set]] [[Set]], $\pi_{i}\circ f$ is [[Continuous]] for all $i$.
>
Let $x\in f^{-1}\left(\prod_{n=1}^{\infty}\left(\frac{-1}{n},\frac{1}{n}\right)\right)$. If $|x|>0$, pick $n\in \mathbb{N}$ such that $\frac{1}{n}<|x|$. Then, $x\notin\left(\frac{-1}{n},\frac{1}{n}\right)$. So, $(x,x,\ldots)\notin\prod_{n=1}^{\infty}\left(\frac{-1}{n},\frac{1}{n}\right)$. Therefore, $x=0$, so $f^{-1}\left(\prod_{n=1}^{\infty}\left(\frac{-1}{n},\frac{1}{n}\right)\right)=\{0\}$, a non-[[Open Set]] [[Set]] in $\mathbb{R}$. Therefore, $f^{-1}$ is not an [[Open Map]] map, so $f$ is not [[Continuous]].
>
(b) Let $A\subseteq X$. Let $$A=A_{1}\times A_{2}\times\cdots$$For each $n$, $A_{n}\subseteq\{0,1\}$. So, $A_{n}\in T_{i}$, since all [[Subset]]s are [[Open Set]] in the [[Discrete Topology]]. Therefore, $A$ is a [[Subbasis]] element, so it is [[Open Set]] in the [[Box Topology]]. As $A$ was arbitrary, all [[Subset]]s of $X$ are [[Open Set]] in the [[Box Topology]]. So, the [[Box Topology]] on $X$ is the [[Discrete Topology]]. 


