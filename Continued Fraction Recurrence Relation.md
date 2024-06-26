---
mathLink: continued fraction recurrence relation
---
>[!prop]
Let $[a_{0};a_{1},\ldots,a_{n}]$ be a [[Continued Fraction]] of length $n\ge2$. Then, the segments $[a_{0};a_{1},\ldots,a_{k}]= \frac{p_{k}}{q_{k}}$ satisfy the two-point recursive relations $$\begin{align*}
p_{k}&= a_{k}p_{k-1}+p_{k-2},\\
q_{k}&= a_{k}q_{k-1}+q_{k-2},
\end{align*}$$for all $2\le k\le n$.

>[!note]
>We extend to $k=1$ by defining $$p_{-1}:=1,q_{-1}:=0$$

>[!note]
>We have that $$p_{0}=a_{0},q_{0}=1$$

>[!prop] Corollary
Let $[a_{0};a_{1},\ldots,a_{n}]$ be a [[Continued Fraction]] of length $n\in \mathbb{N}_{0}$. For $k\ge1$, we have $$\begin{align*}
q_{k}p_{k-1}-q_{k-1}p_{k}=(-1)^{k},\\
q_{k}p_{k-2}-p_{k}q_{k-2}=(-1)^{k-1}a_{k}
\end{align*}$$In particular, if for all $1\le k\le n$, $a_{0}\in\mathbb{Z}$ and $a_{k}\in \mathbb{N}$, then the representation of the [[Continued Fraction Approximant]]s as fractions $\frac{p_{k}}{q_{k}}$ based on the initial choices above is always in reduced form: $$\gcd(p_{k},q_{k})=1,\text{ for all }0≤k≤n$$

>[!prop] Corrolary
We also have $$\frac{p_{2n+1}}{q_{2n+1}}\text{ is monotonically decreasing}$$and $$\frac{p_{2n}}{q_{2n}}\text{ is monotonically increaseing}$$


The first corrolary gives 
$$\left| \frac{p_{n-1}}{q_{n-1}}- \frac{p_{n}}{q_{n}} \right|= \frac{1}{q_{n}q_{n-1}}$$
$$\begin{align*}
\left| \frac{p_{n}}{q_{n}}-\alpha\right|&\le \left| \frac{p_{n}}{q_{n}}- \frac{p_{n+1}}{q_{n+1}}\right|\\
&= \frac{1}{q_{n}q_{n+1}}\\
&\le \frac{1}{q_{n}^{2}}\\
\implies |\alpha q_{n}-p_{n}|&\le \frac{1}{q_{n+1}}
\end{align*}$$
So, an approximant is particularly good, when the next denominator is much bigger. 