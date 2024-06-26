---
tag: topology
mathLink: countable products are metrizable
---
>[!thm]
If $(X_{n},d_{n})$ are [[Metric Space]]s for $n≥1$, and $X=\prod_{n=1}^{\infty}X_{n}$, then the [[Product Topology]] on $X$ is [[Metrizable]] and is defined by the [[Metric]] $$d(x,y)=\sum_{n=1}^{\infty} \frac{1}{2^{n}} \frac{d_{n}(x_{n},y_{n})}{1+d_{n}(x_{n},y_{n})}$$

>[!proof]
Let $\mathcal{T}$ be the [[Product Topology]] on $X$ and let $\mathcal{D}$ be the [[Metric Topology]] induced by $d$. If $G\in \mathcal{T}$, then for any $x\in G$, there are $n_{1}<\cdots<n_N$ and $\epsilon_{1},\ldots,\epsilon_N>0$ such that $$\bigcap_{k=1}^{N}\pi^{-1}_{n_{k}}(B_{d_{n_{k}}}(x_{n_{k}},\epsilon_{k}))\subseteq G$$Pick $\epsilon<1$ such that when $0<s<2^N$, then $s(1-s)^{-1}<\epsilon_{n_{i}}$ for each $n_{i}$. Then when $d(x,y)<\epsilon$, $$d_{n}(x_{n},y_{n})[1+d_{n}(x_{n},y_{n})]^{-1}<2^{n}\epsilon<2^{N}\epsilon$$for $n=1,\ldots,N$. By the choice of $\epsilon$, we have $d_{n}(x_{n},y_{n})<\epsilon_{n}$ (should verify this with $s$). This implies that $$y\in\bigcap_{k=1}^{N}\pi^{-1}_{n_{k}}(B_{d_{n_{k}}}(x_{n_{k}},\epsilon_{k}))\subseteq G$$so, $G\in \mathcal{D}$.
>
Let $G\in \mathcal{D}$, $x\in G$. Pick $\epsilon>0$ such that $B(x,\epsilon)\subseteq G$. Choose $N≥1$ such that $$\sum_{n=N+1}^{\infty}2^{-n}<\frac{\epsilon}{2}$$Let $\delta>0$ be such that when $0≤t<\delta$, then $t(1+t)^{-1}<\frac{\epsilon}{2}$. Thus, if $y\in X$ and $d_{n}(x_{n},y_{n})<\delta$ for all $n≤N$, then $$\sum_{n=1}^{N} \frac{1}{2^{n}}\frac{d_{n}}{1+d_{n}}<\sum_{n=1}^{N} \frac{1}{2^{n}} \frac{\epsilon}{2}<\frac{\epsilon}{2}$$so, $d(x,y)<\epsilon$. That is , $$\bigcap_{n=1}^{N}\pi^{-1}_{n}(B_{d_{n}}(x_{n},\delta))\subseteq B_{d}(x,\epsilon)$$
