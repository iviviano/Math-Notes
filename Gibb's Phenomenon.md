

For the [[Sawtooth Wave]]

[[Fourier Polynomial]]s: $$\phi_{n}=\sum_{k=1}^{n} \frac{\sin(kx)}{k}$$



$$\|\phi_{n}-\phi\|\not\rightarrow 0\iff\exists \epsilon>0:\|\phi_{n}-\phi\|_{\infty}\ge \epsilon$$infinitely often in $n$

Let $$t_{n}= \frac{\pi}{n+1}$$be the location of the first maximum of $\phi_{n}$.

$$\begin{align*}
\|\phi_{n}-\phi\|_{\infty}&\ge |\phi_{n}(t_{n})-\phi(t_{n})|\\
&= \left|\sum_{k=1}^{n}\frac{\sin(k \frac{\pi}{n+1})}{k}- \phi(t_{n})\right|\\
&= \left|\sum_{k=1}^{n}\frac{\sin(k \frac{\pi}{n+1})}{k \frac{\pi}{n+1}} \cdot\frac{\pi}{n+1}- \phi(t_{n})\right|\\
&= \left|\underbrace{\sum_{k=1}^{n+1}\text{sinc}(k \frac{\pi}{n+1})}_{\text{lower Riemann sum}}-\phi(t_{n})\right|\\
&\rightarrow \left|\int_{0}^{\pi}\text{sinc}(y)\ dy- \frac{\pi}{2}\right|:=\epsilon_{0}\\
&> 0
\end{align*}$$
we have the lower Riemann since $\text{sinc}$ is decreasing

This shows that $$\liminf\|\phi_{n}-\phi\|_{\infty}\ge \epsilon_{0}$$
