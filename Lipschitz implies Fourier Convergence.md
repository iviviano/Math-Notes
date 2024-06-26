---
mathLink: Lipschitz implies Fourier convergence
---
>[!thm] Theorem 1
Let $f\in\mathcal{C_1}(\mathbb{R};\mathbb{C})$ be given. Suppose there exists a $t_{0}\in \mathbb{R}$ such that $f$ is [[Point-wise Lipschitz Condition]] at $t_{0}$. Then, the [[Fourier Series]] of $f$ [[Converges (series)]]s [[Point-wise]] at $t_{0}$ with value given by $$\lim_{n=-\infty}S_{n}[f](t_{0})=\mathcal{PV}\left\{\sum_{n=-\infty}^{\infty}\hat{f}_{n}e^{2\pi int_{0}}\right\}=f(t_{0})$$The [[Double-Sided Series]] [[Converges (series)]]s to the [[Principal Value]] in the [[Banach Space]] $(\mathbb{C},|.|)$.

>[!thm] Theorem 2
Let $f\in\mathcal{C}_{1}(\mathbb{R};\mathbb{C})$ be given. Suppose that $A\subseteq \mathbb{R}$ so that the [[Intersection]] with one [[Period]] of $f$ $$A\cap[0,1]\text{ is compact in }\mathbb{R}$$and that $f$ satisfies a [[Lipschitz Condition]] condition on $A$, $$L_{A}:=\sup_{t_{1},t_{2}\in A:t_{1}\ne t_{2}}\left|\frac{f_{t_{1}}-f(t_{2})}{t_{1}-t_{2}}\right|<\infty$$Then, the [[Converges (series)]]nce $S_{n}[f]\rightarrow f$is uniform on $A$: $$\|S_{n}[f]-f\|_{A;\infty}\rightarrow 0\text{ as }n \rightarrow \infty$$




>[!proof] Proof (1)

Strategy:
Split into two integrals: 
1. First estimate with the Lipschitz condition
2. Second estimate with the [[Riemann-Lebesgue Lemma]]


Let $0<\epsilon\le \delta$
$$\begin{align*}
\left|S_{n}[f](t_{0})-f(t_{0})\right|&= \left|\int_{0}^{1}D_{n}(s)f(t_{0}-s)\ ds-\underbrace{f(t_{0})}_{\int_{-\frac{1}{2}}^{\frac{1}{2}}f(t_{0})D_{n}(s)\ ds}\right|\\
&= \left|\int_{0}^{1}(f(t_{0}-s)-f(t_{0}))D_{n}(s)\ ds\right|\\
&= \left|\int_{0}^{1}(f(t_{0}-s)-f(t_{0})) \frac{\sin(\pi(2n+1)s)}{\sin(\pi s)}\ ds\right| \\
&\le \left|\underbrace{\int_{|s|\le \epsilon}...\ ds}_{I_{n;\epsilon}^{(1)}}\right|+\left|\underbrace{\int_{[\frac{-1}{2},\frac{1}{2}]-[-\epsilon,\epsilon]}...\ ds}_{I_{n;\epsilon}^{(2)}}\right|\\
I_{n;\epsilon}^{(1)}&= \left|\int_{-\epsilon}^{\epsilon} \frac{f(t_{0}-s)-f(t_{0})}{\sin(\pi s)}\sin(\pi(2n+1)s)\ ds\right|\\
&\le \int_{-\epsilon}^{\epsilon} \left|\frac{f(t_{0}-s)-f(t_{0})}{\underbrace{\sin(\pi s)}}_{≤2|s|}\right|\cdot\underbrace{|\sin(\pi(2n+1)s)|}_{≤1}\ ds\\
&\le \frac{1}{2}\int_{-\epsilon}^{\epsilon} \frac{|f(t_{0}-s)-f(t)|}{|s|}\ ds\\
&\le \frac{1}{2}\int_{-\epsilon}^{\epsilon}L_{t_{0}} \frac{|s|}{|s|}\ ds\\
&\le \frac{1}{2}L_{t_{0}}2\epsilon\\
&= \epsilon L_{t_{0}}\\
\end{align*}$$
Let $$X=\left[- \frac{1}{2},\frac{1}{2}\right]-[-\epsilon,\epsilon]$$
$$\begin{align*}
I_{n;\epsilon}^{(2)}&= \left|\int_{X} \frac{f(t_{0}-s)-f(t_{0})}{\sin(\pi s)}\sin(\pi(2n+1)s)\ ds\right|\\
\end{align*}$$

Write the $\sin$ term with the complex exponential: $$\begin{align*}\sin(\pi(2n+1)s)&= \Im \text{m}(e^{\pi(2n+1)s})\\
&= \frac{1}{2i}(e^{\pi(2n+1)s}-\overline{e^{\pi(2n+1)s}}\\
&= \frac{1}{2i}(e^{\pi(2n+1)s}-e^{-\pi(2n+1)s})\\
&= \frac{1}{2i}(e^{2\pi ins}e^{\pi is}-e^{-2\pi ins}e^{-\pi is})\end{align*}$$and define two functions $$g^{(\pm)}(s):=\begin{cases} \frac{f(t_{0}-s)-f(t_{0})}{\sin(\pi s)}e^{\pm \pi is} & s\in X \\
0 & |s|\le \epsilon\end{cases}$$
$g^{(\pm)}$ may have jumps only at $s=\pm \epsilon,\pm \frac{1}{2}$. Therefore, $g^{(\pm)}$ is [[Piece-wise Continuous]] and satisfies the [[Riemann-Lebesgue Lemma]]. Now compute: $$\begin{align*}
I^{\epsilon}_{n;\epsilon}&= \left|\int_{X}\frac{f(t_{0}-s)-f(t_{0})}{\sin(\pi s)}\sin(\pi(2n+1)s)\ ds\right|\\
&= \left|\int_{X} \frac{1}{2i}(e^{2\pi ins}e^{\pi is}-e^{-2\pi ins}e^{-\pi i s})\frac{f(t_{0}-s)-f(t_{0})}{\sin(\pi s)}\ ds\right|\\
&\le \left|\int_{X} \frac{1}{2i}(e^{2\pi ins}e^{\pi is})\frac{f(t_{0}-s)-f(t_{0})}{\sin(\pi s)}\ ds\right|+\left|\int_{X} \frac{1}{2i}(e^{-2\pi ins}e^{-\pi is})\frac{f(t_{0}-s)-f(t_{0})}{\sin(\pi s)}\ ds\right|\\
&= \left|\int_{X} \frac{1}{2i}g^{(+)}(s)e^{2\pi ins}\ ds\right|+\left|\int_{X} \frac{1}{2i}g^{(-)}(s)e^{2\pi ins\ ds}\right|\\
&= \left|\int_\frac{-1}{2}^{\frac{1}{2}} \frac{1}{2i}g^{(+)}(s)e^{2\pi ins}\ ds\right|+\left|\int_\frac{-1}{2}^{\frac{1}{2}} \frac{1}{2i}g^{(-)}(s)e^{2\pi ins}\ ds\right|\quad(\text{since }g^{(\pm)}\text{ is 0 on }[-\epsilon,\epsilon])\\
&= \left| \frac{1}{2i}\widehat{[g^{(+)}]}_{n}\right|+ \left| \frac{1}{2i}\widehat{[g^{(-)}]}_{n}\right|\\
&\le \left| \widehat{[g^{(+)}]}_{n}\right|+ \left| \widehat{[g^{(-)}]}_{n}\right|\\
&\rightarrow 0
\end{align*}$$
by the [[Riemann-Lebesgue Lemma]]. 