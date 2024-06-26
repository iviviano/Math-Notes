---
mathLink: pointwise Fourier convergence proposition
---
>[!prop]
Let $f\in\mathcal{C}_{1}(\mathbb{R};\mathbb{C})$ be given. Suppose that for some for some point $t_{0}\in \mathbb{R}$, $$\lim_{n\rightarrow \infty}S_{n}[f](t_{0})$$exists, then, $$\sum_{n\in\mathbb{Z}}\hat{f}_{n}e_{n}(t_{0})=f(t_{0})$$
so if the [[Fourier Polynomial]]s [[Converges (series)]] to $f$ pointwise, $f$ equals its [[Fourier Series of a Function]]. 

>[!proof]
We have that $C_{n}[f]\rightarrow f$ by [[Fejér's Theorem]]. Using the [[Converge in Cesaro Mean]], $$\lim S_{n}[f](t_{0})=\lim C_{n}[f](t_{0})=f(t_{0})$$
So, $S_{n}[f](t_{0})\rightarrow f(t_{0})$
