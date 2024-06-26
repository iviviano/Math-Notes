From 1.5: 1, 3

>[!note] 1
>
Suppose $S$ is an interval. If $S$ is not [[Connected]], $S=S_{1}\cup S_{2}$ where $S_{1},S_{2}$ are [[Separated]]. If $S_{1}$ consisted only of endpoints of $S$, each would be a [[Limit Point]] of $S_{2}$. Thus $S_{1},S_{2}$ [[Intersects]] the [[Interior]] of $S$. Let $\alpha\in S_{1},\beta\in S_{2}$ be [[Interior]] points of $S$. Since $\alpha≠\beta$, assume $\alpha<\beta$. Let $\gamma=\sup\{S_{1}\cap[\alpha,\beta]\}$, so $\alpha≤\gamma≤\beta$. If $\gamma\in S_{1}$ then $\gamma<\beta$ and $(\gamma,\beta]\subseteq S_{2}$. But this implies that $\gamma$ is a [[Limit Point]] of $S_{2}$. Suppose that $\gamma\in S_{2}$. For $n\in \mathbb{N}$, $\gamma - \frac{1}{n}$ is not an upper bound for $S_{1}\cap[\alpha,\beta]$, so there exist $x_{n}\in S_{1}\cap[\alpha,\beta]$ satisfuing $\gamma- \frac{1}{n}<x_{n}<\gamma$. Then $x_{n}\rightarrow \gamma$ so $\gamma\in S_{2}$ is a [[Limit Point]] of $S_{1}$. So, $\gamma\notin S_{1}\cup S_{2}=S$. But as $\alpha,\beta\in S$ and $\alpha<\gamma<\beta$, contradicting the fact that $S$ is an interval.


>[!note] 3
Note: $f(X)\subseteq\{1,-1\}$. Suppose that $f$ is not constant. Then, there exist $x,y\in X$ such that $f(x)≠f(y)$. Without loss of generality, assume that $f(x)=1$ and $f(y)=-1$. Then, $f(X)=\{1,-1\}$. But, $f(X)$ is not [[Connected]] as [[Intervals are Connected in R]]. As $X$ is [[Connected]], this contradicts the fact that $f$ is [[Continuous]], as stated by the [[Intermediate Value Theorem]]. So, $f$ must be constant.