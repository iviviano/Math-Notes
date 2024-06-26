---
mathLink: Fourier transform bound
---
>[!thm]
>1. For $f\in\mathcal{L}^{1}$, the [[Fourier Transform]] is a [[Bounded Function into R]] and satisfies $$\left\|\widehat f\right\|_{\infty}\le\|f\|_{\mathcal{L}^{1}}$$
>2. If a [[Sequence]] of $(f_{n})_{n\in \mathbb{N}}$ of [[L1 Function]]s [[Converges (Sequence)]]s in the [[Script-L1 Norm]] sense to a [[Function]] $f\in\mathcal{L}^{1}$, then the [[Sequence]] of [[Fourier Transform]]s [[Uniform Convergence]] to $\widehat f$ with $$\left\|\widehat f_{n}-\widehat f\right\|_{\infty}\le\|f_{n}-f\|_{\mathcal{L}^{1}}\rightarrow 0,\text{ as }n\rightarrow \infty$$

>[!proof]

(1) $$\begin{align*}
\left|\widehat f(\nu)\right|&= \left|\int_{-\infty}^{\infty}f(t)~e^{-2\pi i \nu t}\ dt\right|\\
&\le \int_{-\infty}^{\infty}\left|f(t)e^{-2\pi i \nu t}\ \right|~dt\\
&= \int_{-\infty}^{\infty}|f(t)|\ dt\\
&= \|f\|_{\mathcal{L}^{1}}
\end{align*}$$
Thus, $$\left\|\widehat f(\nu)\right\|_{\infty}\le\|f(t)\|_{\mathcal{L}^{1}}<\infty$$

(2) An application of the bound in (1).