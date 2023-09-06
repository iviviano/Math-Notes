From 1.2: 7, 10

>[!note] 7
(a) Doesn't seem possible. I think this might let there be more than one point in the [[Intersection]], but I don't see how this lets the [[Intersection]] be empty.
(b) Let $F_{n}=\{n\}$ for $n\in \mathbb{N}$. Then, for each $n$, $F_{n}$ is [[Closed Set]] as $F_{n}$ is finite and finite sets in [[Metric Space]]s are [[Closed Set]] by [[9-7 Problems]]. For each $n$, $\text{diam }F_{n}=0$, so $\text{diam }F_{n}\rightarrow 0$. However, $$\bigcap_{n=1}^{\infty}F_{n}=\emptyset$$
(c) Let $F_{n}=(0,\frac{1}{n})$. Then, for each $n$, $F_{n+1}\subseteq F_{n}$. $\text{diam }F_{n}\rightarrow 0$, as given $\epsilon>0$, if $\frac{1}{n}<\epsilon$, then $d(x,y)<\epsilon$ for all $x,y\in(0,\frac{1}{n})$. However, $$\bigcap_{n=1}^{\infty}F_{n}=\emptyset$$Assume not: $x\in\bigcap F_{n}$. Then $x>0$ as $0\notin F_{1}$. Pick $n\in \mathbb{N}:\frac{1}{n}<x$. Then, $x\notin F_{n}$. [[therefore]] the [[Intersection]] is empty.

>[!note] 10 Let $(X,d)$ be the [[Cartesian Product]] of the two [[Metric Space]]s $(X_{1},d_{1})$ and $(X_{2},d_{2})$.
(a) Let $\epsilon>0$ be given. Assume that a [[Sequence]] $\{(x_{n}^{1},x_{n}^{2})\}$ is [[Cauchy Sequence]] in $X$. Then, pick $N\in \mathbb{N}$ such that if $m,n≥N$, $d((x_{n}^{1},x_{n}^{2}),(x_{m}^{1},x_{m}^{2}))<\epsilon$. As [[Metric]]s take on nonnegative values,
$$d((x_{1},y_{1}),(x_{2},y_{2}))=d_{1}(x_{1},x_{2})+d_{2}(y_{1},y_{2})≥d_{1}(x_{1},x_{2})$$
and 
$$d((x_{1},y_{1}),(x_{2},y_{2}))=d_{1}(x_{1},x_{2})+d_{2}(y_{1},y_{2})≥d_{2}(y_{1},y_{2})$$
So, if $m,n≥N$,
$$d_{1}(x_{n}^{1},x_{m}^{1})≤d((x_{n}^{1},x_{n}^2),(x_{m}^{1},x_{m}^{2}))<\epsilon$$
and $$d_{2}(x_{n}^{2},x_{m}^{2})≤d((x_{n}^{1},x_{n}^2),(x_{m}^{1},x_{m}^{2}))<\epsilon$$
so $x_{n}^{1}$ and $x_{n}^{2}$ are [[Cauchy Sequence]] in $X_{1}$ and $X_{2}$, respectively.
>
Assume $x_{n}^{1},x_{n}^{2}$ are [[Cauchy Sequence]] in $X_{1}$ and $X_{2}$, respectively. Pick $N_{1}\in \mathbb{N}$ such that if $n,m≥N_1$, then $d_{1}(x_{n}^{1}, x_{m}^{1})<\frac{\epsilon}{2}$. Pick $N_{2}\in \mathbb{N}$ such that if $n,m≥N_1$, then $d_{2}(x_{n}^{2}, x_{m}^{2})<\frac{\epsilon}{2}$. Let $N=\max\{N_{1},N_{2}\}$. Then, if $n,m≥N$, 
$$d((x_{n}^{1},x_{n}^{2}),(x_{m}^{1},x_{m}^{2}))=d_{1}(x_{n}^{1},x_{m}^{1})+d_{2}(x_{n}^{2},x_{m}^{2})<\frac{\epsilon}{2} + \frac{\epsilon}{2}=\epsilon$$
so, $\{(x_{n}^{1},x_{n}^{2})\}$ is [[Cauchy Sequence]] in $X$.
>
(b) Let $\epsilon>0$ be given. Suppose $X$ is [[Complete]]. Let $\{x_{1}\}\subseteq X_{1}$ and $\{x_{2}\}\subseteq X_{2}$ be [[Cauchy Sequence]] sequences. Then, $\{x_{n}^{1},x_{n}^{2}\}$ is [[Cauchy Sequence]] $X$ (by a). As $X$ is [[Complete]], the [[Sequence]] [[Converges]]s to $(x_{1},x_{2})\in X$. Pick $N\in \mathbb{N}$ such that if $n≥N$, $d((x_{1},x_{2}),(x_{n}^{1},x_{n}^{2}))<\epsilon$. Then for all $n≥N$,
$$d_{1}(x_{1},x_{n}^{1})≤d((x_{1},x_{2}),(x_{n}^{1},x_{n}^{2}))<\epsilon$$
and 
$$d_{2}(x_{2},x_{n}^{2})≤d((x_{1},x_{2}),(x_{n}^{1},x_{n}^{2}))<\epsilon$$
So, $x_{n}^{1}\rightarrow x_1$ and $x_{n}^{2}\rightarrow x_{2}$. [[therefore]] all [[Cauchy Sequence]] [[Sequence]]s in $X_{1}$ and $X_{2}$ [[Converges]], so $X_{1}$ and $X_{2}$ are [[Complete]]. 
>
Suppose $X_{1}$ and $X_{2}$ are [[Complete]]. Consider the [[Cauchy Sequence]] sequence $\{(x_{n}^{1},x_{n}^{2})\}$ in $X$. Then $\{x_{n}^{1}\}\subseteq X_{1}$ and $\{x_{n}^{2}\}\subseteq X_{2}$ are [[Cauchy Sequence]] sequences, so they [[Converges]] in the [[Complete]] [[Metric Space]]s. Let $x_{1}=\lim x_{n}^{1}$. Pick $N_{1}\in \mathbb{N}$ such that if $n≥N$, then $d_{1}(x_{1},x_{n})<\frac{\epsilon}{2}$. Let $x_{2}=\lim x_{n}^{2}$. Pick $N_{2}\in \mathbb{N}$ such that if $n≥N$, then $d_{1}(x_{2},x_{n})<\frac{\epsilon}{2}$. Let $N=\max\{N_{1},N_{2}\}$. Then, if $n≥N$, 
$$d((x_{1},x_{2}),(x_{n}^{1},x_{n}^{2}))=d_{1}(x_{1},x_{n}^{1})+d_{2}(x_{2},x_{n}^{2})<\frac{\epsilon}{2} +\frac{\epsilon}{2}=\epsilon$$
so $(x_{n}^{1},x_{n}^{2})\rightarrow(x_{1},x_{2})$. [[therefore]] all [[Cauchy Sequence]] [[Sequence]]s in $X$ [[Converges]], so $X$ is [[Complete]].

