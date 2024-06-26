---
mathLink: equidistribution theorem
---
>[!thm]
>1. Given $\alpha\in \mathbb{R}-\mathbb{Q}$, let $R_\alpha$ be the associated [[Rotation Map]]. For an arbitrary, fixed interval $I\subseteq[0,1)$, let $$\mathcal{N}_{n}(x;I):=\#\{k\in\{0,\ldots,n-1\}|R_{\alpha}^{k}(x)\in I\}$$Then, $$\frac{\mathcal{N}_{n}(x;I)}{n}\rightarrow |I|$$uniformly, as $n \rightarrow \infty$.
>2. Fix $\alpha\in \mathbb{R}-\mathbb{Q}$ and let $f\in\mathcal{R}_{1}(\mathbb{R};\mathbb{C})$ be arbitrary. The, we have the values of $f$ evaluated along the $\alpha-$[[Finite Rotational Orbit]]s [[Converge in Cesaro Mean]] uniformly in $x$ with $$\frac{1}{n}\sum_{k=0}^{n-1}f(x+k \alpha)\rightarrow \int_{0}^{1}f(t)\ dt=\hat f_{0}$$as $n \rightarrow \infty$.

>[!proof] Proof (1)
We will formulate (1) as a special case of (2). Let $$\chi_{I}(x)=\begin{cases}1,\text{if }x\in I \\
0,\text{if }x\notin I\end{cases}$$extended periodically. We may write: $$\frac{1}{n}\mathcal{N}_{n}(x,I)= \frac{1}{n}\sum_{n=0}^{n-1}\chi_{I}(x+k \alpha)$$and $$|I|=\int_{0}^{1}\chi_{I}(x)\ dx=\widehat{[x_{I}]}_{0}$$

>[!proof] Proof (2) for [[Continuous]] [[Function]]s

We are estimating $$\left| \frac{1}{n}\sum_{k=0}^{n-1}f(x+k \alpha)-\hat f_{0}\right|=\left| \frac{1}{n}\sum_{k=0}^{n-1}(f(x+k \alpha)-\hat f_{0})\right|$$

This proof uses a cohomological equation: Does there exist a [[Function]] $h\in \mathcal{C}_{1}(\mathbb{R};\mathbb{C})$ such that  $$f(x)-\hat f_{0}=h(x+ \alpha)-h(x)$$holds for all $x\in[0,1)$.

If this is true, we have $$\begin{align}\left| \frac{1}{n}\sum_{k=0}^{n-1}(f(x+k \alpha)-\hat f_{0})\right|=\left| \frac{1}{n}\sum_{k=0}^{n-1}(h(x+(k+1)\alpha)-h(x+k \alpha)\right|=\left| \frac{1}{n}(h(x+n \alpha)+h(x))\right|\\
\le \frac{2}{n}\|h\|_{\infty}\end{align}$$which gives the rate of convergence.

Solve the cohomological equation:
Suppose we have a solution and compute the [[Fourier Coefficient]]s of both sides:

LHS:
$$\begin{align*}
\int_{0}^{1}(f(x)-\hat f_{0})e^{-2\pi in x}\ dx&= \hat f_{n}-\hat f_{0}\cdot\delta_{n,0}
\end{align*}$$
RHS: $$\begin{align*}
\int_{0}^{1}(h(x+\alpha)-h(x))e^{-2\pi inx}\ dx&= \int_{0}^{1}h(x+\alpha)e^{-2\pi inx}\ dx-\hat h_{n}\\
&= \int_{\alpha}^{1+\alpha}h(u)e^{-2\pi in(u-\alpha)}du\quad(\text{change variables }u=x+\alpha)\\
&= e^{-2\pi in \alpha}\int_{0}^{1}h(u)e^{-2\pi inu}du\\
&= e^{-2\pi in \alpha}\cdot\hat h_{n}
\end{align*}$$
So, $$\hat h_{n}(e^{2\pi in \alpha}-1)=\hat f_{n}+\hat f_{0}\cdot \delta_{n,0}$$giving, $$\hat h_{n}:=\begin{cases} \frac{\hat f_{n}}{e^{2\pi in \alpha}-1} & \text{ if }n≠0\\
\text{const} & \text{ if }n=0
\end{cases}$$
Is $\hat h_{n}$ a [[Sequence]] of [[Fourier Coefficient]]s for some [[Function]] $h\in\mathcal{C}_{1}(\mathbb{R};\mathbb{C})$? 

Note that
$$\sum_{n=-\infty}^{\infty}\left|\hat h_{n}\right|<\infty\implies h\in\mathcal{C}_{1}$$
since $$\sum_{n=-\infty}^{\infty}\hat h_{n}e^{-2\pi inx}\le\sum_{n=-\infty }^{\infty}\left|\hat h_{n}\right|$$so the [[Weierstrass M-test]] implies $\sum_{n=-\infty}^{\infty}\hat h_{n}e^{-2\pi inx}$ [[Uniform Convergence]]. Therefore, it [[Converges (series)]]s to a [[Continuous]] [[Function]] $h\in \mathcal{C}_{1}$ by the [[Sequence Convergence and Uniformly Convergent Functions]]. 

$e^{2\pi in \alpha}-1≠0$ for all $n≠0$, but it gets really close, since irrational orbits are [[Dense]]. This is the [[Small Divisor Problem]]: $$\sum_{n≠0} \frac{|\hat f_{n}|}{|e^{2\pi in \alpha}-1|}$$does not converge in general. But, it will for all [[Trigonometric Polynomial]]s, $f\in \mathcal{T}$. So, we have proven (2) for all [[Trigonometric Polynomial]]s.


We extend using density. Let $f\in \mathcal{C}_{1}$ be arbitrary. By the [[Weierstrass Approximation Theorem for Periodic Functions]]. Take a $p\in\mathcal{T}$ such that $\|f-p\|_{\infty}<\epsilon$. $$
\begin{align*}\left| \frac{1}{n}\sum_{j=0}^{n-1}f(x+j \alpha)-\hat f_{0}\right|&\le  \frac{1}{n}\sum_{j=0}^{n-1}\underbrace{|f(x+j \alpha)-p(x+j \alpha)|}_{\le\|f-p\|_{\infty}<\epsilon}+\\&\underbrace{\left| \frac{1}{n}\sum_{j=0}^{n-1}p(x+j \alpha)-\hat p_{0}\right|}_{\rightarrow 0,\text{uniformly in }x}+\underbrace{|\hat p_{0}-\hat f_{0}|}_{\le \|p-f\|_{\infty}<\epsilon}
\end{align*}$$
---
More on the small divisor problem:

There are irrational $\alpha$ such that $$|e^{2\pi in \alpha}-1|\ge \frac{\kappa}{|n|^{r}}$$for all $n\ne0$. We say that $\alpha$ is $r$-[[Diophantine]]. For $r>1$, $r$-[[Diophantine]] are generic

If we restrict $\alpha$ to be $r$-[[Diophantine]] and $f$ to $\mathcal{C}^{k}_{1}$, and use the [[Fourier Differentiation Mantra]], $$|\hat f_{n}|\le \frac{C}{|n|^{k}}$$
we can compute $$\begin{align*}
\sum_{n\ne0}\left|\hat h_{n}\right|&\le C\kappa\sum_{n=-\infty}^{\infty} \frac{1}{|n|^{k-r}}<\infty
\end{align*}$$whenever, $k-r>1$ [[iff]] $k>1+r$.


