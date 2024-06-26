---
mathLink: uncertainty principle
---
>[!thm]


$$w_{t}\cdot w_{\nu}\ge \frac{1}{4\pi}>0$$

Let $f\in\mathcal{S}(\mathbb{R};\mathbb{C})$ be normalized in the time domain. Then, [[Parseval Identity]]'s gives: $$\left\|\widehat f\right\|_{\mathcal{L}^{2}}=\|f\|_{\mathcal{L}^{2}}=1$$
We take $$\begin{align*}
\langle t\rangle&= \int_{-\infty}^{\infty}t|f(t)|^{2}\ dt\\
\langle \nu\rangle&= \int_{-\infty}^{\infty}\nu\left|\widehat f(t)\right|^{2}\ dt\\
\sigma_{t}^{2}=\langle (t-\langle t\rangle)^{2}\rangle&= \int_{-\infty}^{\infty}(t-\langle t\rangle)^{2}|f(t)|^{2}= \left\|(t-\langle t\rangle)f(t)\right\|_{\mathcal{L}^{2}}^{2}\\
\sigma_{\nu}^{2}=\langle (\nu-\langle \nu\rangle)^{2}\rangle&= \int_{-\infty}^{\infty}(\nu-\langle \nu\rangle)^{2}|f(\nu)|^{2}= \left\|(\nu-\langle \nu\rangle)f(\nu)\right\|_{\mathcal{L}^{2}}^{2}
\end{align*}$$

>[!prop] Lemma
$$\langle f',g\rangle_{\mathcal{L}^{2}}=-\langle f,g'\rangle_{\mathcal{L}^{2}}$$

This is easily proven with integration by parts.

>[!proof]

Reduce to case where $\langle t\rangle=\langle \nu\rangle=0$. We will show 
$$\underbrace{\|t\cdot f(t)\|_{\mathcal{L}^{2}(dt)}}_{=\sigma_{t}}\cdot\underbrace{\|\nu\cdot \widehat f(\nu)\|_{\mathcal{L}^{2}}}_{=\sigma_{\nu}}\ge \frac{1}{4\pi}$$
for all $f\in\mathcal{S}(\mathbb{R},\mathbb{C})$ with $$\|f\|_{\mathcal{L}^{2}}=1$$
The first equality uses the [[Fourier Differentiation Mantra]] and [[Plancherel's Identity]]. The second inequality is [[Cauchy-Schwartz Inequality]]. The third equality uses the [[Linearity in the Second Entry]].
$$\begin{align*}
\|t\cdot f(t)\|_{\mathcal{L}^{2}(dt)}\cdot\|\nu\cdot \widehat f(\nu)\|_{\mathcal{L}^{2}(\nu)}&= \|t\cdot f(t)\|_{\mathcal{L}^{2}(dt)}\cdot\| \frac{1}{2\pi i}\cdot \frac{df}{dt}(t)\|_{\mathcal{L}^{2}(dt)}\\
&\ge \left|\left\langle t\cdot f(t), \frac{1}{2\pi i} \frac{df}{dt}(t)\right\rangle_{\mathcal{L}^{2}}\right|\\
&= \frac{1}{2\pi}\left|\left\langle t\cdot f(t), f'(t)\right\rangle\right|\\
&\ge \frac{1}{2\pi}\left|\Re \text{e}\langle t\cdot f(t),f'(t)\rangle\right|\\
&= \frac{1}{2\pi}\cdot \frac{1}{2}\left|\text{e}\langle t\cdot f(t),f'(t)\rangle+\overline{\langle f(t)\cdot t,f'(t)\rangle}\right|\\
&= \frac{1}{2\pi}\cdot \frac{1}{2}\left|\text{e}\langle t\cdot f(t),f'(t)\rangle+\langle f'(t),t\cdot f(t)\rangle\right|\\
&\overset{\text{lemma}}{=}  \frac{1}{4\pi}\left|\langle f(t),t\cdot f'(t)\rangle-\langle f(t),f(t)+t\cdot f'(t)\rangle\right|\\
&= \frac{1}{4\pi}|\langle f(t),t\cdot f'(t)-f(t)-t\cdot f'(t)\rangle|\\
&= \frac{1}{4\pi}\left|\langle f(t), \left\{ t\cdot \frac{d}{dt}- \frac{d}{dt}\cdot t\right\} f(t)\rangle\right|\\
&= \frac{1}{4\pi}\left|\langle f(t), t\cdot f'(t)-f(t)-t\cdot f'(t)\rangle\right|\\
&= \frac{1}{4\pi}|\underbrace{\langle f,f\rangle_{\mathcal{L}^{2}}}_{=1}|\\
&= \frac{1}{4\pi}
\end{align*}$$
The step after lemma usage has as the second inner product entry the difference between differentiating then multiplying by $t$ and multiplying by $t$ then differentiating. Since these linear operators don't commute: $$
\left[t, \frac{d}{dt}\right]= -1\ne0
$$there is uncertainty.
