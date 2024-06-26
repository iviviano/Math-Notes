---
mathLink: Parseval identity
---
>[!thm]
For $f,g\in \mathcal{S}(\mathbb{R};\mathbb{C})$, 
$$\int_{-\infty}^{\infty}f(x)\widehat g(x)\ dx=\int_{-\infty}^{\infty}\widehat f(x) g(x)\ dx$$

>[!proof]
We apply [[Fubini's Theorem on R2]]:$$\begin{align*}
\int_{-\infty}^{\infty}f(x)\widehat g(x)\ dx&= \int_{-\infty}^{\infty}f(x) \left[\int_{-\infty}^{\infty}g(t)e^{-2\pi itx}\ dt\right]\ dx\\
&=^{\text{Fubini}}\int_{-\infty}^{\infty} \left[\int_{-\infty}^{\infty}f(x)e^{-2\pi i tx}\ dx\right]\cdot g(t)\ dt \\
&= \int_{-\infty}^{\infty}\widehat f(t)\cdot g(t)\ dt
\end{align*}$$


>[!prop] Corollary (Continuum analogue of [[Plancherel's Identity]])
$$\|f\|_{\mathcal{L}^{2}(dt)}^{2}=\int_{-\infty}^{\infty}|f(t)|^{2}\ dt= \int_{-\infty}^{\infty}\left|\widehat f(\nu)\right|^{2}\ d \nu=\left\|\widehat f\right\|_{\mathcal{L}^{2}(d \nu)}^{2}$$

>[!note]
This [[Norm]]-preserving property is called [[Isometry]]. In particular, the [[Fourier Map]] is an [[Isometry]] on $\mathcal{S}(\mathbb{R};\mathbb{C})$

>[!proof]

Let $g(x)=\overline{\widehat{f}(x)}$.
$$\widehat g(x)=\int_{-\infty}^{\infty}\overline{\widehat f(t)}e^{-2\pi i t x}\ dt=\overline{\int_{-\infty}^{\infty}\widehat{f}(t)e^{2\pi i tx}\ dt}=\overline{f(x)}$$
where the last equality is the [[Fourier Inversion Property]]. Then,
$$\begin{align*}
\int_{-\infty}^{\infty}|f(t)|^{2}\ dt&= \int_{-\infty}^{\infty}f(t)\cdot\overline{f(t)}\ dt\\
&= \int_{-\infty}^{\infty}f(t)\cdot\widehat g(t)\ dt\\
&= \int_{-\infty}^{\infty}\widehat{f}(t)\cdot g(t)\ dt\\
&= \int_{-\infty}^{\infty}\widehat f(t)\cdot\overline{\widehat f(t)}\ dt\\
&= \int_{-\infty}^{\infty}\left|\widehat f(t)\right|^{2}\ dt
\end{align*}$$
