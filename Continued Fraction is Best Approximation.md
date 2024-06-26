---
mathLink: continued fraction is BA-2 theorem
---
>[!thm]
Given $\alpha\in\mathbb{R}-\mathbb{Q}$, for $n\in \mathbb{N}_{0}$, let $\alpha_{n}= \frac{p_{n}}{q_{n}}$, $\gcd(p_{n},q_{n})=1$, be the $n$-th [[Continued Fraction Approximant]] of $\alpha$. Then,
>1. The [[Sequence]] of denominators $q_{n}$ increases strictly with $q \rightarrow \infty$ and for each $n\in \mathbb{N}_{0}$,one has $$|\alpha_{n}-\alpha|\le \frac{1}{q_{n}q_{n+1}}$$in particular, $\alpha_{n}\rightarrow \alpha$.
>2. A fraction $\frac{p}{q}$ is [[BA-2]] [[iff]] it is one of the [[Continued Fraction Approximant]]s $\alpha_{n}$ for some $n\in \mathbb{N}_{0}$.

Also, an integer $q$ is a [[Approximate Return Time]] [[iff]] $\frac{p}{q}$ is one of the [[Continued Fraction Approximant]]s $\alpha_{n}$ for some $p,n\in \mathbb{N}_{0}$.

>[!proof] Proof of (2 $\implies$)

Suppose $\frac{p}{q}$ is [[BA-2]]. We will show that $\frac{p}{q}$ is one of the [[Continued Fraction Approximant]]s with an argument by contradiction.

Suppose $\frac{p}{q}$ is not a [[Continued Fraction Approximant]]. There are three cases to consider.

**(1)** $\frac{p}{q}< \frac{p_{0}}{q_{0}}$

Note that $q_{0}=1$ and $p_{0}=a_{0}$
$$\begin{align*}
	\left| \frac{p}{q}-\alpha\right|&> \left| \frac{p_{0}}{q_{0}}-\alpha\right|\\
&= \left|a_{0}-\alpha\right|
\end{align*}$$
We also have $\frac{p}{q}$ is [[BA-2]], so $$\left|q \alpha-p\right|\le \left| \alpha\cdot 1-a_{0}\right|< \left|\alpha- \frac{p}{q}\right|\le q \left|\alpha- \frac{p}{q}\right|=|\alpha q-p|$$
which is a contradiction.

**(2)** $\frac{p_{n+1}}{q_{n+1}}>\frac{p}{q}> \frac{p_{n-1}}{q_{n-1}}$ since all of the odds are above $\alpha$ (We suppose $n$ is odd WLOG)

$$\begin{align*}
\left| \frac{p}{q}- \frac{p_{n-1}}{q_{n-1}}\right|&= \frac{\overbrace{|pq_{n-1}-qp_{n-1}|}^{\in \mathbb{N}}}{q\cdot q_{n-1}}\ge \frac{1}{qq_{n-1}}
\end{align*}$$
$$\begin{align*}
\left| \frac{p}{q}- \frac{p_{n-1}}{q_{n-1}}\right|&\le \left| \frac{p_{n-1}}{q_{n-1}}- \frac{p_{n}}{q_{n}}\right|\\
&= \frac{1}{q_{n-1}q_{n}}\\
\implies \frac{1}{q_{n-1}q_{n}}&\ge \frac{1}{qq_{n-1}}\implies q_{n}≤q
\end{align*}$$
And 
$$\begin{align*}
\left|\alpha- \frac{p}{q}\right|&\ge \left| \frac{p}{q}- \frac{p_{n+1}}{q_{n+1}}\right|\\
&= \frac{\overbrace{\left| pq_{n+1}-qp_{n+1}\right|}^{\in \mathbb{N}}}{qq_{n+1}}\\
&\ge \frac{1}{qq_{n+1}}\\
\implies \frac{1}{q_{n+1}}&\le |\alpha q-p|\\
&≤ |\alpha q_{n}-p_{n}|\\
&< \frac{1}{q_{n+1}}
\end{align*}$$
which is a contradiction.

**(3)** $\frac{p}{q}> \frac{p_{0}}{q_{0}}$

This is very similar to case 1