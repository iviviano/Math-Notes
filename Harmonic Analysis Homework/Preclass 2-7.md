>[!note] 1.4
>$$\begin{align}
y(t)&=A\cos(\omega t)+B\sin(\omega t)\\
\frac{dy}{dt}&=-\omega A\sin(\omega t)+\omega B\cos(\omega t)\\
\frac{d^{2}y}{d t^{2}}&=-\omega^{2}A\cos(\omega t)-\omega^{2}B\sin(\omega t)\\\\
\frac{d^{2}y}{dt^{2}}+\omega^{2}y&=-\omega^{2}A\cos(\omega t)-\omega^{2}B\sin(\omega t)+\omega^{2}(A\cos(\omega t)+B\sin(\omega t))=0
\end{align}$$

>[!proof] Proof of Prop 1.1
Suppose $f:[a,b]\rightarrow \mathbb{R}$ is [[Continuous]] and $f'$ exists on $(a,b)$ with $f'(x)=0$ for all $x\in(a,b)$. Let $c\in(a,b)$. By the [[Mean Value Theorem]], pick $d\in(c,b)$ such that $$\frac{f(b)-f(c)}{b-c}=f'(d)=0.$$Then, $f(b)-f(c)=0$, so $f(b)=f(c)$ for all $c\in(a,b)$. This shows that $f$ is constant on $(a,b]$. The same method can be used to show $f$ is constant on $[a,b)$. Therefore, $f$ is constant on $[a,b]$.

>[!note] 1.6
$(7)$ and Proposition 1.1 imply that $y'$ is constant. So, $y'=B$ for a parameter $B\in \mathbb{R}$. Then, $$y=\int y'\ dx=\int B\ dx=A+Bx$$

