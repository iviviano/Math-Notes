From 2.5: 2 and 3

>[!note] 2
Let $p=(p_x,p_y),q=(q_x,q_y)\in C$. Let $f:[0,1]\rightarrow C$ be defined by $$f(t)=\left(p_{x},1-\frac{t}{p_{y}}\right)$$Then, $f$ is a [[Path]] from $p$ to $(p_{x},0)$. Let $g:[0,1]\rightarrow C$ be defined by $$g(t)=\left(\frac{t}{q_{x}-p_{x}},0\right)$$Then, $g$ is a path from $(p_{x},0)$ to $(q_{x},0)$. Let $h:[0,1]\rightarrow C$ be defined by $$h(t)=\left(q_{x},\frac{1-t}{q_{y}}\right)$$Then, $h$ is a [[Path]] from $(q_{x},0)$ to $q$. So, $f\cdot g\cdot h$ is a [[Path]] from $p$ to $q$ in $C$ by the [[Product of Paths Proposition]]. So, $C$ is [[Pathwise Connectedness]], and therefore [[Connected]]

Note: can also use [[Unions of Overlapping Pathwise Connected Sets are Pathwise Connected]].


>[!note] 3
The same argument from $2$ may be used to show that $X-\{(0,1)\}$ is [[Pathwise Connectedness]] and thus [[Connected]]. $B_{X}((0,1), \frac{1}{n})\ni(\frac{1}{n+1},1)\in X-\{(0,1)\}$, so $(0,1)$ is a [[Limit Point]] of $X-\{0,1\}$. Therefore, $X-\{(0,1)\}\subseteq X\subseteq \text{cl }X$, so $X$ is [[Connected]] by the [[Closure of Connected Sets Proposition]].
>
Suppose there was a [[Continuous]] [[Function]] $f:[0,1]\rightarrow X$ with $f(0)=(0,1)$ and $f(1)=(1,0)$. Then, $f([0,1])$ is [[Connected]] by the [[Intermediate Value Theorem]]. But $f([0,1])$ may be covered by two [[Disjoint]] [[Open Set]] [[Subset]]s of $\mathbb{R}^{2}$: 
![[IMG_1305.jpg|400]]
So, $U\cap f([0,1])$ and $V\cap f([0,1])$ are relatively [[Open Set]] [[Subset]]s of $f([0,1])$. But this implies $f([0,1])$ is not [[Connected]], contradicting the assumption that there is a [[Path]] from $(0,1)$ to $(1,0)$.
