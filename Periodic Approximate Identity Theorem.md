---
mathLink: PAI theorem
---
>[!thm]
Let $\phi_{n}$ be a $\mathcal{C}^k$-[[Periodic Approximate Identity]] for some $k\in\mathbb{N}_{0}\cup\{\infty\}$. Then, for each $f\in\mathcal{C_1}(\mathbb{R};\mathbb{C})$, one has $$\int_\frac{-1}{2}^{\frac{1}{2}}f(s)\phi_{n}(t-s)\ ds\rightarrow f(t),\text{uniformly in }t\in \mathbb{R}\text{ as }n \rightarrow \infty$$
or in terms of [[Convolution]]s, $$f\star \phi_{n}\rightarrow f,\text{uniformly as }n\rightarrow \infty$$

>[!proof]

Let $\epsilon>0$. Since $f$ is [[Uniform Continuity]], pick $\delta$ such that for all $t_{1},t_2$ with $$|t_{1}-t_{2}|<\delta$$then, $$|f(t_1)-f(t_2)|<\epsilon$$
By [[PAI-3]], there exists $N$ such that for all $n\ge N$, $$\int_{[\frac{-1}{2},\frac{1}{2}]-(-\delta,\delta)} |\phi_{n}(t)|\ dt<\epsilon$$

First equality due to [[PAI-1]] and [[Convolution]]s are commutative

$C_{1}$ is a constant bounding $f$ ($f$ is bounded by [[Extreme Value Theorem]])

$C$ is the constant given in [[PAI-2]].

For $n\ge N$ and any $t$, 
$$\begin{align*}
|[f\star \phi_{n}](t)-f(t)|&= \left|\int_{\frac{-1}{2}}^{\frac{1}{2}}\phi_{n}(s)f(t-s)\ dt-f(t)\int_\frac{-1}{2}^{\frac{1}{2}}\phi_{n}(s)ds\right|\\
&= \left|\int_\frac{-1}{2}^{\frac{1}{2}}\phi_{n}(s)\cdot[f(t-s)-f(t)]\ ds\right|\\
&= \left|\int_{-\delta}^{\delta}\phi(s)\cdot[f(t-s)-f(t)]\ ds+\int_{[\frac{-1}{2},\frac{1}{2}]-(-\delta,\delta)}\phi_{n}(s)\cdot[f(t-s)-f(t)]\ ds\right|\\
&\lt \int_{-\delta}^{\delta}\left|\phi_{n}(s)\cdot[f(t-s)-f(t)]\ ds\right|+\int_{[\frac{-1}{2},\frac{1}{2}]-(-\delta,\delta)} \left|\phi_{n}(s)\cdot[f(t-s)-f(t)]\right|ds\\
&\le \epsilon\int_{-\delta}^{\delta}|\phi_{n}(s)|\ ds+ 2C_{1}\int_{[\frac{-1}{2},\frac{1}{2}]-(-\delta,\delta)}\left|\phi_{n}(s)\right|\ ds\\
&< 2C_{1}\epsilon+\epsilon\cdot\int_\frac{-1}{2}^{\frac{1}{2}}|\phi_{n}(s)|\ ds\\
&< 2C_{1}\cdot \epsilon+\epsilon C
\end{align*}$$
