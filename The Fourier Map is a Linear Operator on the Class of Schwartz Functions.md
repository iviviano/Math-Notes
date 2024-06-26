>[!prop]
For every $f\in\mathcal{S}(\mathbb{R};\mathbb{C})$, its [[Fourier Transform]] satisfies $\widehat f\in\mathcal{S}(\mathbb{R};\mathbb{C})$. [[Restriction]] of the [[Fourier Map]] $\mathcal{F}$ to $\mathcal{S}(\mathbb{R};\mathbb{C})$ gives a [[Linear Transformation]]: $$\mathcal{F}:\mathcal{S}(\mathbb{R};\mathbb{C})\rightarrow \mathcal{S}(\mathbb{R};\mathbb{C})$$

>[!note]
>Since $\mathcal{F}$ is also [[Bijective]] ([[Fourier Inversion Property]]) and an [[Isometry]] ([[Parseval Identity]]), it is [[Unitary]]


>[!proof]

$\widehat f\in\mathcal{S}(\mathbb{R};\mathbb{C})$:
Let $C_{m,n}$ be the [[Schwartz Function]] constants of $f$. We apply the [[Fourier Differentiation Mantra]]:
$$\begin{align*}
\left| \nu^{m} \frac{d^{n}}{d \nu^{n}}\widehat f(\nu)\right|&= \left|\nu^{m} \frac{d^{n}}{d \nu^{n}}\int_{-\infty}^{\infty}f(t)e^{-3\pi i \nu t}\ dt\right|\\
&= \left|\nu^{m} \int_{-\infty}^{\infty}f(t) \underbrace{\frac{\partial ^{n}}{\partial  \nu^{n}}(e^{-2\pi i \nu t})}_{=(-2\pi i t)^{n}e^{-2\pi i \nu t}}\ dt\right|\\
&= \left|\nu^{m}\int_{-\infty}^{\infty}\underbrace{f(t)\cdot (-2\pi i t)^{n}}_{:=g(t)\in\mathcal{S(\mathbb{R})}}e^{-2\pi i \nu t}\ dt\right|\\
&= \left|\nu^{m}\widehat g(\nu)\right|\\
&= \frac{1}{(2\pi)^{m}}\left|\widehat{[g^{m)}]}(\nu)\right|\\
&\le \|g^{(m)}\|_{\mathcal{L}^{1}}\cdot \frac{1}{(2\pi)^{m}}\\
\end{align*}$$
To create $g$, we note that the product of a [[Schwartz Function]] [[Function]] with a polynomial is a [[Schwartz Function]] [[Function]]. We justified moving the derivative inside the integral on [[set_3.pdf]] (the modification of this argument to an unbounded integration interval comes from the decay of Schwartz functions). The bound on $\widehat{[g^{(m)}]}$ comes from the [[Fourier Transform Bound]]. 