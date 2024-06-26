
Inversion Property: 
$$S_{n}[f]\rightarrow? f$$point-wise or uniform

Set 2: 
For $f\in\mathcal{C}_{1}^{k}(\mathbb{R};\mathbb{C})$, $$|\widehat{f^{(k)}}_n|= (2\pi in)^{k}\hat{f}_{n}$$Therefore, $$\begin{align*}\\
|\hat{f}_{n}|&\le  \frac{|\widehat{f^{(k)}}_{n}|}{2\pi|n|^{k}}\\
&\le \frac{\|f^(k)\|_{\infty}}{2\pi}|n|^{-k}
\end{align*}$$For $k=2$, apply the [[Weierstrass M-test]]: 
$$\sum_{n\in \mathbb{Z}}\left|\hat{f}_{n}e^{2\pi int}\right|=\sum_{n\in \mathbb{Z}}|\hat{f}_{n}|\le\sum_{n\in \mathbb{Z}} \frac{C}{|n|^{2}}=|\hat{f_{0}}|+2C\sum_{n=1}^{\infty} \frac{1}{n^{2}}<+\infty$$So, $S_{n}[f]$ converges uniformly, so we can write $$\lim_{n\rightarrow \infty}S_{n}[f]$$We have that $C_{n}[f]\rightarrow f$ by [[Fejér's Theorem]]. Using the [[Converge in Cesaro Mean]], $$\lim S_{n}[f]=\lim C_{n}[f]=f$$
So, $S_{n}[f]\rightarrow f$ uniformly
