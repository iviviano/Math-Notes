>[!1]

(a) 

Let $g\in\mathcal{S}(\mathbb{R};\mathbb{C})$. Pick $C\in \mathbb{R}$ such that $$
|g(t)|\le \frac{C}{|t|^{2}},\text{ for all }t\ne0
$$
In particular, we have $$
|g(n)|\le \frac{C}{n^{2}},\text{ for all }n\in \mathbb{N}
$$
$\frac{C}{n^{2}}$ is a $p$-series with $p=2>1$, so it converges. By the comparison test (REFERENCE), $g(n)$ is absolutely summable. Therefore, the sum in (\ref{eq_schwartz_sum}) converges.



Remark:
Lemma \ref{lm_schwartz_sum} immediately implies that both sides of (\ref{eq_poisson}) are summable. Let $f\in \mathcal{S}(\mathbb{R};\mathbb{C})$ and define $$f^{(-)}:\mathbb{R}\rightarrow \mathbb{C},~f^{(-)}(t)=f(-t)$$
Note that $f^{(-)}\in \mathcal{S}(\mathbb{R};\mathbb{C})$: $$
\left|t^{m}\cdot \frac{d^{n}f^{(-)}}{dt^{n}}(t)\right|= \left|t^{m}\cdot(-1)^{n} \frac{d^{n}f}{dt^{n}}(t)\right|<\infty
$$
Thus, by Lemma \ref{lm_schwartz_sum}, both of the series $$
\sum_{n=0}^{\infty}f(n),~\sum_{n=1}^{\infty}f^{(-)}(n)
$$
converge. Since $$
\sum_{n=-\infty}^{\infty}f(n)=\sum_{n=0}^{\infty}f(n)+\sum_{n=1}^{\infty}f^{(-)}(n)
$$we have the double sided series on the left side of (\ref{eq_poisson}) converges. For the right side, we note that $f\in\mathcal{S}(\mathbb{R};\mathbb{C})$ implies $\widehat f\in\mathcal{S}(\mathbb{R};\mathbb{C})$ (Fourier transform is a linear map on the class of Schwartz functions). 


(b)

(1) 


Let $K\subseteq \mathbb{R}$ be compact. We will to show that $$\begin{equation} %\label{eq_weier}
\sum_{n=-\infty}^{\infty}\|f_{n}\|_{\infty;K}=\sum_{n=0}^{\infty}\|f_{n}\|_{\infty;K}+\sum_{n=1}^{\infty}\|f_{-n}\|_{\infty;K}
\end{equation}$$converges. We first show the first term on the right-hand side is summable. Let $t_{0}=\min(K)$ by (EVT). Let $N\in \mathbb{N}$ such that $N>|t_{0}|+1$ by (A). Since $f$ is a Schwartz function, select $C\in \mathbb{R}$ with $$
|f(t)|\le \frac{C}{|t|^{2}},\text{ for all }t\ne0
$$
If $n\ge N$,
$$\begin{align*}
\|f_{n}\|_{\infty;K}&= \sup_{t\in K}|f(t+n)|\\
&\le \sup_{t\in K} \frac{C}{|\underbrace{t+n}_{>0}|^{2}} \\
&= \sup_{t\in K} \frac{C}{(t+n)^{2}}\\
&= \frac{C}{(t_{0}+n)^{2}}\\
&< \frac{C}{(n-N+1)^{2}}
\end{align*}$$
Thus, we have $\|f_{n}\|_{\infty;K}$ for $n\ge N$ is bounded by the terms of a convergent $p$ series for $p=2>1$. Thus, $$\sum_{n=0}^{\infty}\|f_{n}\|_{\infty;K}=\sum_{n=0}^{N-1}\|f_{n}\|_{\infty;K}+\sum_{n=N}^{\infty}\|f_{n}\|_{\infty;K}$$
converges.

In complete analogy, we can show the second series converges. Let $t_{0}=\max(K)$ by (EVT). Let $N\in \mathbb{N}$ such that $N>|t_{0}|+1$ by (A). Since $f$ is a Schwartz function, select $C\in \mathbb{R}$ with $$
|f(t)|\le \frac{C}{|t|^{2}},\text{ for all }t\ne0
$$
If $n\ge N$,
$$\begin{align*}
\|f_{-n}\|_{\infty;K}&= \sup_{t\in K}|f(t-n)|\\
&\le \sup_{t\in K} \frac{C}{|\underbrace{t-n}_{<0}|^{2}} \\
&= \sup_{t\in K} \frac{C}{(n-t)^{2}}\\
&= \frac{C}{(n-t_{0})^{2}}\\
&< \frac{C}{(n-N+1)^{2}}
\end{align*}$$
Thus, we have $\|f_{-n}\|_{\infty;K}$ for $n\ge N$ is bounded by the terms of a convergent $p$ series for $p=2>1$. Thus, $$\sum_{n=1}^{\infty}\|f_{n-}\|_{\infty;K}=\sum_{n=1}^{N-1}\|f_{n-}\|_{\infty;K}+\sum_{n=N}^{\infty}\|f_{-n}\|_{\infty;K}$$
converges. So, both terms of (\ref{eq_weier}) converge. Therefore, the series $$
\sum_{n=-\infty}^{\infty}f_{n}
$$
converges uniformly to $g$ by the Weierstrass $M$-test.


(2) 1-periodic:

For each $t\in \mathbb{R}$: 
$$\begin{align*}
g(t+1)&= \sum_{n=-\infty}^{\infty}f(t+1+n)\\
&= \sum_{n=1}^{\infty}f(t+1-n)+\sum_{n=0}^{\infty}f(t+1+n)\\
&= \sum_{n=0}^{\infty}f(t-n)+\sum_{n=1}^{\infty}f(t+n)\quad(\text{reindex}) %\label{eq_reindex}
\\
&= \sum_{n=-\infty}^{\infty}f(t+n)\\
&= g(t)
\end{align*}$$
We justify the reindexing of the infinite sum in (\ref{eq_reindex}) by: $$\begin{align*}
\sum_{n=1}^{\infty}f(t+1-n)&= \lim_{n \rightarrow \infty}\sum_{k=1}^{n}f(t+1-k)\\
&= \lim_{n \rightarrow \infty}\sum_{j=0}^{n-1}f(t-j)\quad(\text{reindex: }j=k-1)\\
&= \sum_{n=0}^{\infty}f(t-n)
\end{align*}$$
and similarly for the second term of (\ref{eq_reindex}). 

Note that by Lemma \ref{lm_cinfty}, $g$ is $\mathcal{C}^{\infty}$. In particular $g$ is Riemann integrable, so the Fourier coefficients are well-defined. We apply Theorem \ref{th_abott} in (\ref{eq_order_switch}) to compute the Fourier coefficients of $g$:
$$
\begin{align*}
\hat g_{n}&= \int_{- \frac{1}{2}}^{\frac{1}{2}}g(t)~e^{-2\pi int}\ dt\\
&= \int_{- \frac{1}{2}}^{\frac{1}{2}}\left(\sum_{k=-\infty}^{\infty}f(t+k)\right)~e^{-2\pi int}\ dt\\
&= \int_{- \frac{1}{2}}^{\frac{1}{2}}\left(\sum_{k=-\infty}^{\infty}f(t+k)~e^{-2\pi int}\right)\ dt\\
&= \sum_{k=-\infty}^{\infty}\left(\int_{- \frac{1}{2}}^{\frac{1}{2}}f(t+k)~e^{-2\pi int}\ dt\right)%\label{eq_order_switch}
\\
&= \sum_{k=-\infty}^{\infty}\int_{k- \frac{1}{2}}^{k+\frac{1}{2}}f(s)~e^{-2\pi ins}\cdot \underbrace{e^{2\pi ink}}_{=1}\ ds%\label{eq_int}
\\
&= \lim_{N \rightarrow \infty}\sum_{k=0}^{N}\int_{k- \frac{1}{2}}^{k + \frac{1}{2}}f(s)~e^{-2\pi ins}\ ds+\lim_{N \rightarrow \infty}\sum_{k=1}^{N}\int_{-k- \frac{1}{2}}^{-k + \frac{1}{2}}f(s)~e^{-2\pi ins}\ ds\\
&= \lim_{N \rightarrow \infty}\int_{-\frac{1}{2}}^{N + \frac{1}{2}}f(s)~e^{-2\pi ins}\ ds+\lim_{N \rightarrow \infty}\int_{-N- \frac{1}{2}}^{-\frac{1}{2}}f(s)~e^{-2\pi ins}\ ds\\
&= \int_{- \frac{1}{2}}^{\infty}f(s)~e^{-2\pi ins}\ ds+\int_{-\infty}^{- \frac{1}{2}}f(s)~e^{-2\pi ins}\ ds\\
&= \int_{-\infty}^{\infty}f(s)~e^{-2\pi ins}\ ds\\
&= \widehat f(n)
\end{align*}
$$
where $e^{2\pi ink}=1$ in (\ref{eq_int}) since $nk\in \mathbb{Z}$ and $e^{2\pi i x}=1\iff x\in\mathbb{Z}$.  


(c) 

We verify the hypotheses of Set 7, problem 3b: 

(1) We need that the series $\sum_{n=-\infty}^{\infty}f_{n}(t)$ converges for at least one point $x\in \mathbb{R}$. This follows from the uniform convergence of Part 1. 

(2) We need that for all compact sets $K$, the series of $k$-th derivatives is infinity norm summable on $K$: $$\begin{equation} %\label{eq_der_sum}
0\le\sum_{n=-\infty}^{\infty}\|f_{n}^{(k)}\|_{\infty;K}<\infty
\end{equation}$$
Since $f$ is a Schwartz function, all of its derivatives are Schwartz functions (Set 7, problem 4a). By the chain rule, $$
f_{n}^{(k)}(t)=f^{(k)}(t+n)
$$
So, for all $k\in \mathbb{N}$, (\ref{eq_der_sum}) follows immediately from part 1 of Lemma \ref{lm_b}.

Thus, the interchanging derivatives and series theorem implies that $g\in\mathcal{C}^{\infty}$. 


(d) 

By the Fourier series inversion property for $\mathcal{C}^{2}_{1}$ functions (Proposition 5.2.2 of [CM]), the Fourier series of $g$ converges uniformly to $g$. So for all $t\in \mathbb{R}$,
$$\begin{align*}
\sum_{n=-\infty}^{\infty}f(t+n)&= g(t)\\
&= \sum_{n=-\infty}^{\infty}\hat g_{n}~e^{2\pi int}\\
&= \sum_{n=-\infty}^{\infty}\widehat f(n)~e^{-2\pi int}
\end{align*}$$
The desired equality of (\ref{eq_poisson}) follows from the $t-0$ case.


>[!2]


Fix a $t\in \mathbb{R}$. By the Fourier Transform inversion property, we can write
$$\begin{align*}
f(t)&= \int_{-\infty}^{\infty}\widehat f(\nu)~e^{2\pi i \nu t}\ d\nu \\
&= \int_{-\infty}^{\infty} \underbrace{\frac{1}{1+|\nu|}}_{= \overline{ 1/1+|\nu|}}\cdot(1+|\nu|)\widehat f(\nu)e^{2\pi i \nu t}\ d \nu\\
&= \left\langle \frac{1}{1+|\nu|},(1+|\nu|)\cdot\widehat f(\nu)~e^{2\pi i \nu t}\right\rangle_{\mathcal{L}^{2}} %\label{eq_IP}
\end{align*}$$
where we can take the $\mathcal{L}^{2}$ inner product of the Schwartz function $(1+|\nu|)\cdot \widehat f(\nu)~e^{2\pi i \nu t}$ and the square integrable function $\frac{1}{1+|\nu|}$:
$$\begin{align*}
\left\| \frac{1}{1+|\nu|}\right\|_{\mathcal{L}^{2}}^{2}&= \int_{-\infty}^{\infty} \left|\frac{1}{1+|\nu|}\right|^{2}\ d \nu\\
&= \int_{-\infty}^{\infty} \frac{1}{(1+|\nu|)^{2}}\ d \nu %\label{eq_even}
\\
&= 2\int_{0}^{\infty} \frac{1}{(1+\nu)^{2}}\ d \nu\\
&= 2\lim_{R \rightarrow \infty} \left(\frac{-1}{1+\nu}\bigg|_{0}^{R}\right)\\
&= 2
\end{align*}
$$
where (\ref{eq_even}) uses the even symmetry of the integrand to remove the absolute value. Applying the Cauchy Schwarz inequality to the inner product in (\ref{eq_IP}), we have 
$$
\begin{align*}
\left|\left\langle \frac{1}{1+|\nu|},(1+|\nu|)\cdot\widehat f(\nu)~e^{2\pi i \nu t}\right\rangle_{\mathcal{L}^{2}}\right|\le \left\| \frac{1}{1+|\nu|}\right\|_{\mathcal{L}^{2}}\cdot \left\|(1+|\nu|)\cdot\widehat f(\nu)~e^{2\pi i \nu t}\right\|_{\mathcal{L}^{2}}
\end{align*}
$$
We compute the second norm factor:
$$\begin{align*}
\left\|(1+|\nu|)\cdot\widehat f(\nu)~e^{2\pi i \nu t}\right\|_{\mathcal{L}^{2}}^{2}&= \int_{-\infty}^{\infty}\left|\underbrace{(1+|\nu|)}_{>0}\cdot \widehat f(\nu)~e^{2\pi i \nu t}\right|^{2}\ d \nu\\
&= \int_{-\infty}^{\infty}\underbrace{(1+|\nu|)^{2}}_{\le4\max\{1,|\nu|^{2}\}}\cdot \left|\widehat f(\nu)\right|^{2}\cdot\underbrace{\left|e^{2\pi i \nu t}\right|^{2}}_{=1}\ d \nu\\
&\le 4\max\left\{\int_{-\infty}^{\infty}\left|\widehat f(\nu)\right|^{2}\ d \nu,\int_{-\infty}^{\infty}\left| \nu\cdot\widehat f(\nu)\right|^{2}\ d \nu,\right\}
\end{align*}$$
The first argument of the max is handled with Plancherel's identity for the Fourier Transform: 
$$\begin{align*}
\int_{-\infty}^{\infty}\left|\widehat f(\nu)\right|^{2}\ d \nu&= \int_{-\infty}^{\infty}\left|f(t)\right|^{2} \ dt=\|f\|_{\mathcal{L}^{2}}^{2}
\end{align*}$$
For the second term, we must first apply the Fourier Differentiation Mantra: 
$$\begin{align*}
\int_{-\infty}^{\infty}\underbrace{\left|\nu \cdot\widehat f(\nu)\right|}_{=\left| \frac{\widehat f'(\nu)}{2\pi i}\right|}\ ^{2}\ d \nu&= \frac{1}{2\pi}\int_{-\infty}^{\infty}\left|\widehat{f'}(\nu)\right|^{2}\ d \nu= \frac{1}{2\pi}\|f'\|_{\mathcal{L}^{2}}^{2}
\end{align*}
$$
where the second equality is Plancherel's identity for $f'$. We have shown$$
|f(t)|^{2}\le 8\max\left\{\|f\|^{2}_{\mathcal{L}^{2}}, \frac{1}{2\pi}\|f'\|_{\mathcal{L}^{2}}^{2}\right\}
$$Since $\sqrt{}$ is monotonic, taking $C=\sqrt{8}$ gives the desired relation (\ref{eq_sob}).  
