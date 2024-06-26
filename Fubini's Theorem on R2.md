---
mathLink: Fubini's theorem on $\mathbb{R}^2$
---
>[!thm]
Let $f:\mathbb{R}^{2}\rightarrow \mathbb{C}$ be a [[Continuous]] [[Function]] such that $$
\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}|f(x,y)|\ dx\ dy<\infty
$$Then, the double integral $$
I=\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}f(x,y)\ dx\ dy
$$exists and it can be computed by iterated integrals for which the order of [[Integration]] does not matter: $$
I=\int_{-\infty}^{\infty}\left\{\int_{-\infty}^{\infty}f(x,y)\ dx\right\}\ dy=\int_{-\infty}^{\infty}\left\{\int_{-\infty}^{\infty}f(x,y)\ dy\right\}\ dx
$$
