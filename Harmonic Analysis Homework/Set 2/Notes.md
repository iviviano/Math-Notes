

>[!note] 1


(b) Suppose $y(x,t)=f(x)\cdot g(t)$ is a solution to the 1-dimensional wave equation: $$\begin{equation}\frac{\partial ^{2}y}{\partial t^{2}}=c^{2} \frac{\partial ^{2}y}{\partial x^{2}}\end{equation}$$Note that $$\begin{align*}
\frac{\partial y}{\partial t}&= \frac{\partial }{\partial t}(f(x)\cdot g(t))=f(x)\cdot\frac{\partial }{\partial t}g(t)=f(x)g'((t)\\
\frac{\partial ^{2}y}{\partial t^{2}}&= f(x)g''(t)\\
\frac{\partial ^{2}y}{\partial x^{2}}&= f''(x)g(t)
\end{align*}$$
So, $$f(x)g''(t)=c^{2}f''(x)g(t)$$On $f(x)\ne0$ and $g(t)\ne 0$, this may be written $$\begin{equation}\frac{g''(t)}{g(t)}=c^{2}\frac{f''(x)}{f(x)}\end{equation}$$Note that if $f(x)=0$ or $g(t)=0$, $y(x,t)=0$, so $y$ satisfies (1). So, any separated solution $y$ to (1) must only satisfy (2).

Suppose $y(x,t)=f(x)g(t)$ is a solution to (1). Fix $t_{0}\in \mathbb{R}$ with $g(t_{0})\ne0$ and let $$-k= \frac{g''(t_{0})}{g(t_{0})}$$Then, for all $x\in \mathbb{R}$ with $f(x)\ne0$, $$\begin{equation}-k=c^{2} \frac{f''(x)}{f(x)}\end{equation}$$So, $f$ is a solution to NUMBER. Similarly, fixing an $x$ shows that $g$ is a solution to $$\begin{equation}-k= \frac{g''(t)}{g(t)}\end{equation}$$
(c) We now apply the boundary condition $y(0,t)=y(l,t)=0$. We have $y(x,t)=f(x)\cdot g(t)$. If $f(0)=0$ and $f(l)=0$, then for all $t$, $$\begin{align*}
y(0,t)&= f(0)\cdot g(t)=0\cdot g(t)=0\\
y(l,t)&= f(l)\cdot g(t)=0\cdot g(t)=0
\end{align*}$$
so the boundary conditions are satisfied. 

Suppose $f(0)\ne0$. We need that for all $t$, $y(0,t)=0$: $$0=y(0,t)=f(0)\cdot g(t)\implies g(t)=0$$But this is only possible if $g$ is identically 0. This gives $f$ identically 0, not a solution we are interested in. The same argument shows that $f(l)=0$ for any separated solution to the initial value problem.

Thus, $y(x,t)=f(x)\cdot g(t)$ is a solution to the initial value problem (1) if and only if $f(0)=f(l)=0$. 


(d) 

Solve: $$f''+kf=0$$
From Set 1, the general solution is $$f(x)=A\cos \sqrt{k}x+B\sin \sqrt{k}x$$
Suppose there is a nonzero solution $f$ that satisfies the initial value problem $f(0)=f(l)=0$. Then, $$\begin{align*}
0=f(0)&= A\cos \sqrt{k}0+B\sin \sqrt{k}0\\
&= A
\end{align*}$$
So, $A=0$. The second boundary condition gives $$\begin{align*}
0=f(l)&= B\sin(\sqrt{k}l)\\
\sin(\sqrt{k}l)&= 0
\end{align*}$$
This occurs when $\sqrt{k}\cdot l=\pi\cdot n$ for some integer $n$. Solving for $k$, we see that possible values are $$k= \left(\frac{n\pi}{l}\right)^{2}$$

Let $k_{n}=\left(\frac{n\pi}{l}\right)^{2}$. Then, for all $n$, the function $f_n$ defined by $$f_{n}(x)=\sin \sqrt{k}x$$is a solution to the initial value problem: $$\begin{align*}
f_{n}'(x)&= \sqrt{k}\cos \sqrt{k}x\\
f_{n}''(x)&= -k\sin \sqrt{k}x\\
f_{n}(0)&= 0\\
f_{n}(l)&= \sin \sqrt{k}l=\sin\left(\frac{n\pi}{l}\cdot l\right)=0\\
f''(x)+kf(x)&= -k\sin \sqrt{k}x+k\sin \sqrt{k}x=0
\end{align*}$$
(e) Solving the time differential equation, $$g''+kc^{2}g=0$$we get the general solution $$g(x)=A\cos c\sqrt{k}t+B\sin c\sqrt{k}t$$which may be rewritten $$g(x)=B\sin(c\sqrt{k}t+\phi)$$

The general solution to the wave equation is the product of the these two solutions for the same $k$ value. So, $$y=C\sin\left(\frac{cn\pi t}{l}+\phi\right)\sin\frac{n\pi t}{l}$$where $C\in \mathbb{R}$ is a constant that represents the product of the temporal and spacial amplitudes. 

>[!note] 2

This will restrict to the Bernoulli solutions with a node at $x= \frac{l}{N}$. We need Bernoulli solutions with $$f_{n}\left(\frac{l}{N}\right)=0$$Solving $$0=\sin\left(\frac{n \pi x}{\frac{l}{N}}\right)=\sin\left(\frac{nN\pi x}{l}\right)$$we get $f_k$ where $k=nN$ for some $n\in \mathbb{N}$. These are the Bernoulli solutions where $k$ is divisible by $N$.



>[!note] 3

$$\frac{d}{dt}e^{\lambda t}=\lambda e^{\lambda t}$$

$$\int_{a}^{b} e^{\lambda t}=\frac{1}{\lambda}(e^{\lambda b}-e^{\lambda a})$$if $\lambda\ne0$


>[!note] 4

Let $a_{n}$ be a [[Sequence]] in $\mathbb{C}$ and suppose $a_{n}\rightarrow a\in \mathbb{C}$. 

Goal: $a_{n}$ does [[Converge in Cesaro Mean]] to $a$. 


Let $a_{n}$ be a sequence in $\mathbb{C}$ with $a_{n}\rightarrow a\in \mathbb{C}$. Let $$C_{n}= \frac{1}{n}\sum_{k=1}^{n}a_{k}$$
Let $\epsilon>0$ be given and pick $M\in \mathbb{N}$ such that for all $n\ge M$, $$|a_{n}-a|< \frac{\epsilon}{2}$$
Choose $N\ge M$ such that $$\frac{1}{N}\sum_{k=1}^{M}|a_{k}-a|< \frac{\epsilon}{2}$$
Let $$N=something$$Then, if $n\ge N$,
$$\begin{align*}|C_{n}-a|&= \left| \frac{1}{n}\sum_{k=1}^{n}a_{k}-a\right|\\
&= \left| \frac{1}{n}\sum_{k=1}^{n}a_{k}- \frac{1}{n}\sum_{k=1}^{n} a\right|\\
&= \left| \frac{1}{n}\sum_{k=1}^{n}(a_{k}-a)\right|\\
&\le \frac{1}{n}\sum_{k=1}^{n}\left|a_{k}-a\right|\quad (\Delta\text{ inequality in }\mathbb{C})\\
&= \frac{1}{n}\sum_{k=1}^{M}|a_{k}-a|+ \frac{1}{n}\sum_{k=M+1}^{n}\left|a_{k}-a\right|\\
&\le \frac{1}{N}\sum_{k=1}^{M}\left|a_{k}-a\right|+ \frac{1}{n}\sum_{k=M+1}^{n}\left|a_{k}-a\right|\\
&< \frac{\epsilon}{2}+ \frac{(n-N)}{n}\cdot \frac{\epsilon}{2}\\
&\le \frac{\epsilon}{2}+\frac{\epsilon}{2}\\
&= \epsilon
\end{align*}$$



>[!note] 5

(a) Note that $$
\left|e^{-2\pi int}\right|= 1
$$for all $t\in \mathbb{R}$, and for a 1-periodic function $f$, $$\|f\|_{\infty}=\sup\{f(x):x\in[0,1]\}$$
Then, 
$$\begin{align*}
|\hat{f_{n}}|&= \left|\int_{0}^{1}e^{-2\pi int}f(t)\ dt\right|\\
&\le \int_{0}^{1}\left| e^{-2\pi int}f(t)\right|dt\quad(\Delta \text{ inequality})\\
&= \int_{0}^{1}\left|e^{-2\pi int}\right|\cdot \left|f(t)\right|\ dt\\
&= \int_{0}^{1}|f(t)|\ dt\\
&\le 1\cdot\sup_{x\in[0,1]}f(x)\quad(\text{ML estimate})\\
	&= \|f\|_{\infty}
\\
\end{align*}$$

(b) Integration by parts: $$\int u(t)v'(t)\ dt= u(t)v(t)-\int u'(t)v(t)\ dt\quad(\text{IBP})$$
Let $u(t)=f(t)$ and $v'(t)=e^{-2\pi int}$. By problem (3), $$v(t)=\frac{e^{-2\pi int}}{-2\pi in}$$is an antiderivative of $v$. Note that $$\begin{align*}
v(0)&= \frac{-1}{2\pi in}\\
v(1)&= -\frac{e^{-2\pi in}}{{2\pi in}}
\end{align*}$$
$$\begin{align*}
\hat{f_{n}}&= \int_{0}^{1}e^{-2\pi int}f(t)\ dt\\
&= \left. u(t)v(t)\right|_{0}^{1}-\int_{0}^{1}u'(t)v(t)\ dt\\
&= \frac{f(0)-e^{-2\pi in}f(1)}{2\pi in}+ \frac{1}{{2\pi in}}\int_{0}^{1} f'(t)e^{-2\pi int}\ dt \\
&= \frac{f(0)-e^{-2\pi in}f(1)+\hat{f'_{n}}}{2\pi in}
\end{align*}$$

(c)

let $P(m)$ be that $$\hat{f_{n}}= \left(\frac{1}{2\pi in}\right)^{m}\left(\hat{f_{n}}^{(m)}+\sum_{l=0}^{m-1}(2\pi in)^{m-1-l}(f^{(l)}(0)-e^{-2\pi in}f^{(l)}(1))\right)$$


Base Case: $m=1$

$$\begin{align*}
\frac{1}{2\pi in}\left(\hat{f'_{n}}+\sum_{l=0}^{0}(2\pi in)^{0-l}(f^{(l)}(0)-e^{-2\pi in}f^{(l)}(1))\right)&= \frac{1}{2\pi in}(\hat{f_{n}'}+f(0)-e^{-2\pi in}f(1))
\end{align*}$$
which equals $\hat{f_{n}}$ by (b), so $P(1)$ is true.

Inductive Step: Assume $P(m)$ for some $1\le m<k$

$$\begin{align*}
\hat{f_{n}}^{(m)}&= \frac{f^{(m)}(0)-e^{-2\pi in}f^{(m)}(1)+\hat{f_{n}}^{(m+1)}}{2\pi in}\\
\hat{f_{n}}&= \left(\frac{1}{2\pi in}\right)^{m}\left(\hat{f_{n}}^{(m)}+\sum_{l=0}^{m-1}(2\pi in)^{m-1-l}(f^{(l)}(0)-e^{-2\pi in}f^{(l)}(1))\right)\\
&= \left(\frac{1}{2\pi in}\right)^{m}\left(\frac{f^{(m)}(0)-e^{-2\pi in}f^{(m)}(1)+\hat{f_{n}}^{(m+1)}}{2\pi in}+\sum_{l=0}^{m-1}(2\pi in)^{m-1-l}(f^{(l)}(0)-e^{-2\pi in}f^{(l)}(1))\right)\\
&= \left(\frac{1}{2\pi in}\right)^{m+1}\left(\hat{f_{n}}^{(m+1)}+f^{(m)}(0)-e^{-2\pi in}f^{(m)}(1)+\sum_{l=0}^{m-1}(2\pi in)^{m-l}(f^{(l)}(0)-e^{-2\pi in}f^{(l)}(1))\right)\\
&= \left(\frac{1}{2\pi in}\right)^{m+1}\left(\hat{f_{n}}^{(m+1)}+(2\pi i n)^{m-m}(f^{(m)}(0)-e^{-2\pi in}f^{(m)}(1))+\sum_{l=0}^{m-1}(2\pi in)^{m-l}(f^{(l)}(0)-e^{-2\pi in}f^{(l)}(1))\right)\\
&= \left(\frac{1}{2\pi in}\right)^{m+1}\left(\hat{f_{n}}^{(m+1)}+\sum_{l=0}^{m}(2\pi in)^{m-l}(f^{(l)}(0)-e^{2\pi in}f^{(l)}(1))\right)\\
&= \left(\frac{1}{2\pi in}\right)^{m+1}\left(\hat{f_{n}}^{(m+1)}+\sum_{l=0}^{(m+1)-1}(2\pi in)^{(m+1)-1-l}(f^{(l)}(0)-e^{2\pi in}f^{(l)}(1))\right)\\

\end{align*}$$
So, $P(m+1)$.

Therefore, by (PMI), $P(m)$ for all $1\le m\le k$. In particular, $$\hat{f_{n}}= \left(\frac{1}{2\pi in}\right)^{k}\left(\hat{f_{n}}^{(k)}+\sum_{l=0}^{k-1}(2\pi in)^{k-1-l}(f^{(l)}(0)-e^{-2\pi in}f^{(l)}(1))\right)$$
Now, $$\begin{align*}
&\left|\hat{f_{n}}^{(k)}+\sum_{l=0}^{k-1}(2\pi in)^{k-1-l}(f^{(l)}(0)-e^{-2\pi in}f^{(l)}(1))\right|\\
&\le \left|\hat{f_{n}}^{(k)}\right|+\left|\sum_{l=0}^{k-1}(2\pi in)^{k-1-l}(f^{(l)}(0)-e^{-2\pi in}f^{(l)}(1))\right|\\
&\le \left\|f^{(k)}\right\|+\left|\sum_{l=0}^{k-1}(2\pi in)^{k-1-l}(f^{(l)}(0)-e^{-2\pi in}f^{(l)}(1))\right|\\
:&= C\in \mathbb{R}x
\end{align*}$$
Then, $$\begin{align*}
\left|\hat{f_{n}}\right|&\le \left| \left(\frac{1}{2\pi in}\right)^{k}\cdot C\right|= \frac{C}{|n|^{k}}
\end{align*}$$

>[!note] 6



Let $\phi$ be the $2\pi$-periodic function described by $$\phi(\theta)= \frac{\pi-\theta}{2}$$and $\phi(0)=\phi(2\pi)=0$. 
For all $n\ne0,$
$$\begin{align*}
\int_{0}^{2\pi}e^{-ni\theta}d\theta&= - \left.\frac{e^{ni\theta}}{ni}\right|_{0}^{2\pi}=0\\
\int_{0}^{2\pi} \frac{\theta}{2}e^{-ni \theta}\ d\theta&= \left.\frac{-\theta e^{-ni\theta}}{2ni}\right|^{2\pi}_{0}-\int_{0}^{2\pi} e^{-ni\theta}\ d \theta\\
&= \frac{-2\pi}{2ni}=- \frac{\pi}{ni}\\
\hat{f_{n}}&= \int_{0}^{2\pi}\phi(\theta)e^{-ni \theta}\ d\theta\\
&= \int_{0}^{2\pi} \frac{\pi-\theta}{2}e^{-ni \theta}\ d \theta\\
&= \int_{0}^{2\pi} \frac{\pi}{2}e^{-ni \theta}d \theta-\int_{0}^{2\pi} \frac{\theta}{2}e^{-ni \theta}\ d \theta\\
&= \frac{\pi}{ni}
\end{align*}$$
And for $n=0$, $$\int_{0}^{2\pi}\phi(\theta)e^{-ni\theta}\ d\theta=\int_{0}^{2\pi} \frac{\pi-\theta}{2}d\theta$$
$$\begin{align*}
\hat{f_{0}}&= \int_{0}^{2\pi}\phi(\theta)e^{-ni\theta}\ d\theta=\int_{0}^{2\pi} \frac{\pi-\theta}{2}d\theta\\
&=\left. \frac{\pi}{2}\theta- \frac{\theta^{2}}{4}\right|_{0}^{2\pi}\\
&= \pi^{2}- \frac{(2\pi)^{2}}{4}=0
\end{align*}$$

So, the Fourier series is $$\begin{align*}
f(t)&= \sum_{n=-1}^{-\infty}\hat{f_{n}}e^{int}+\hat{f_{0}}+\sum_{n=1}^{\infty}\hat{f_{n}}e^{int}\\
&= \sum_{n=-1}^{-\infty}\hat{f_{n}}e^{int}+0+\sum_{n=1}^{\infty}\hat{f_{n}}e^{int}\\
&=\sum_{n=1}^{\infty}\hat{f_{-n}}e^{-int}+\sum_{n=1}^\infty\hat{f_{n}}e^{int}\\
&=\sum_{n=1}^{\infty} \frac{\pi}{-ni}(\cos (-nt)+i\sin(-nt))+\sum_{n=1}^{\infty} \frac{\pi}{ni}(\cos nt+i\sin nt)\\
&=\sum_{n=1}^{\infty} \frac{\pi}{ni}(-\cos nt+i\sin nt)+\sum_{n=1}^{\infty} \frac{\pi}{ni}(\cos nt+i\sin nt)\\
&=\sum_{n=1}^{\infty} \frac{\pi}{ni}(-\cos nt+\cos nt +2i\sin nt)\\
&=\sum_{n=1}^{\infty} \frac{2\pi}{n}\sin nt
\end{align*}$$

