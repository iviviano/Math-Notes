>[!1]

From integration by parts, we have $$\int x^{2}\cos x\ dx=2x\cos x+(x^{2}-2)\sin x+C$$
Let $f:[0,1]\rightarrow \mathbb{R}$ be the 1-periodic extension of $f(t)=(\pi t)^{2}$. As $f\in\mathcal{PC}_{1}(\mathbb{R};\mathbb{R})$, its real Fourier series converges pointwise: $$\frac{1}{2}(f(t+)+f(t-))= \frac{1}{2}a_{0}+\sum_{n=1}^{\infty}a_{n}\cos(2\pi nt)+\sum_{n=1}^{\infty}b_{n}\sin(2\pi nt),\text{ for all }t\in \mathbb{R}$$where $$\begin{align*}
a_{n}&:= 2\int_{0}^{1}f(t)\cos(2\pi int)\ dt\\
b_{n}&:= 2\int_{0}^{1}f(t)\sin(2\pi int)\ dt
\end{align*}$$
Compute: $$\begin{align*}
\text{for }n>0,a_{n}&= 2\int_{0}^{1}f(t)\cos(2\pi nt)\ dt\\
&= 2\int_{0}^{1}(\pi t)^{2}\cos(2\pi nt)\ dt\quad(\text{substitute }u=2\pi nt)\\
&= \frac{1}{4\pi n^{3}}\int_{0}^{2\pi n}u^{2}\cos u\ du\\
&= \frac{1}{4\pi n^{3}}(2u\cos u+(u^{2}-2)\sin u)\bigg|_{0}^{2\pi n}\\
&= \frac{1}{4\pi n^{3}}(4\pi n \cdot\underbrace{\cos(2\pi n)}_{=1}+((2\pi n)^{2}-2)\cdot\underbrace{\sin (2\pi n)}_{=0}-(2\cdot0\cos 0-2\sin0))\\
&= \frac{1}{{4\pi n^{3}}}\cdot 4\pi n\\
&= \frac{1}{n^{2}}\\
\text{for }n=0,a_{0}&= 2\int_{0}^{1}(\pi t)^{2}\cos(2\pi 0t)\ dt\\
&= 2\int_{0}^{1}\pi^{2}t^{2}\ dt\\
&= \frac{2\pi^{2}t^{3}}{3}\bigg|_{0}^{1}\\
&= \frac{2\pi^{2}}{3}
\end{align*}$$

Thus, $$\frac{1}{2}(f(t+)+f(t-))= \frac{\pi^{2}}{3}+\sum_{n=1}^{\infty} \frac{1}{n^{2}}\cos(2\pi nt)+\sum_{n=1}^{\infty}b_{n}\sin(2\pi nt)$$
Note that at $0$, $$\begin{align*}
f(t+)&= 0\\
f(t-)&= \pi^{2}\\
\frac{1}{2}(f(t+)+f(t-))&= \frac{\pi^{2}}{2}
\end{align*}$$
So, $$\begin{align*}
\frac{\pi^{2}}{2}&= \frac{1}{2}(f(0+)+f(0-))\\
&= \frac{\pi^{2}}{3}+\sum_{n=1}^{\infty} \frac{1}{n^{2}}\ \underbrace{\cos(2\pi n0)}_{=1}+\sum_{n=1}^{\infty}b_{n}\ \underbrace{\sin(2\pi n0)}_{=0}\\
&= \frac{\pi^{2}}{3}+\sum_{n=1}^{\infty} \frac{1}{n^{2}}
\end{align*}$$So, $$\sum_{n=1}^{\infty} \frac{1}{n^{2}}= \frac{\pi^{2}}{2}- \frac{\pi^{2}}{3}= \frac{\pi^{2}}{6}$$

---
Let $f:[\frac{-1}{2},\frac{1}{2}]\rightarrow \mathbb{R}$ be the 1-periodic extension of $f(t)=(\pi t)^{2}$. Since $f\in\mathcal{C}^{1}_{1}(\mathbb{R};\mathbb{R})$, its real Fourier series converges pointwise: $$f(t)= \frac{1}{2}a_{0}+\sum_{n=1}^{\infty}a_{n}\cos(2\pi nt),\text{ for all }t\in \mathbb{R}$$Note that since $f$ is even, $b_{n}=0$ for all $n$. Compute: $$\begin{align*}
\text{for }n>0, a_{n}&= 2\int_{-\frac{1}{2}}^{\frac{1}{2}}f(t)\cos(2\pi nt)\ dt\\
&= 4\int_{0}^{\frac{1}{2}}f(t)\cos(2\pi nt)\ dt\quad(f,\cos \text{ even})\\
&= 4\int_{0}^{\frac{1}{2}}(\pi t)^{2}\cos(2\pi nt)\ dt\\
&= \frac{1}{2\pi n^{3}}(2u\cos u+(u^{2}-2)\sin u)\bigg|_{0}^{\pi n}\\
&= \frac{1}{2\pi n^{3}}(2\pi n\cdot \underbrace{\cos(\pi n)}_{=(-1)^{n}}+((\pi n)^{2}-2)\cdot\underbrace{\sin(\pi n)}_{=0}-(2\cdot0\cdot\cos 0-2\sin0))\\
&= \frac{1}{2\pi n^{3}}\cdot 2\pi n(-1)^{n}\\
&= \frac{(-1)^{n}}{n^{2}}\\
\text{for }n=0,a_{0}&= 2\int_{- \frac{1}{2}}^{\frac{1}{2}}f(t)\cos(2\pi 0t)\ dt\\
&= 4\int_{0}^{\frac{1}{2}}(\pi t)^{2}\ dt\\
&= \frac{4\pi^{2}t^{3}}{3}\bigg|_{0}^{\frac{1}{2}}\\
&= \frac{\pi^{2}}{6}
\end{align*}$$
Thus, $$f(t)= \frac{\pi^{2}}{12}+\sum_{n=1}^{\infty} \frac{(-1)^{n}}{n^{2}}\cos(2\pi nt)$$So, $$\begin{align*}
0&= f(0)\\
&= \frac{\pi^{2}}{12}+\sum_{n=1}^{\infty} \frac{(-1)^{n}}{n^{2}}\cos(2\pi n0)\\
&= \frac{\pi^{2}}{12}+\sum_{n=1}^{\infty} \frac{(-1)^{n}}{n^{2}}
\end{align*}$$So, $$\sum_{n=1}^{\infty} \frac{(-1)^{n}}{n^{2}}= - \frac{\pi^{2}}{12}$$


>[!2]

Let $x,y\in V$ be two linearly independent vectors. Since $y\ne0$, $\langle y,y\rangle \ne0$. Define $$\begin{align*}\lambda:= \frac{\langle y,x\rangle}{\|y\|^{2}}\\
\bar \lambda:=\frac{\langle x,y\rangle}{\|y\|^{2}} \end{align*}$$Using repeated applications of [[Linearity in the Second Entry]] and [[Conjugate Symmetry]], compute:
$$\begin{align*}
\|x-\lambda y\|^{2}&= \langle x-\lambda y,x-\lambda y\rangle\\
&= \langle x-\lambda y, x\rangle - \lambda\langle x-\lambda y, y\rangle\\
&= \overline{\langle x, x-\lambda y\rangle}-\lambda\overline{\langle y,x-\lambda y\rangle}\\
&= \overline{\langle x,x\rangle-\lambda\langle x,y\rangle}-\lambda(\overline{\langle y,x\rangle-\lambda\langle y,y\rangle})\\
&= \overline{\langle x,x\rangle}-\bar \lambda\cdot\overline{\langle x, y\rangle}-\lambda\overline{\langle y,x\rangle}+\lambda\cdot\bar \lambda\cdot\overline{\langle y,y\rangle}\\
&= \langle x,x\rangle-\bar \lambda\cdot\overline{\langle x, y\rangle}-\lambda\overline{\langle y,x\rangle}+|\lambda|^{2}\langle y,y\rangle\\
&= \|x\|^{2}- \frac{\langle x,y\rangle\overline{\langle x,y\rangle}}{\|y\|^{2}}- \frac{\langle y,x\rangle\overline{\langle y,x\rangle}}{\|y\|^{2}}+ \frac{|\langle x,y\rangle|^{2}}{\|y\|^{4}}\|y\|^{2}\\
&= \|x\|^{2}- 2\frac{|\langle x,y\rangle|^{2}}{\|y\|^{2}} + \frac{|\langle x,y\rangle|^{2}}{\|y\|^{2}}\\
&= \|x\|^{2}- \frac{|\langle x,y\rangle|^{2}}{\|y\|^{2}}
\end{align*}$$
Since $0\le\|x-\lambda y\|^{2}$, $$\frac{|\langle x,y\rangle|^{2}}{\|y\|^{2}}\le \|x\|^{2}\iff|\langle x,y\rangle|^{2}\le\|x\|^{2}\|y\|^{2}$$Since $\sqrt{}$ is monotonic, we have $$|\langle x,y\rangle|\le \|x\|\|y\|$$

Equality iff:

Let $x,y\in V$ be two linearly dependent vectors with $x= \lambda y$. Then, $$\begin{align*}
|\langle x,y\rangle|&= |\langle x, \lambda x\rangle|\\
&= |\lambda\langle x,x\rangle|\\
&= |\lambda|\cdot|\underbrace{\langle x,x\rangle}_{\ge0}|\\
&= |\lambda|\cdot\langle x,x\rangle\\
&= |\lambda|\cdot{\|x\|}\  \|x\|\\\
&= \|x\|\ \|\lambda x\|\\
&= \|x\|\ \|y\|
\end{align*}$$ 
Suppose $|\langle x,y\rangle|=\|x\|\cdot\|y\|$. If $y=0$, then, $x$ and $y$ are trivially linearly dependent. Otherwise, let $\lambda:=\frac{\langle y,x\rangle}{\|y\|^{2}}$, and continue the prior computation: $$\begin{align*}
\|x-\lambda y\|^{2}&= \|x\|^{2}- \frac{|\langle x,y\rangle|^{2}}{\|y\|^{2}}\\
&= \|x\|^{2}- \frac{(\|x\|\|y\|)^{2}}{\|y\|^{2}}\\
&= \|x\|^{2}- \|x\|^{2}\\
&= 0
\end{align*}$$By the positive definiteness of the induced norm, $$x-\lambda y=0\iff x=\lambda y$$showing that $x$ and $y$ are linearly dependent.


>[!3]

By the [[Positive Definiteness]] of [[Inner Product]]s, we have $$\begin{align*}
0&= x\\
\iff0&= \langle x,x\rangle\\
\iff 0&= \sqrt{\langle x,x\rangle}=\|x\|\\
\end{align*}$$
Positive homogeneity: $$\begin{align*}
\|\lambda x\|&= \sqrt{\langle \lambda x,\lambda x\rangle}\\
&= \sqrt{\lambda\langle \lambda x,x\rangle}\\
&= \sqrt{\lambda\overline{\langle x,\lambda x\rangle}}\\
&= \sqrt{\lambda(\overline{\lambda\langle x,x\rangle})}\\
&= \sqrt{\lambda\cdot \bar \lambda\cdot\langle x,x\rangle}\\
&= \sqrt{|\lambda|^{2}\langle x,x\rangle}\\
&= |\lambda|\ \|x\|
\end{align*}$$
Triangle Inequality:
$$\begin{align*}
\|x+y\|^{2}&= \langle x+y,x+y\rangle\\
&= \langle x+y,x\rangle+\langle x+y,y\rangle\\
&= \overline{\langle x,x+y\rangle}+\overline{\langle y,x+y\rangle}\\
&= \overline{\langle x,x\rangle+\langle x,y\rangle}+\overline{\langle y,x\rangle+\langle y,y\rangle}\\
&= \overline{\langle x,x\rangle}+\overline{\langle x,y\rangle}+\overline{\langle y,x\rangle}+\overline{\langle y,y\rangle}\\
&= \langle x,x\rangle+\langle y,x\rangle+\langle x,y\rangle+\langle y,y\rangle\\
&\le \|x\|^{2}+\|y\|\cdot \|x\|+\|x\|\cdot\|y\|+\|y\|^{2}\quad(\text{Cauchy-Schwarz})\\
&= \|x\|^{2}+2\|x\|\cdot\|y\|+\|y\|^{2}\\
&= (\|x\|+\|y\|)^{2}
\end{align*}$$
Therefore, $$\|x+y\|\le \|x\|+\|y\|$$

>[!4]

(a) 

$f_{n}\rightarrow 0$ pointwise: Fix $x\in[0,1]$ and consider two cases. If $x=0$, then, for all $n\in \mathbb{N}$, $$f_{n}(x)=\sqrt{g_{n}(x)}=\sqrt{4n^{2}x}=0$$So, $f_{n}(0)\rightarrow 0$. If $x>0$, there exists $N\in \mathbb{N}$ such that $\frac{1}{N}<x$. For all $n\ge N$, $$\frac{1}{n}\le \frac{1}{N}<x$$so, $$|f_{n}(x)|=\left|\sqrt{g_{n}(x)}\right|= \left|\sqrt{0}\right|=0$$Therefore, $f_{n}(x)\rightarrow 0$ for all $x\in[0,1]$, so $f_{n}\rightarrow 0$ pointwise.


$f_{n}$ does not converge to $0$ in the $L^{2}$ norm: $$\begin{align*}
\|f_{n}\|_{2}^{2}&= \langle f_{n},f_{n}\rangle_{2}\\
&= \int_{0}^{1}\overline{f_{n}(t)}f_{n}(t)\ dt\\
&= \int_{0}^{1}f_{n}(t)f_{n}(t)\ dt\\
&= \int_{0}^{1}\left(\sqrt{g_{n}(t)}\right)^{2}\ dt\\
&= \int_{0}^{1}g_{n}(t)\ dt\\
&= 1
\end{align*}$$where the integral of $g_{n}$ was computed geometrically from its graph: 

PICTURE



Since $\|f_{n}\|_{2}^{2}=1$, $\|f_{n}\|_{2}=1$ for all $n$. 






(b) 

Claim: $j \rightarrow \infty$ and $n \rightarrow \infty$.
>[!proof]

Let $M>0$ be given and pick $N$ such that for all $n\ge N$, $$
n\ge 2^{M+1}
$$if 

$$\frac{n}{2}=\frac{2^{j}+k}{2}\le \frac{2^{j}+2^{j}}{2}= 2^{j}$$Therefore, $$\begin{align*}
j&= \log_{2}(2^{j})\\
&\ge \log_{2}\left(\frac{n}{2}\right)\quad(\log\text{ is monotonic})\\
&\ge \log_{2}\left(\frac{2^{M+1}}{2}\right)\\
&= \log_{2}(2^{M})\\
&= M
\end{align*}$$
$\|f_{n}\|_{2}\rightarrow 0$ as $n \rightarrow 0$: for $n=2^{j}+k$,  $$\begin{align*}
\|f_{n}\|^{2}_{2}&= \int_{0}^{1}\overline{f_{n}(t)}f_{n}(t)\ dt\\
&= \int_{0}^{1}f_{n}(t)f_{n}(t)\ dt\\
&= \int_{\frac{k}{2^{j}}}^{\frac{k+1}{2^{j}}}1\ dt\\
&= \frac{1}{2^{j}}
\end{align*}$$Therefore, $f_{n}\rightarrow 0$ in the $L^{2}$ sense as $j \rightarrow \infty$. As $j \rightarrow \infty$ with $n$, $\|f_{n}\|_{2}\rightarrow 0$



$f_{n}$ converges point-wise at no point $x\in[0,1]$. Fix $x\in[0,1]$. To show that $f_{n}(x)$ does not converge, we show that it is not a Cauchy sequence. This is equivalent to the statement: for all $N\in \mathbb{N}$, there exist $n,m\ge N\ge$ such that $$|f_{n}(x)-f_{m}(x)|=1$$
Let $N\in \mathbb{N}$ be arbitrary and 

Break into two cases: if $x=0$, define $$\begin{align*}
j_{n}&= N\\
k_{n}&= 0\\
j_{m}&= N\\
k_{m}&= 1
\end{align*}$$We have $$0\in\left[0, \frac{1}{2^{N}}\right]$$so, $f_{n}(0)=1$, but $$0\notin\left[ \frac{1}{2^{N}},\frac{2}{2^{N}}\right]$$so $f_{m}(0)=0$. Thus, $$|f_{n}(x)-f_{m}(x)|=1$$
For the second case, we take $x>0$. Using the Archimedean law consider an $N$ satisfying $1<2^{N}x$. 

Let $j_{n}=N$ and $$K_{n}=\{k\in \mathbb{N}:k<2^{N}x\}$$Since $1\in K_{n}$ and $K_{n}$ is a set of integers bounded by $2^{N}x$, let $k_{n}=\max K_{n}$. $1\in K_{n}$ implies that $k_{n}\ge1\ge0$. 

Suppose $k_{n}=2^{N}$. Since $k_{n}\le 2^{N}x$, $x=1$. If $k\in K_{n}$, then $k\in \mathbb{N}$ and $k<2^{N}$. So, $k\le2^{N}-1$. This contradicts that $k_{n}$ is an upper bound. Therefore, $k_{n}\ne 2^N$. Since $k\le 2^N$, $k<2^N$. Now, $k\in K_{n}$ implies $k\in \mathbb{N}$ so $k\le2^{N}-1$. This shows that $$n=2^{j_{n}}+k$$is in dyadic form with $$n\ge2^{N}\ge N$$

(EXPLAIN) There $k\in K_{n}$ such that $k+1\ge 2^{N}x$. Thus, $k_{n}\ge k\ge 2^{N}x-1$. So, $$k_{n}\le2^{j_{n}}x\le k_{n}+1$$which implies $$x\in\left[ \frac{k_{n}}{2^{j_{n}}}, \frac{k_{n}+1}{2^{j_{n}}}\right]\iff f_{n}(x)=1$$

Let $j_{m}=2N$ and let $k_{m}=k_{n}-1$. We still have $k_{m}\le 2^{N}-2\le2^{2N}-1=2^{j_{m}}-1$. Thus, $$m=2^{j_{m}}+k_{m}$$is in dyadic form with $$m\ge2^{2N}\ge N$$
We have $$x\ge \frac{k_{n}}{2^{N}}= \frac{k_{m}+1}{2^{N}}> \frac{k_{m}+1}{2^{N}}$$so, $$x\notin\left[\frac{k_{m}}{2^{j_{m}}}, \frac{k_{m}+1}{2^{j_{m}}}\right]\iff f_{m}(x)=0$$
Therefore, $$|f_{n}(x)-f_{m}(x)|=|1-0|=1$$
