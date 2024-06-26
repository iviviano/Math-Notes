---
mathLink: $L^2$ inversion property
---
>[!thm]
>For all [[Function]]s $f\in\mathcal{R}_{T}(\mathbb{R};\mathbb{C})$, the [[Fourier Polynomial]]s [[Converges (Sequence)]] in the [[L2 Inner Product]][[Norm]]: $$\frac{1}{T}\int_{0}^{T}\left|S_{n}[f](t)-f(t)\right|^{2}\ dt \rightarrow 0,\text{ as }n \rightarrow \infty$$

>[!proof] Proof for [[Continuous]] [[Function]]s:

From [[3-8]], this is equivalent to [[Plancherel's Identity]] (for [[Continuous]] [[Function]]s): $$\|f\|_{2}^{2}=\int_{0}^{1}|f(t)|\ dt=\sum_{n=-\infty}^{\infty}\left|\hat f_{n}\right|$$
Start by showing this for [[Trigonometric Polynomial]]s: $$f=\sum_{|k|≤M}\hat f_{k}e_{k}$$
$$\begin{align*}
\|f\|_{2}^{2}&= \langle f,f\rangle\\
&= \langle\sum_{|k|≤M}\hat f_{k}e_{k},\sum_{|m|≤M}\hat f_{m}e_{m}\rangle\\
&= \sum_{|m|≤M}\langle\sum_{|k|≤M}\hat f_{k}e_{k},\hat f_{m}e_{m}\rangle\\
&= \sum_{|m|≤M}\sum_{|k|≤M}\langle\hat f_{k}e_{k},\hat f_{m}e_{m}\rangle\\
&= \sum_{|m|≤M}\sum_{|k|≤M}\int_{0}^{1}\overline{\hat f_{k}(t)e_{k}(t)}\hat f_{m}(t)e_{m}(t)\ dt\\
&= \sum_{|m|≤M}\sum_{|k|≤M}\overline{\hat f_{k}}\hat f_{m}\cdot\int_{0}^{1}\overline {e_{k}(t)}e_{m}(t)\ dt\\
&= \sum_{|m|≤M}\sum_{|k|≤M}\overline{\hat f_{k}}\hat f_{m}\cdot \delta_{k,m}\ dt\\
&= \sum_{|m|≤M}\overline{\hat f_{m}}\hat f_{m}\ dt\\
&= \sum_{|m|≤M}|\hat f_{m}|^{2}\\
&= \sum_{m=-\infty}^{\infty}|\hat f_{m}|^{2}
\end{align*}$$
Extend to all [[Continuous]] [[Function]]s $f$. We have the [[Fejer Kernel]]$$C_{n}[f]=\sum_{|k|≤n}\left(1-\frac{|k|}{n}\right)\hat f_{k}e_{k}\rightarrow f,\text{ uniformly}$$We have $$\sum_{n=-\infty}^{\infty}\left|\hat f_{n}\right|^{2}\le\|f\|_{2}^{2}$$So, we must show $$\sum_{n=-\infty}^{\infty}\left|\hat f_{n}\right|^{2}\ge\|f\|_{2}^{2}$$Let $f\in\mathcal{C}_{1}$ we know $$\begin{align*}\|C_{n}[f]\|_{2}&= \sum_{|k|≤n}\left(1- \frac{|k|}{n}\right)|\hat f_{k}|^{2}\\
&\le \sum_{|k|≤n}|f_{k}|^{2}\\
&\le \sum_{k=-\infty}^{\infty}|\hat f_{k}|^{2}<\infty
\end{align*}$$
>[!note]
$$\|g\|_{2}^{2}=\int_{0}^{1}|g(x)|^{2}\ dx\le \|g\|_{\infty}^{2}$$by the [[ML-Estimate]], so $$\|g\|_{2}≤\|g\|_{\infty}$$

Thus, 
$$\begin{align*}
|\|C_{n}[f]\|_{2}-\|f\|_{2}|&\le \|C_{n}[f]-f\|_{2}\quad(\text{left side of }\triangle \text{ inequality})\\
&\le \|C_{n}[f]-f\|_{\infty}\\
&\rightarrow 0
\end{align*}$$by [[Fejér's Theorem]]. Therefore, $$\|C_{n}[f]\|_{2}\rightarrow \|f\|_{2}\implies\|f\|^{2}\le \sum_{n=-\infty}^{\infty}|\hat f_{n}|^{2}$$

>[!note]
>There is a theorem (Carleson) that shows that the set of points for which the Fourier series does not converge pointwise is of [[Lebesgue Measure]] zero

