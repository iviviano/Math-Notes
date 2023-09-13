From 1.2: 7, 10

This problem uses the following theorem which I don't believe is in the book.
>[!thm]
Let $\{x_{n}\}$ be a [[Bounded Metric Space]] [[Sequence]] of real numbers. 
>1. If for all $n$, $x_{n}≥x_{n+1}$, then $\lim x_{n}=\inf\{x_{n}\}$
>2. If for all $n$, $x_{n}≤x_{n+1}$, then $\lim x_{n}=\sup\{x_{n}\}$

>[!proof]
(1) As $\{x_{n}\}$ is a [[Bounded Metric Space]] [[Set]] and $x_{1}\in\{x_{n}\}$, $x=\inf\{x_{n}\}\in \mathbb{R}$ as $\mathbb{R}$ is [[Complete]]. Suppose $x_{n}\not\rightarrow x$. Pick $\epsilon>0$ such that for all $N\in \mathbb{N}$, there exists $n≥N$ such that $|x_{n}-x|≥\epsilon$. Then, $x_{n}≥x+\epsilon>x$, so $x$ is not the [[infinum]] of $\{x_{n}\}$ as it is not the greatest lower bound. By contradiction, $x_{n}\rightarrow x$.

>[!note] 7
(a) Let $F_{n}=\{m\in \mathbb{N}:m≥n\}$. 
(i) For each $n$, $F_{n}$ is [[Closed Set]] as it is a [[Collection]] of [[Isolated Point]]s which is [[Closed Set]] by [[9-7 Problems]]. 
(ii) Let $m\in F_{n+1}$. Then, $m≥n+1≥n$ so $m\in F_{n}$. [[therefore]]$F_{n+1}\subseteq F_{n}$ for all $n\in \mathbb{N}$. 
Suppose $x\in\bigcap F_{n}$. Then, pick $n\in \mathbb{N}$ such that $n>x$. Then, $x\notin F_{n}$. By contradiction, $\bigcap F_{n}=\emptyset$.
>
(b) Let $F_{n}=\{n\}$ for $n\in \mathbb{N}$. 
(i) Then, for each $n$, $F_{n}$ is [[Closed Set]] as $F_{n}$ is finite and finite sets in [[Metric Space]]s are [[Closed Set]] by [[9-7 Problems]]. 
(ii) For each $n$, $\text{diam }F_{n}=0$, so $\text{diam }F_{n}\rightarrow 0$. 
However, $$\bigcap_{n=1}^{\infty}F_{n}=\emptyset$$
>
(c) Let $F_{n}=(0,\frac{1}{n})$. 
(i) For each $n$, $F_{n+1}\subseteq F_{n}$. Let $x\in(0,\frac{1}{n+1})$. Then $0<x<\frac{1}{n+1} <\frac{1}{n}$, so $x\in F_{n}$.
(ii) $\text{diam }F_{n}\rightarrow 0$, as given $\epsilon>0$, if $\frac{1}{n}<\epsilon$, then $d(x,y)<\epsilon$ for all $x,y\in(0,\frac{1}{n})$. 
However, $$\bigcap_{n=1}^{\infty}F_{n}=\emptyset$$Assume not: $x\in\bigcap F_{n}$. Then $x>0$ as $0\notin F_{1}$. Pick $n\in \mathbb{N}:\frac{1}{n}<x$. Then, $x\notin F_{n}$. [[therefore]] the [[Intersection]] is empty.
>
(d) The [[Supremum]] of a [[Set]] is the [[Limit of a Sequence]] of a possibly non-unique [[Sequence]] in that set as there must be at least one element arbitrarily close to the supremum, so [[Closed Set]] sets in a [[Complete]] space like $\mathbb{R}$ contain their [[Supremum]]s (if they exist).
>
Let $x_{n}=\sup(F_{n})$. $\{x_{n}\}$ is bounded below by $\inf(F_{1})$. As $F_{n}$ is [[Closed Set]], it contains its [[Supremum]] by the [[Characterizations of Compactness]]. Additionally, $x_{n}≥x_{n}+1$ as $F_{n}\supseteq F_{n+1}$ (VERIFY). So $x_{n}\rightarrow x\in X$ by [[Monotone Convergence Theorem]]. 
>
For each $k$, the [[Subsequence]] $\{x_{n}\}_{n=k}^{\infty}\subseteq F_{k}$. So, $F_{n}$ contains $x$ as [[Closed Sets in Metric Spaces contain Sequence Limits]] and [[Subsequences of Convergent Sequences Converge]] to the same [[Limit of a Sequence]]. [[therefore]] $x\in F_{n}$ for all $n$, so $x\in\bigcup F_{n}$.

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
(b) Let $\epsilon>0$ be given. Suppose $X$ is [[Complete]]. Let $\{x_{1}\}\subseteq X_{1}$ and $\{x_{2}\}\subseteq X_{2}$ be [[Cauchy Sequence]] sequences. Then, $\{x_{n}^{1},x_{n}^{2}\}$ is [[Cauchy Sequence]] $X$ (by a). As $X$ is [[Complete]], the [[Sequence]] [[Converges (Sequence)]]s to $(x_{1},x_{2})\in X$. Pick $N\in \mathbb{N}$ such that if $n≥N$, $d((x_{1},x_{2}),(x_{n}^{1},x_{n}^{2}))<\epsilon$. Then for all $n≥N$,
$$d_{1}(x_{1},x_{n}^{1})≤d((x_{1},x_{2}),(x_{n}^{1},x_{n}^{2}))<\epsilon$$
and 
$$d_{2}(x_{2},x_{n}^{2})≤d((x_{1},x_{2}),(x_{n}^{1},x_{n}^{2}))<\epsilon$$
So, $x_{n}^{1}\rightarrow x_1$ and $x_{n}^{2}\rightarrow x_{2}$. [[therefore]] all [[Cauchy Sequence]] [[Sequence]]s in $X_{1}$ and $X_{2}$ [[Converges (Sequence)]], so $X_{1}$ and $X_{2}$ are [[Complete]]. 
>
Suppose $X_{1}$ and $X_{2}$ are [[Complete]]. Consider the [[Cauchy Sequence]] sequence $\{(x_{n}^{1},x_{n}^{2})\}$ in $X$. Then $\{x_{n}^{1}\}\subseteq X_{1}$ and $\{x_{n}^{2}\}\subseteq X_{2}$ are [[Cauchy Sequence]] sequences, so they [[Converges (Sequence)]] in the [[Complete]] [[Metric Space]]s. Let $x_{1}=\lim x_{n}^{1}$. Pick $N_{1}\in \mathbb{N}$ such that if $n≥N$, then $d_{1}(x_{1},x_{n})<\frac{\epsilon}{2}$. Let $x_{2}=\lim x_{n}^{2}$. Pick $N_{2}\in \mathbb{N}$ such that if $n≥N$, then $d_{1}(x_{2},x_{n})<\frac{\epsilon}{2}$. Let $N=\max\{N_{1},N_{2}\}$. Then, if $n≥N$, 
$$d((x_{1},x_{2}),(x_{n}^{1},x_{n}^{2}))=d_{1}(x_{1},x_{n}^{1})+d_{2}(x_{2},x_{n}^{2})<\frac{\epsilon}{2} +\frac{\epsilon}{2}=\epsilon$$
so $(x_{n}^{1},x_{n}^{2})\rightarrow(x_{1},x_{2})$. [[therefore]] all [[Cauchy Sequence]] [[Sequence]]s in $X$ [[Converges (Sequence)]], so $X$ is [[Complete]].

