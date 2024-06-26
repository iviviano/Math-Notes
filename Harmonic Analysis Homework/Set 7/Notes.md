>[!1]

Let $0<\epsilon<\min\{a,1-b, \frac{b-a}{2}\}$ and define:
$$
f_{-}^{(\epsilon)}(t):=\begin{cases}
 0 & \text{if }x\in[0,a]\\
 \frac{x-a}{\epsilon} & \text{if }x\in[a,a+\epsilon]\\
 1 & \text{if }x\in[a+\epsilon,b-\epsilon] \\
\frac{b-x}{\epsilon} & \text{if }x\in[b-\epsilon,b] \\
0 & \text{if }x\in[b,1]
\end{cases}
$$
$$
f_{+}^{(\epsilon)}(t):=\begin{cases}
 0 & \text{if }x\in[0,a-\epsilon]\\
 \frac{x-a+\epsilon}{\epsilon} & \text{if }x\in[a-\epsilon,a]\\
 1 & \text{if }x\in[a,b] \\
\frac{b-x+\epsilon}{\epsilon} & \text{if }x\in[b,b+\epsilon] \\
0 & \text{if }x\in[b,1]
\end{cases}
$$

We see that $f_{+}^{(\epsilon)}$ and $f^{(\epsilon)}_{-}$ are the functions depicted in ...

Using geometric evaluation, the areas may be found$$\begin{align*}
\int_{0}^{1}f^{(\epsilon)}_{+}(x)-f(x)\ dx&= \int_{0}^{1}f^{(\epsilon)}_{+}(x)\ dx-\int_{0}^{1}f(x)\ dx\\
&= (b-a)+ \epsilon-(b-a)\\
&= \epsilon\\
\int_{0}^{1}f^{(\epsilon)}_{-}(x)-f(x)\ dx&= \int_{0}^{1}f^{(\epsilon)}_{-}(x)\ dx-\int_{0}^{1}f(x)\ dx\\
&= (b-a)-(b-a-\epsilon)\\
&= \epsilon
\end{align*}$$
showing (\ref{area_bound}).

(b)

We formulate \ref{t7.5} as a special case of \ref{t7.6}.
Let $$\chi_{I}(x)=\begin{cases}1,\text{if }x\in I \\
0,\text{if }x\notin I\end{cases}$$extended periodically. We may write: $$\frac{1}{n}\mathcal{N}_{n}(x,I)= \frac{1}{n}\sum_{n=0}^{n-1}\chi_{I}(x+k \alpha)$$and $$|I|=\int_{0}^{1}\chi_{I}(x)\ dx=\widehat{[x_{I}]}_{0}$$
Now, we prove \ref{t7.6} for the 1-periodic indicator function $f_{I}$.


$$\left|\widehat{[f_{I}]}_{0}-\widehat{[f_{\pm}^{(\epsilon)}]}_{0}\right|=\left|\int_{0}^{1}f_{I}(t)-f_{\pm}^{(\epsilon)}(t)\ dt\right|\le \epsilon$$

(c)

Extension of ... to 1-periodic real-valued step functions. We consider an arbitrary step function $f$ defined by $$f=\sum_{I\in A}a_{I}f_{I}$$where $A$ is a finite collection of intervals and $a_{I}\in\mathbb{R}$ for all $I\in A$, and $f_{I}$ denotes the 1-periodic extension of the indicator $\chi_{I}$. For any $x\in \mathbb{R}$,
$$\begin{align*}
\left| \frac{1}{n}\sum_{k=0}^{n-1}\sum_{I\in A}a_{I}f_{I}(x+k \alpha)-\widehat{\left[\sum_{I\in A}a_{I}f_{I}\right]}_{0}\right|&= \left| \sum_{I\in A}a_{I} \frac{1}{n}\sum_{k=0}^{n-1}f_{I}(x+k \alpha)-\sum_{I\in A}a_{I}\widehat{\left[f_{I}\right]}_{0}\right|\\
&= \left| \sum_{I\in A}a_{I} \left(\frac{1}{n}\sum_{k=0}^{n-1}f_{I}(x+k \alpha)-\widehat{\left[f_{I}\right]}_{0}\right)\right| \label{step_ex}
\end{align*}$$
where each term of the finite sum in (\ref{step_ex}) converges to 0 uniformly in $x$. Therefore, the Equidistribution Theorem holds for all real-valued 1-periodic step functions.


Note: we extend first to real valued Riemann integrable functions $f\in\mathcal{R}(\mathbb{R};\mathbb{R})$. 


Show there exist 1-periodic step functions $s_{\pm}^{(\epsilon)}$ such that $s^{(\epsilon)}_{-}\le f\le s_{+}^{(\epsilon)}$ and $$\left|\int_{0}^{1} \left(s_{\pm}^{(\epsilon)}(t)-f(t)\right)\ dt\right|\le \epsilon$$
Let $\epsilon>0$ be given. We first observe that for any partition of $[0,1]$, the upper and lower Riemann sums may be written as the integrals of step functions. By the definition of Riemann integrable, pick a partition $x_{0}<\cdots<x_{n}$ of $[0,1]$ such that 
 $$\sum_{i=0}^{n-1} (M_{i}-m_{i})(x_{i+1}-x_{i})<\epsilon$$
where $$\begin{align*}
M_{i}&:= \sup_{x\in[x_{i},x_{i+1}]}f(x),~0\le i<n\\
m_{i}&:= \inf_{x\in[x_{i},x_{i+1}]}f(x),~0\le i<n
\end{align*}$$
Define two step functions $$\begin{align*}
s^{(\epsilon)}_{+}(x)&:= \sum_{i=0}^{n-1}M_{i}\chi_{[x_{i},x_{i+1}]}(x)\ge f(x)\\
s^{(\epsilon)}_{-}(x)&:= \sum_{i=0}^{n-1}m_{i}\chi_{[x_{i},x_{i+1}]}(x)\le f(x)\\
\end{align*}$$
Observe that these step functions integrate to the Riemann sums: $$\begin{align*}
\int_{0}^{1}s_{+}^{(\epsilon)}(x)\ dx&= \sum_{i=0}^{n-1}M_{i}(x_{i+1}-x_{i})\\
\int_{0}^{1}s_{-}^{(\epsilon)}(x)\ dx&= \sum_{i=0}^{n-1}m_{i}(x_{i+1}-x_{i})\\
\end{align*}$$
Show both 
$$\left|\int_{0}^{1}\left(s_{\pm}^{(\epsilon)}(t)-f(t)\right)\ dt\right|\le \epsilon$$
and $$\left|\int_{0}^{1}\left(s_{\pm}^{(\epsilon)}(t)-s_{\mp}^{(\epsilon)}(t)\right)\ dt\right|\le \epsilon$$
FINISH THIS...

$$\begin{align*}
0\le\int_{0}^{1}s_{+}^{(\epsilon)}(t)-s_{-}^{(\epsilon)}(t)\ dt&= \int_{0}^{1}s^{(\epsilon)}_{+}(t)\ dt-\int_{0}^{1}s^{(\epsilon)}_{-}(t)\ dt\\
&= \sum_{i=0}^{n-1}M_{i}(x_{i+1}-x_{i})-\sum_{i=0}^{n-1}m_{i}(x_{i+1}-x_{i})\\
&= \sum_{i=0}^{n-1}(M_{i}-m_{i})(x_{i+1}-x_{i})\\
&< \epsilon\\
\end{align*}$$
So, $$\left|\int_{0}^{1}s_{-}^{(\epsilon)}(t)-s_{+}^{(\epsilon)}(t)\ dt\right|=\left|\int_{0}^{1}s_{+}^{(\epsilon)}(t)-s_{-}^{(\epsilon)}(t)\ dt\right|<\epsilon$$

$$\begin{align*}
0\le\int_{0}^{1}s_{+}^{(\epsilon)}(t)-\underbrace{f(t)}_{\ge s_{-}^{(\epsilon)}(t)}\ dt&\le \int_{0}^{1}s^{(\epsilon)}_{+}(t)\ dt-\int_{0}^{1}s^{(\epsilon)}_{-}(t)\ dt\\
&\le \left|\int_{0}^{1}s_{+}^{(\epsilon)}(t)-s_{-}^{(\epsilon)}(t)\ dt\right|\\
&< \epsilon\\
0\le \int_{0}^{1}\underbrace{f(t)}_{\le~s_{+}^{(\epsilon)}(t)}-s_{-}^{(\epsilon)}(t)~dt&\le \int_{0}^{1}s^{(\epsilon)}_{+}(t)\ dt-\int_{0}^{1}s^{(\epsilon)}_{-}(t)\ dt\\
&< \epsilon
\end{align*}$$
Giving $$\left|\int_{0}^{1}s_{\pm}^{(\epsilon)}(t)-f(t)~dt\right|<\epsilon$$



Then, estimate:

$$\begin{align*}
\left| \frac{1}{n}\sum_{k=0}^{n-1}f(x+k \alpha)-\hat f_{0}\right|&= \left| \frac{1}{n}\sum_{k=0}^{n-1}f(x+k \alpha) - \frac{1}{n}\sum_{k=0}^{n-1}s_{-}^{(\epsilon)}(x+k \alpha)+\frac{1}{n}\sum_{k=0}^{n-1}s_{-}^{(\epsilon)}(x+k \alpha)-\hat f_{0}\right|\\
&\le \left| \frac{1}{n}\sum_{k=0}^{n-1}f(x+k \alpha) - \frac{1}{n}\sum_{k=0}^{n-1}s_{-}^{(\epsilon)}(x+k \alpha)\right|+\left|\frac{1}{n}\sum_{k=0}^{n-1}s_{-}^{(\epsilon)}(x+k \alpha)-\hat f_{0}\right|\\
&\le \left| \frac{1}{n}\sum_{k=0}^{n-1}f(x+k\alpha)-s_{-}^{(\epsilon)}(x+k \alpha)\right|%\label{fs}
\\
&+ \left| \frac{1}{n}\sum_{k=0}^{n-1}s_{-}^{(\epsilon)}(x+k \alpha)-\widehat{[s_{-}^{(\epsilon)}]}_{0}\right|%\label{sset}
\\
&+\left|\widehat{[s_{-}^{(\epsilon)}]}_{0}-\hat f_{0}\right|%\label{fcs}
\end{align*}$$

Note that (\ref{ss}) converges to 0 uniformly by the version of Theorem \ref{et2} proven in class for continuous functions. For (\ref{fcs}), $$\left|\widehat{[s_{-}^{(\epsilon)}]}_{0}-\hat f_{0}\right|=\left|\int_{0}^{1}s_{-}^{(\epsilon)}(t)-f(t)\ dt\right|<\epsilon$$
We estimate (\ref{fs}):
$$\begin{align*}
\left| \frac{1}{n}\sum_{k=0}^{n-1}f(x+k\alpha)-s_{-}^{(\epsilon)}(x+k \alpha)\right|&= \frac{1}{n}\sum_{k=0}^{n-1}\underbrace{f(x+k\alpha)}_{\le~s_{+}^{(\epsilon)}(x+k \alpha)}-s_{-}^{(\epsilon)}(x+k \alpha)\\
&\le \frac{1}{n}\sum_{k=0}^{n-1} s_{+}^{(\epsilon)}(x+k \alpha)-s_{-}^{(\epsilon)}(x+k \alpha)\\
&= \left|\frac{1}{n}\sum_{k=0}^{n-1} s_{+}^{(\epsilon)}(x+k \alpha)-s_{-}^{(\epsilon)}(x+k \alpha)\right|\\
&\le \left| \frac{1}{n}\sum_{k=0}^{n-1}s_{+}^{(\epsilon)}(x+k \alpha)-\widehat{[s_{-}^{(\epsilon)}]}_{0}\right|\label{first}\\
&+\left|\widehat{[s_{+}^{(\epsilon)}]}_{0}-\widehat{[s_{-}^{(\epsilon)}]}_{0}\right|\label{something}\\
&+\left| \frac{1}{n}\sum_{k=0}^{n-1}s_{+}^{(\epsilon)}(x+k \alpha)-\widehat{[s_{-}^{(\epsilon)}]}_{0}\right|\label{last}
\end{align*}$$
Again, (\ref{first}) and (\ref{last}) go to zero uniformly in $x$ by the version of Theorem \ref{et2} proven in class for continuous functions. For (\ref{something}) gives,
$$\begin{align*}
\left|\widehat{[s_{+}^{(\epsilon)}]}_{0}-\widehat{[s_{-}^{(\epsilon)}]}_{0}\right|&= \left|\int_{0}^{1}s_{+}^{(\epsilon)}(t)-s_{-}^{(\epsilon)}(t)\ dt \right|\le \epsilon\\
&= \left|\int_{0}^{1}s_{+}^{(\epsilon)}(t)-f(t)\ dt+\int_{0}^{1}f(t)-s_{-}^{(\epsilon)}(t)\ dt \right|\\
&= \left|\int_{0}^{1}s_{+}^{(\epsilon)}(t)-f(t)\ dt\right|+\left|\int_{0}^{1}f(t)-s_{-}^{(\epsilon)}(t)\ dt \right|\\
&\le \epsilon+\epsilon
\end{align*}$$
so, we have proven

Extension to complex valued functions:
Let $f\in\mathcal{R}(\mathbb{R};\mathbb{C})$ be defined by $$f=h+ig$$for $h,g\in\mathcal{R}(\mathbb{R};\mathbb{R})$.

$$\begin{align*}
\left| \frac{1}{n}\sum_{k=0}^{n-1}f(x+k \alpha)-\hat f_{0}\right|&= \left| \frac{1}{n}\sum_{k=0}^{n-1}(h(x+k \alpha)+ig(x+k \alpha))-\widehat{[h-ig]}_{0}\right|\\
&= \left| \frac{1}{n}\sum_{k=0}^{n-1}h(x+k \alpha)-\hat h_{0}+ \frac{1}{n}\sum_{k=0}^{n-1}ig(x+k \alpha)-i\hat g_{0}\right|\\
&\le \left| \frac{1}{n}\sum_{k=0}^{n-1}h(x+k \alpha)-\hat h_{0}\right|+\left| \frac{1}{n}\sum_{k=0}^{n-1}g(x+k \alpha)-\hat g_{0}\right| \label{com_ex}
\end{align*}$$
where both terms of (\ref{com_ex}) converge to $0$ uniformly in $x$ as $n \rightarrow \infty$ by the Equidistribution Theorem for real-valued Riemann integrable functions.

>[!2]

(a)

(c)

Let $\phi:[0,\infty)\rightarrow [0,\infty)$ be defined by $$\phi(x):=e^{x}$$
Define $$f_{n}(t):=e^{-|n|}~e^{2\pi int},~t\in \mathbb{R}$$
Note that
$$\|f_{n}\|_{\infty}=e^{-|n|}$$


At $t=0$, $f_{n}(t)=e^{-|n|}$, for all $n\in\mathbb{Z}\setminus\{0\}$. So, $$\sum_{0\ne n=-\infty}^{\infty} \|f_{n}\|_{\infty}=\sum_{n=1}^{\infty}\|f_{-n}\|_{\infty}+\sum_{n=1}^{\infty}\|f_{n}\|_{\infty}=\sum_{n=1}^{\infty}e^{-n}+\sum_{n=1}^{\infty}e^{-n}$$
That $e^{-n}$ is summable follows from the comparison test. Since $\log$ is monotonic, 
$$\begin{align*}
&e^{-n}\le \frac{1}{n^{2}}\\
&\iff n^{2}\le~e^{-n}\\
&\iff n^{2}\le e^{n}\\
&\iff \log n^{2}\le \log e^{n}\\
&\iff 2\log n\le n
\end{align*}$$
Since $\sqrt{}$ is also a monotonic function, if $n\ge16$, $$2\log n=4\log \sqrt{n}\le \sqrt{n}\sqrt{n}=n$$
So, we see that $$e^{-n}\le \frac{1}{n^{2}}$$for all $n\ge 16$. Since $e^{-n}=|e^{-n}|$, and $\frac{1}{n^{2}}$ is a summable $p$-series we see that $e^{-n}$ is absolutely summable and thus summable. So, $$\sum_{0\ne n=-\infty}^{\infty}f_{n}$$converges uniformly in $x$ to a function $$f:=\sum_{0\ne n=-\infty}^{\infty}f_{n}$$

We use induction to show that $f\in\mathcal{C}^{\infty}$. The base case was just shown. Suppose that for some $k\ge0$, $f$ is $k$ times continuously differentiable with derivative $$\frac{d^{k}}{dx^{k}}f=f^{(k)}=\sum_{0\ne n=-\infty}^{\infty}f^{(k)}_{n}$$Note that this is equivalent to $f\in\mathcal{C}^{k}$.

We have that $$\sum_{0\ne n=-\infty}^{\infty}f_{n}^{(k)}$$converges point-wise everywhere per the inductive hypothesis.

We have $$f_{n}^{(k)}(t)=(2\pi i|n|)^{k}e^{-|n|}~e^{2\pi int}$$
For any closed interval $I$, $$\|f^{(k)}\|_{\infty;I}\le \|f^{(k)}\|_{\infty}=(2\pi |n|)^{k}e^{-|n|}$$
$$\sum_{0\ne n=-\infty}^{\infty} \|f^{(k)}_{n}\|_{\infty;I}=\sum_{n=1}^{\infty}\|f^{(k)}_{-n}\|_{\infty;I}+\sum_{n=1}^{\infty}\|f^{(k)}_{n}\|_{\infty;I}$$
Again, we use the comparison test to show that $f'$ is norm summable: 
$$\begin{align*}
(2\pi|n|)^{k}e^{-|n|}&\le \frac{1}{|n|^{2}}\\
&\iff (2\pi)^{k}|n|^{k+2}\le e^{|n|}\\
&\iff k\log2\pi+(k+2)\log|n|\le |n|
\end{align*}$$
Note that $\log 2\pi<\log|n|$ if $|n|\ge 2\pi$. Pick an integer $N>2\pi,(4k+2)^{4}$. Then, if $|n|\ge N$, 
$$\begin{align*}
k\log 2\pi+(k+2)\log |n|&\le (2k+2)\log|n|\\
&= (4k+4)\log \sqrt{|n|}\\
&\le \sqrt{|n|}\log \sqrt{|n|}\\
&\le \sqrt{|n|}\sqrt{|n|}\\
&= |n|
\end{align*}$$
So, we see that $$\|f^{(k)}_{n}\|_{\infty;I}\le|n|^{2}$$for all $n\ge N$. Thus, the double sided sequence of functions $f_{n}^{(k)}$ is norm summable under the supremum norm by the comparison test.

We have verified both hypotheses of Theorem \ref{thm_seriesderiv}. Thus, $$f^{(k)}:=\sum_{0\ne n=-\infty }^{\infty}f^{(k)}_{n}$$is a $\mathcal{C}^{1}$ function with $$f^{(k+1)}=\sum_{0\ne n=-\infty}^{\infty}f^{(k+1)}_{n}$$
Additionally, $f\in\mathcal{C}^{k+1}$.

By (PMI), we have $f\in\mathcal{C}^k$ for all $k\in \mathbb{N}_{0}$ and thus, $$f\in\mathcal{C}^{\infty}=\bigcap_{k=0}^{\infty}\mathcal{C}^{k}$$Consider the cohomological equation: 
$$\begin{equation}
f(x)-\hat f_{0}=h(x+ \alpha)-h(x)\label{cohom}
\end{equation}$$
We showed that $\{e^{-n}\}_{n\in \mathbb{N}}$ is summable. Thus, Proposition 7.5.2 of [CM] implies that there exists a function $g\in \mathcal{C}_{1}(\mathbb{R};\mathbb{C})$ with $\hat g_{0}=0$ and $$\hat g_{\pm}= \frac{1}{\phi(n)},~\text{for all }n\in \mathbb{N}$$and an irrational $\alpha$ such that the cohomological equation (\ref{cohom}) has no continuous solution $h$. We also note from the convergent Fourier series of $f$ that the function $f$ defined above has the same Fourier coefficients as $g$. By the uniqueness property, $f=g$. 

If $\alpha$ were Diophantine for some $r>0$, then Proposition 7.5.1 of [CM] would imply that for all $g\in\mathcal{C}_{1}^{l}(\mathbb{R};\mathbb{C})$ with $l>r+1$, the cohomological equation (\ref{cohom}) would have a continuous solution. That $f\in\mathcal{C}_{1}^{\infty}(\mathbb{R};\mathbb{C})\subseteq\mathcal{C}^{l}_{1}(\mathbb{R};\mathbb{C})$ with no continuous solution to (\ref{cohom}) implies that $\alpha\notin\mathcal{DC}(r)$ for any $r>0$. In particular, we have found $r\notin\mathcal{DC}$.

>[!3]

(b)

Prove
>[!thm]
>Given an [[Open Interval]] $I\subseteq \mathbb{R}$ and $\mathcal{C}^{1}-$[[Function]]s $f_{n}:I \rightarrow \mathbb{R}$, $n\in \mathbb{N}$, suppose that 
>1. The [[Series]] $\sum_{n=1}^{\infty}f_{n}(x)$ [[Converges (series)]] for at least one point $x\in I$
>2. For all [[Closed Set]] sub-intervals $[a,b]\subseteq I$, we have $$0\le\sum_{n=1}^{\infty}\|f_{n}'\|_{\infty;[a,b]}<\infty %\label{norm_sum}
>$$
>
>Then, $f(x)=\sum_{n=1}^{\infty}f_{n}(x)$ [[Uniform Convergence]] on all [[Compactness]] [[Subset]]s of $I$ with $$\frac{d}{dx}\sum_{n=1}^{\infty}f_{n}(x)=\sum_{n=1}^{\infty} \frac{df_{n}}{dx} $$


Note that any compact subset of $\mathbb{R}$ has a minimum and maximum by (EVT). For any compact subset $K$ of $I$, 
$$
K\subseteq[\min K,\max K]:=[a,b]
$$
Also,
$$
\|f'_{n}\|_{\infty;K}\le\|f'_{n}\|_{\infty'[a,b]}=:M_{n}
$$ By the second hypothesis (\ref{norm_bound}), the series $$\sum_{n=1}^{\infty}M_{n}<\infty$$So, the series $$
\sum_{n=1}^{\infty}f_{n}'
$$converges uniformly to $g\in\mathcal{B}(I,\mathbb{C})$ by the Weierstrass $M$-Test. 

Letting $$
\{g_{n}\}_{n\in \mathbb{N}_{0}}:=\left\{ \sum_{k=1}^{n}f_{n}\right\}_{n\in \mathbb{N}_{0}}
$$
we see that, the sequence $$
\{g_{n}'\}_{n\in \mathbb{N}_{0}}=\left\{  \frac{d}{dx}\sum_{k=1}^{n}f_{n}\right\}_{n\in \mathbb{N}_{0}}=\left\{ \sum_{k=1}^{n}f_{n}'\right\}_{n\in \mathbb{N}_{0}}
$$converges uniformly to $g$ on all compact subsets of $I$. 

By the first hypothesis, we have 
$$
g_{n}(x)=\sum_{k=1}^{n}f_{n}(x)\text{ converges for some }x\in I\label{con}
$$
Thus, the sequence $g_{n}$ satisfies both conditions of the "interchanging limits and derivatives" theorem. So, $g_{n}\rightarrow f$ uniformly on compact subsets of $I$ for some function $f:I \rightarrow \mathbb{R}$ satisfying $f'=g$. We see that $f=\sum_{n=1}^{\infty}f_{n}$ from (\ref{con}). And, $$
\frac{d}{dx}\sum_{n=1}^{\infty}f_{n}=f'=g=\sum_{n=1}^{\infty}f_{n}'=\sum_{n=1}^{\infty} \frac{df_n}{dx}
$$


>[!4]

(a) 

Vector subspace: Let $f,g\in\mathcal{S}(\mathbb{R};\mathbb{C})$ and $a,b\in \mathbb{C}$ and $m,n\in \mathbb{N}_{0}$. Let $C_{m,n}$ and $D_{m,n}$ be the Schwartz constants of $f$ and $g$, respectively. We see: 
$$\begin{align*}
\sup_{x\in\mathbb{R}}\left|x^{m}(af^{(n)}(x)+bg^{(n)}(x))\right|&= \sup_{x\in\mathbb{R}}\left|ax^{m}f^{(n)}(x)+bx^{m}g^{(n)}(x))\right|\\
&\le \sup_{x\in\mathbb{R}}a\left|x^{m}(f^{(n)}(x)\right|+b\sup_{x\in\mathbb{R}}\left|g^{(n)}(x))\right| %\label{te_sup}\\
\\&= aC_{m,n}+bD_{m,n}\\
&< \infty
\end{align*}$$so, $af+bg\in\mathcal{S}(\mathbb{R};\mathbb{C})$. Note that (\ref{te_sup}) uses the triangle inequality and positive homogeneity for the supremum norm. 

Clearly, $0\in\mathcal{S}(\mathbb{R};\mathbb{C})$ with $C_{m,n}=0$ for all $m,n\in \mathbb{N}_{0}$. 

any other things for vector subspace?

Closed under multiplication:

Repeated applications of the product rule show:
$$\begin{align*}
(f\cdot g)^{(n)}=\sum_{k=0}^{n}\binom{n}{k}f^{(k)}g^{(n-k)}\\
\end{align*}$$
$$\begin{align*}
\sup_{x\in \mathbb{R}}\left|x^{m}(f\cdot g)^{(n)}(x)\right|&= \sup_{x\in \mathbb{R}}\left|x^{m}\sum_{k=0}^{n}\binom{n}{k}f^{(k)}(x)g^{(n-k)}(x)\right|\\
&\le \sum_{k=0}^{n}\binom{n}{k}\sup_{x\in \mathbb{R}}\left|x^{m}f^{(k)}(x)g^{(n-k)}(x)\right|\\
&\le \sum_{k=0}^{n}\binom{n}{k}\sup_{x\in \mathbb{R}}\left|x^{m}f^{(k)}(x)\right|\cdot\sup_{x\in \mathbb{R}}\left|g^{(n-k)}(x)\right|\\
&= \sum_{k=0}^{n}\binom{n}{k}C_{m,k}\cdot D_{0,n-k}\\
&< \infty %\label{finite}
\end{align*}$$
where (\ref{finite}) is finite since it is a finite sum.


[[Function]] is [[Schwartz Function]] [[implies]] derivative is [[Schwartz Function]]:

Let $f\in\mathcal{S}(\mathbb{R};\mathbb{C})$ have Schwartz constants $C_{m,n}$. For a fixed $k\in \mathbb{N}$, and any $n,m\in \mathbb{N}_{0}$, let $[f^{(k)}]^{(n)}$ denote the $n$-th derivative of the $k$-th derivative of $f$. We have $$\sup_{x\in \mathbb{R}}\left|x^{m}[f^{(k)}]^{(n)}\right|=\sup_{x\in \mathbb{R}}\left|x^{m}f^{(k+n)}(x)\right|=C_{m,n+k}<\infty$$showing that $f^{(k)}\in\mathcal{S}(\mathbb{R};\mathbb{C})$.


(b)

Let $f:\mathbb{R}\rightarrow \mathbb{R}$ be defined by $$f(x)=e^{-\pi x^{2}}$$



Claim: all derivatives of $f$ are of the form $$p(x)e^{-\pi x^{2} }$$
Induction: Let $P(k)$ be that the $k$-th derivative of $f$ is of the form $$
f^{(k)}(x)=p_{k}(x)e^{-\pi x^{2}}
$$for some polynomial $p_{k}$. 

Base case: $k=0$
Taking $p_{0}(x)=1$, we see that $P(0)$ holds.

Inductive Step: Suppose for some $k\ge0$, $P(k)$ holds for a polynomial $p_{k}(x)=\sum_{i=0}^{n_{k}}a_{i}x^{i}$. 

We compute the $(k+1)$-st derivative of $f$:
$$\begin{align*}
\frac{d}{dx}\left(p_{k}(x)e^{-\pi x^{2}}\right)&= \frac{d}{dx}\sum_{i=0}^{n_{k}}a_{i}x^{i}e^{-\pi x^{2}}\\
&= \sum_{i=0}^{n_{k}} \frac{d}{dx}\left(a_{i}x^{i}e^{-\pi x^{2}}\right)\\
&= \sum_{i=0}^{n_{k}}ia_{i}x^{i}e^{-\pi x^{2}}-2a_{i}x^{i+1}e^{-\pi x^{2}}\\
&= \left(\sum_{i=0}^{n_{k}}ia_{i}x^{i}-2a_{i}x^{i+1}\right)e^{-\pi x^{2}}\\
&:= p_{k+1}(x)e^{-\pi x^{2}}
\end{align*}$$
showing $P(k+1)$.

Thus, by (PMI), $P(k)$ holds for all $k\in \mathbb{N}_{0}$. 



Fix $n\in \mathbb{N}_{0}$ and examine the $n$-th derivative of $f$: $$
f^{(n)}(x)=p_{n}(x)e^{-\pi x^{2}}
$$with $p_{n}$ degree $k$.

Pick $x_{0}\in \mathbb{R}$ such that for for all $x\notin[-x_{0},x_{0}]$, $$|p_{n}(x)|\le |x^{k+1}|$$
and $x_{0}\ge m+k+1$.

Note that we can do (\ref{polybound}) since for all $|x|\ge1$, 
$$\begin{align*}
\left|\sum_{i=0}^{N}a_{i}x^{i}\right|&\le \sum_{i=0}^{N}|a_{i}|\cdot|x|^{i}\\
&\le \sum_{i=0}^{N}|a_{i}|\cdot|x|^{N}\\
&= |x|^{N}\sum_{i=0}^{N}|a_{i}|
\end{align*}$$
So, if we also require $|x|\ge\sum_{i=0}^{N}|a_{i}|$, (\ref{polybound}) holds.

Since $\log$ is monotonic, we have $$\begin{align*}
x^{m+k+1}e^{-\pi x^{2}} &\le  1\\
\iff x^{m+k+1}&\le e^{\pi x^{2}}\\
\iff\log x^{m+k+1}&\le \log e^{\pi x^{2}}\\
\iff(m+k+1)\log x&\le \pi x^{2}
\end{align*}$$
For a fixed $x\notin[-x_{0},x_{0}]$, $|x|\ge m+k+1$ and $\log |x|\le |x|$. So we have 
$$\begin{align*}
(m+k+1)\log |x|&\le (m+k+1)\cdot|x|\\
&\le (m+k+1)^{2}\\
&\le |x|^{2} %\label{mono}
\\&\le \pi x^{2}
\end{align*}$$
where (\ref{mono}) is true because $y^{2}\le z^{2}\iff y\le z$ for all $y,z\in \mathbb{R}$. So, we have indeed have that $$x^{m+k+1}e^{-\pi x^{2}}\le1$$for all $x\notin[-x_{0},x_{0}]$.

Then for any $m\in \mathbb{N}_{0}$,
$$\begin{align*}
\sup_{x\notin [-x_{0},x_{0}]}\left|x^{m}f^{(n)}(x)\right|&= \sup_{x\notin [-x_{0},x_{0}]}\left|x^{m}p_{n}(x)e^{-\pi x^{2}}\right|\\
&\le \sup_{x\notin [-x_{0},x_{0}]}\left|x^{m}x^{k+1}e^{-\pi x^{2}}\right|\\
&= \sup_{x\notin [-x_{0},x_{0}]}\left|x^{m+k+1}e^{-\pi x^{2}}\right|\\
&\le1
\end{align*}$$
We also have the continuous function $x^{m}f^{(n)}(x)$ is bounded on the compact domain $[-x_{0},x_{0}]$ by the (EVT). Therefore, there exists $$C_{m,n}:=\sup_{x\in \mathbb{R}}\left|x^{m}f^{(n)}(x)\right|$$
