>[!1]

$$\begin{equation} %\label{cohom}
h(x+ \alpha)-h(x)=f(x)-\hat f_{0}
\end{equation}$$

>[!prop]
Let $\phi:(0,\infty)\rightarrow (0,\infty)$ be a strictly increasing function which satisfies $$\sum_{n=1}^{\infty} \frac{1}{\phi(n)}<+\infty$$Then, there exists a 1-periodic, continuous function $f\in\mathcal{C}_{1}(\mathbb{R};\mathbb{R})$ with $\hat f_{0}=0$ and $$\hat f_{\pm n}= \frac{1}{\phi(n)},\text{ for all }n\in \mathbb{N}$$and an irrational $\alpha\in \mathbb{R}$ so that the cohomological equation (\ref{cohom}) has no continuous solution $h$.


Since $\phi$ maps into $(0,\infty)$, $$\left\|\frac{1}{\phi(n)}e_{\pm n}\right\|_{\infty}= \left\| \frac{1}{\phi(n)}\right\|_{\infty}= \frac{1}{\phi(n)}$$
Since $\frac{1}{\phi(n)}$ is summable, the Weierstrass $M$-test implies that the Fourier series $$\sum_{n=-\infty}^{\infty} \frac{1}{\phi(|n|)}e_{n}$$converges uniformly. Defining $$f:=\sum_{n=-\infty}^{\infty} \frac{1}{\phi(|n|)}e_{n}$$
we see that $$\hat f_{\pm n}= \frac{1}{\phi(n)}$$


Goal: find a subsequence of the digits $(x_{n})_{n\in \mathbb{N}}$ so that along some subsequence $(x_{n_{k}})_{k\in \mathbb{N}}$, one has $$|1-e^{2\pi in_{k}\alpha}|\le \frac{1}{{\phi(n_{k})}}=\hat f_{n_{k}},\text{ for all }k\in \mathbb{N}$$

Define two mutually recursive sequences $\{n_{k}\}_{k\in\mathbb{N}}$ and $\{b_{k}\}_{k\in \mathbb{N}}$: 
$$\begin{align*}
b_{1}&:= 1\\
n_{k}&:= 10^{b_{k}}\\
b_{k+1}&:= \min\left(\{l\in \mathbb{N}: \frac{4\pi}{10^{l}}\le \frac{1}{\phi(n_{k})}\}\setminus \{b_{1},\ldots,b_{k-1}\}\right)
\end{align*}$$
For each $k\in \mathbb{N}$, let 
$$\begin{align*}
&x_{b_{k}}:= 1\\
&x_{b_{k}+1},\ldots,x_{b_{k+1}-1}:=0
\end{align*}$$
Define $$
\begin{equation}
\alpha:=\sum_{k=0}^{\infty} \frac{x_{k}}{10^{k}}
\end{equation}$$
We have for each $k$, $$\left| \frac{x_{k}}{10^{k}}\right|\le \left| \frac{1}{10^{k}}\right|$$Since $\frac{1}{10^{k}}$ is a geometric series with radius less than 1, it converges absolutely. Thus, the series in (\ref{alpha}) converges to $\alpha$ by the comparison test. Note also that we may write the decimal expansion of $\alpha$ as $$\alpha=x_{0}.x_{1}x_{2}\ldots$$
Noting that all of the $b_{k}$'s are unique, we see that $\alpha$ is irrational since it never terminates or repeats. 

We estimate
$$\begin{align*}
n_{k}\alpha\mod1&= 10^{b_{k}}\sum_{l=0}^{\infty} \frac{x_{l}}{10^{l}}\mod1\\
&= \left(\underbrace{\sum_{l=0}^{\infty}10^{b_{k}-l}x_{l}}_{\in \mathbb{N}} -\underbrace{\sum_{l= b_{k}+1}^{\infty} \frac{x_{l}}{10^{l-b_{k}}}}_{<1}\right)\mod1\\
&= \sum_{l=b_{k}+1}^{\infty} \frac{x_{l}}{10^{l-b_{k}}}\\
&= \sum_{l=b_{k}+1}^{b_{k+1}} \frac{x_{l}}{10^{l-b_{k}}}+\sum_{l=b_{k+1}+1}^{\infty} \frac{x_{l}}{10^{l-b_{k}}}\\
&\le \sum_{l=b_{k}+1}^{b_{k+1}} \frac{x_{l}}{10^{l-b_{k}}}+ \frac{1}{10^{b_{k}+1}}
\\&= \frac{2}{10^{b_{k+1}}}
\end{align*}$$




Noting that we can associate $e^{2\pi in_{k}\alpha}$ with the rotation angle $n_{k}\alpha$. As shown in Figure \ref{geom_arg}, we estimate $|1-e^{2\pi in_{k}\alpha}|$ by the rotation map, since the straight-line distance between the points $1$ and $e^{2\pi in_{k}\alpha}|$ will always be less than the distance around the circle (of circumference $2\pi$). Thus, 
$$\begin{align*}
|e^{2\pi in_{k} \alpha}-1|&\le  2\pi (n_{k} \alpha-1\mod1)\\
&= 2\pi(n_{k}\alpha\mod1)\\
&\le 2\pi\cdot \frac{2}{10^{b_{k+1}}}\\
&\le \frac{1}{\phi(n_{k})}
\end{align*}$$ 

If $h$ were a continuous solution to (\ref{cohom}), we have 
$$\hat h_{n}:=\begin{cases} \frac{\hat f_{n}}{e^{2\pi in \alpha}-1} & \text{ if }n≠0\\
\text{const} & \text{ if }n=0
\end{cases}$$
In particular, we have $$\begin{equation} %\label{FC_lower}
|\hat h_{n_{k}}|= \frac{\left|\hat f_{n_{k}}\right|}{|1-e^{2\pi in_{k}\alpha}|}\ge 1,~\text{for all }k\in \mathbb{N}
\end{equation}$$
The Riemann Lebesgue lemma implies that $\hat h_{n}\rightarrow 0$ as $n \rightarrow \infty$. But any subsequence of a convergent subsequence converges to the same value. (\ref{FC_lower}) implies that $\hat h_{n_{k}}\not\to0$. This contradicts the Riemann-Lebesgue lemma, showing that there is no continuous solution $h$ to (\ref{cohom}) for the $\alpha$ chosen.

>[!2]

(b)

Corollary 8.1.1 states that the [[Approximate Return Time]]s are determined by the [[Sequence]] of denominators of the [[Continued Fraction Approximant]]s of $\alpha$.

Prove:

>[!thm]
For a fixed irrational $\alpha\in \mathbb{R}\setminus\mathbb{Q}$, let $\frac{p_{n}}{q_{n}}$ be the sequence of convergents in the continued fraction expansion of $\alpha$. Given $M\in \mathbb{N}$, let $n_{M}\in \mathbb{N}$ be the unique natural number such that $$q_{n_{M}}\le M< q_{n_{M}+1}$$Then, one has $$
\begin{equation} \label{approx_ret}
\|\alpha\cdot q_{n_{M}}\|=\min_{1\le k\le M}\|\alpha\cdot k\|
\end{equation}$$in particular, for all $n\in \mathbb{N}$, $$\|\alpha\cdot q_{n}\|=\min_{1\le k<q_{n+1}}\|\alpha\cdot k\|$$

Show that $n_M$ exists and is unique:

Let $M\in \mathbb{N}$ be given. Let $A=\{k\in \mathbb{N}_{0}:q_{k}\le M\}$

Note that $A\subseteq \mathbb{N}$ is nonempty (it contains $q_{0}=1$) and bounded (by $M$). Thus, it has a maximum:
$$n_{M}:=\max A$$
We have $n_{M}\in A$ and thus, $$q_{n_{M}}\le M$$
That $n_{M}$ is the maximum of $A$ implies $n_{M}+1\notin A$. So, $q_{n_{M}+1}\not\le M\iff M<q_{n_{M}}$. 

If $k<n_{M}$, $$q_{k+1}\le q_{n_{M}}\le M$$so, $$q_{k+1}\not>M$$
If $k>n_{M}$, $$q_{k}\ge q_{n_{M}+1}>M$$so, $$q_{k}\not\le M$$
So, we have shown the existence and uniqueness of $n_{M}$. 

From Corollary 8.1.1, $q_{n_{M}}$ and $q_{n_{M}+1}$ are approximate return times and for all $q_{n_{M}}< k<q_{n_{M}+1}$, $k$ is not an approximate return time. If (\ref{approx_ret}) were false, we would have 
$$\|\alpha\cdot q_{n_{M}}\|>\|\alpha\cdot k_{0}\|=\min_{1\le k\le M}\|\alpha\cdot k\|$$
for some $1\le k_{0}\le M$ with $k_{0}\ne q_{n_{M}}$. Consider two cases. If $k_{0}<q_{n_{M}}$, this contradicts that $q_{n_{M}}$ is BA-2. Otherwise, $k_{0}>q_{n_{M}}$. So, $$\|\alpha\cdot k_{0}\|=\min_{1\le k\le M}\|\alpha\cdot k\|=\min_{1\le k\le k_{0}}\|\alpha\cdot k\|$$
which implies that $k_{0}$ is an approximate return time. Since the sequence of denominators $q_{n}$ is monotonic and $q_{n_{M}}<k_{0}<q_{n_{M}+1}$, we have contradicted Corollary 8.1.1, so (\ref{approx_ret}) holds.

Fix $n\in \mathbb{N}$ and let $M=q_{n+1}-1$. Note that taking $n_{M}=n$, we have $$q_{n_{M}}\le q_{n_{M}+1}-1=M$$since the $n_{M}$ satisfying this is unique for a given $M$, we have 
$$\|\alpha\cdot q_{n_{M}}\|=\min_{1\le k\le M}\|\alpha\cdot k\|$$which we may rewrite as $$\|\alpha\cdot q_{n}\|=\min_{1\le k< q_{n+1}}\|\alpha\cdot k\|$$

>[!3]


(a)

$$h:\mathbb{R}\rightarrow \mathbb{R},~h(x)=\begin{cases}e^{- \frac{1}{x^{2}}} & \text{if }x\ne0 \\
0 & \text{if }x=0\end{cases}$$
Show that $h$ is $\mathcal{C}^{\infty}$. 

Let $P(n)$ be that $$h^{(n)}(x)=p_{n}\left(\frac{1}{x}\right)\cdot e^{-\frac{1}{x^{2}}},~\text{for all }x>0$$with $h^{(n)}(0)=0$ for some polynomial $p_{n}$.

Base case: $n=0$. 
Let $p_{0}=1$. We get $$h^{(0)}(x)=1\cdot h(x)=h(x),~\text{for all }x>0$$
For $x=0$, the definition of $h$ gives $$h^{(0)}(0)=h(0)=0$$

Inductive Step: Suppose $P(n)$ holds for some $n\ge0$ for a polynomial $p_{n}=\sum_{k=0}^{n_{k}}a_{k}x^{k}$. 

For $x>0$, $$\begin{align*}
h^{(n+1)}(x)&= \frac{d}{dx}h^{(n)}(x)\\
&= \frac{d}{dx} \left(p_{n}\left(\frac{1}{x}\right)e^{- \frac{1}{x^{2}}}\right)\\
&= \frac{d}{dx} \left(\sum_{k=0}^{n_{k}}a_{k}x^{-k}~e^{-\frac{1}{x^{2}}}\right)\\
&= \sum_{k=0}^{n_{k}} a_{k}\frac{d}{dx}\left( x^{-k}~e^{-\frac{1}{x^{2}}}\right)\\
&= \sum_{k=0}^{n_{k}} a_{k}\left( -kx^{-k-1}~e^{-\frac{1}{x^{2}}}+x^{-k}e^{- \frac{1}{x^{2}}}\cdot \frac{d}{dx} \left(\frac{-1}{x^{2}}\right)\right)\\
&= \sum_{k=0}^{n_{k}} a_{k}\left( -kx^{-k-1}~e^{-\frac{1}{x^{2}}}+x^{-k}e^{- \frac{1}{x^{2}}}\cdot \frac{2}{x^{3}}\right)\\
&= \sum_{k=0}^{n_{k}} a_{k}\left(-kx^{-k-1}~e^{-\frac{1}{x^{2}}}+x^{-k}e^{- \frac{1}{x^{2}}}\cdot \frac{2}{x^{3}}\right)\\
&= \sum_{k=0}^{n_{k}} a_{k}\left(-k \left(\frac{1}{x}\right)^{k+1}~e^{-\frac{1}{x^{2}}}+2\left(\frac{1}{x}\right)^{k+3}e^{- \frac{1}{x^{2}}}\right)\\
&= e^{- \frac{1}{x^{2}}}\sum_{k=0}^{n_{k}} a_{k}\left(-k \left(\frac{1}{x}\right)^{k+1}+2\left(\frac{1}{x}\right)^{k+3}\right)\\
&:= e^{- \frac{1}{x^{2}}}p_{n+1}\left(\frac{1}{x}\right)
\end{align*}$$


At $x=0$, 

$$h^{(n+1)}(0)=\lim_{x \rightarrow 0} \frac{h^{(n)}(x)-h^{(n)}(0)}{x-0}=\lim_{x \rightarrow 0} \frac{h^{(n)}(x)}{x}$$
Since $$\begin{align*}
&\lim_{x \rightarrow 0}h^{(n)}(x)\rightarrow 0\\
&\lim_{x \rightarrow 0}x\rightarrow 0
\end{align*}$$by the inductive hypothesis, the rule de l'Hopital says that this is indeed the limit: $$h^{(n+1)}(0)=\lim_{x \rightarrow 0} \frac{\frac{d}{dx}h^{(n)}(x)}{\frac{d}{dx}x}=\lim_{x \rightarrow 0} \frac{h^{(n+1)}(x)}{1}=\lim_{x\rightarrow 0}h^{(n+1)}(x)$$Note that $h^{(n)}$ differentiable for all $x>0$ was shown above, and this is what we need to compute the limit. 

On set 7, problem 4, we showed that $$x^{m}e^{- x^{2}}\rightarrow 0\text{ as }x \rightarrow \infty,\text{ for all }m\in \mathbb{N}_{0}$$
Consider an arbitrary term $b_{k}x^{k}$ of $p_{n+1}$. Let $\epsilon>0$ be given and pick $x_{0}$ such that for all $x>x_{0}$, $$|x^{k}e^{- x^{2}}|< \frac{\epsilon}{b_{k}}$$
If $0<x< \frac{1}{x_{0}}$, then, $$\frac{1}{x}>x_{0}$$and $$\left|b_{k} \left(\frac{1}{x}\right)^{k}e^{- \frac{1}{x^{2}}}\right|<\epsilon$$Thus, we see that each term of $p_{n+1}(x)e^{- \frac{1}{x^{2}}}\rightarrow 0$ as $x \rightarrow 0$ and thus $$h^{(n+1)}(x)= p_{n+1}(x)e^{- \frac{1}{x^{2}}}\rightarrow 0,\text{ as }x \rightarrow 0$$
This concludes the inductive step.

By (PMI), we have $P(n)$ for all $n\in \mathbb{N}_{0}$. 



(b)

$$g(x):= \frac{h(x)}{h(x)+h(1-x)}$$
Show that $g\in\mathcal{C}^{\infty}(\mathbb{R};\mathbb{R})$ which satisfies $0\le g\le 1$ and $g(x)=0$ if $x\le0$ and $g(x)=1$ if $x\ge1$. 

Recall the product rule:

$$\begin{align*}
(f\cdot g)^{(n)}=\sum_{k=0}^{n}\binom{n}{k}f^{(n-k)}g^{(k)}\\
\end{align*}$$


Let $f:\mathbb{R}\rightarrow \mathbb{R}$ be defined by $$f(x):=h(x)+h(1-x)$$so we have $g(x)= \frac{h(x)}{f(x)}$. 

Let $P(n)$ be that $g\in\mathcal{C}^{n}$. 

Base case: 

Note that $h(x)$ is 0 if and only if $x=0$. Also, $h$, is non-negative. Thus, $h(x)=-h(1-x)$ is false for all $x$ and $f$ is nonzero.

Since $f$ is nonzero and continuous, the quotient $h$ is continuous, by the algebra of continuous functions. This shows $P(0)$.

Inductive Step: Suppose $P(n)$ for some $n-1\ge0$. 

We have $g^{(k)}$ is continuous for all $k\le n-1$. Note that $f^{(k)}$ and $h^{(k)}$ are also continuous for all $k$ by part (a). 

Write $h= g\cdot f$ and apply the product rule:
$$\begin{align*}
h^{(n)}&= (f\cdot g)^{(n)}\\
&= \sum_{k=0}^{n}\binom{n}{k}f^{(n-k)}g^{(k)}\\
&= f\cdot g^{(n)}+\sum_{k=0}^{n-1}\binom{n}{k}f^{(n-k)}g^{(k)}\\
\iff g^{(n)}&= \frac{h^{(n)}-\sum_{k=0}^{n-1}\binom{n}{k}f^{(n-k)}g^{(k)}}{f}
\end{align*}$$
where we can divide by $f$ in the last step since it is nonzero. Thus, the algebra of continuous functions implies that $g^{(n)}$ is continuous. So, $g\in\mathcal{C}^{n}$.

By (PMI), we have $g\in\mathcal{C}^{\infty}$.








(c)


$$\chi_{\delta}(x):=\begin{cases} 
 0 & \text{if }t\notin(-1-\delta,1+\delta) \\
1 & \text{if }t\in[-1,1] \\
g\left(\frac{1+\delta-x}{\delta}\right) & \text{if }t\in(1,1+\delta) \\
g\left(\frac{x+1+\delta}{\delta}\right) & \text{if }t\in(-1-\delta,-1)
\end{cases}$$

For all $t\in[-1,1]$, $$\chi_{\delta}(t)=1$$
For all $t\notin(-1-\delta,1-\delta)$, $$\chi_{\delta}(t)=0$$
If $1<t<1+\delta$, $$0<\frac{1+\delta-t}{\delta}<1$$
So, $$0<g(t)<1$$
If $-1-\delta<t<-1$, $$0< \frac{x+1+\delta}{\delta}<1$$So, $$0<g(t)<1$$


Obviously, $\chi_{\delta}$ is $\mathcal{C}^{\infty}$ except possibly at $t=-1-\delta,-1,1,1+\delta$. Noting that $\chi_{\delta}$ is even, we consider $t=1,1+\delta$. 

At $t=1$, for all $n>0$, the left limit of $\chi_{\delta}^{(n)}$ is $0$, since $\chi_{\delta}$ is constant left of 1. The right limit is also 0, since we have $$\frac{1+\delta-1}{\delta}=1$$and, b implies that $g^{(n)}$ is 0 at 1. For $n=0$, $\chi_{\delta}$ is uniformly 1 to the right of 1 (and at 1). Also, $g(1)=1$.

At $t=1+\delta$, for all $n>0$, the left limit of $\chi_{\delta}^{(n)}$ is 0, since we have $$\frac{1+\delta-1-\delta}{\delta}=0$$and, $b$ implies that $g^{(n)}$ is 0 at $0$. The right limit is 0, since $\chi_{\delta}$ is constant right of $1+\delta$. For $n=0$, $\chi_{\delta}$ is uniformly 0 to the right of $1+\delta$. Also, $g(0)=0$.


>[!4]


(b)

Suppose that every gap has length either $g_{m}$ or $2g_{m}$. We first show that $g_{m}$ must be rational.
$$\begin{align*}
\sum_{k=1}^{n}g_{k}&= 1+b_{1}-b_{n}+\underbrace{\sum_{k=2}^{n}b_{k}-b_{k-1}}_{\text{telescopes}}\\
&= 1+b_{1}-b_{n} -b_{1}+b_{n}\\
&= 1
\end{align*}$$
Note also that each $g_{k}$ is an integer multiple of $g_{m}$. In particular, there exists $k\in \mathbb{N}$ such that $$1=\sum_{k=1}^{n}g_{k}=kg_{m}$$So, $$g_{m}= \frac{1}{k}\in\mathbb{Q}$$

Consider two cases: 
Case 1: $b_{n}$ is the first iterate corresponding to the fractional part of $1\alpha$. Then, $b_{n}=\alpha$. Since $n>1$, we have some $k<n$ such that $$b_{n}+\alpha= b_{k}(\mod1)$$Note that since $b_{k}<b_{n}$, $$b_{n}+\alpha-1=b_{k}\iff b_{n}-b_{k}=1-\alpha$$
For the points in between $b_{k}$ and $b_{n}$, we count the number of each distance: 
$$\begin{align*}
l:=&\#\{i:k\le i<n,~b_{i+1}-b_{i}=g_{m}\}\\
j:=&\#\{i:k\le i<n,~b_{i+1}-b_{i}=2g_{m}\}
\end{align*}$$
As in part b, a telescoping sum argument shows that the total distance between $b_{k}$ and $b_{n}$ is given by $$1-\alpha=b_{n}-b_{k}=lg_{m}+2jg_{m}$$
Thus, $$1-\alpha=(\underbrace{l+2j}_{\in\mathbb{Q}})g_{m}$$and so $\alpha\in \mathbb{Q}$ by the closure of $\mathbb{Q}$ under multiplication and addition.


Case $2$: $b_{n}$ is not the first iterate. Then, $b_{n}>\alpha$, so there exists $k$ with $b_{k}=b_{n}-\alpha$ and $n>k$. We use the same argument as in Case 1, calculating the total distance between $b_{k}$ and $b_{n}$ as an integer multiple of $g_m$ to show that $\alpha\in \mathbb{Q}$.


(c)

>[!thm]

Let $\alpha>0$ be a fixed irrational generator. Consider a musical scale of length $q\in \mathbb{N}$ generated by $\alpha$, given by the set of $q$ distinct points of the form 
$$\mathcal{S}_{q}(k):=\{R_{\alpha}^{j}(0):k≤j≤k+q-1\},~\text{for some }k\in \mathbb{Z}$$
Then, 
1. The set $\mathcal{S}_{q}(k)$ will give rise to two or three distinct consecutive distances
2. Scales with two consecutive distances arise if and only if $q$ corresponds to an optimal scale size of the first kind.




Let's generalize the definition of a scale: 
$$\mathcal{S}_{n}(k,x):=\{R_{\alpha}^{j}(x):k\le j\le n+k-1\}$$
Note that we wish to show that (i) and (ii) hold for all scales of type: 
$$\begin{align*}
\mathcal{S}_{n}(k,0)&=\{R_{\alpha}^{j}(0):k\le j\le n+k-1\}\\
&= \{\underbrace{R^{i+k-1}_{\alpha}(0)}_{=R^{i}_{\alpha}(R^{k-1}_{\alpha}(0))}:1\le i\le n\}\\
&= \mathcal{S}_{n}(1,R_{\alpha}^{k-1}(0))
\end{align*}$$
We will show that (i) and (ii) hold for all scales of the form $$\mathcal{S}_{n}(1,x):x\in[0,1)$$which implies Theorem \ref{music_TGT}. 


Consider the sequence $b_{m}$ of \ref{} with $$0<b_{1}<\cdots b_{n}<1$$and let $x\in [0,1)$ be given. Let $m$ be 1 if $b_{1}+x\ge1$. Otherwise, we take $m$ to be the greatest integer such that $b_{m}+x<1$:
$$
m:=\max\{k\in \mathbb{N}:b_{k}+x<1\}
$$
Observe that the sequence 
$$\{a_{k}\}_{k=1}^{n}:=\{b_{k}+x(\mod 1)\}_{k=1}^{n}$$
may be written in increasing order: 
$$
0<a_{m+1}<\cdots<a_{n}<a_{1}<\cdots<a_{m}<1
$$
since: 
$$\begin{align*}
k\le m&\implies b_{k}\le b_{m}\\
&\implies b_{k+x}\le b_{m}+x<1\\
&\implies a_{k}=b_{k}+x\\
k>m&\implies b_{m}<b+k \\
&\implies b_{k}+k \not<1\\
&\implies a_{k}=b_{k}+x-1<a_{1}
\end{align*}$$
So we see that the order of $a_{1}\ldots, a_{m}$ is the same and the order of $a_{m+1},\ldots a_{n}$ is the same, but with the larger terms first.

We compute the gaps of $a_{k}$: $$G_{1}=1+a_{1}-a_{n},\quad G_{m}=a_{m}-a_{m-1},\quad m=2,\ldots,n$$
$$\begin{align*}
G_{1}&= 1+a_{1}-a_{n}\\
&= 1+[(b_{1}+x)\mod1]-[(b_{n}+x)\mod1]\\
&= 1+[(b_{1}+x)-(b_{n}+x)\mod1]\\
&= 1+[(\underbrace{b_{1}-b_{n}}_{<1})\mod1]\\
&= 1+b_{1}-b_{n}\\
&= g_{1}\\
G_{m}&=a_{m}-a_{m-1}\\
&= [(b_{m}+x)\mod1]-[(b_{m-1}+x)\mod1]\\
&= [(b_{m}+x)-(b_{m-1}+x)]\mod1\\
&= (\underbrace{b_{m}-b_{m-1}}_{<1})\mod1\\
&= b_{m}-b_{m-1}\\
&= g_{m}
\end{align*}$$
Thus, the sequence $a_{k}$ has exactly the same gaps as $b_{m}$. 

Note that $$\{a_{k}\}_{k=1}^{n}=\mathcal{S}_{n}(1,x)$$
since for each $1\le k\le n$, we can write $$a_{k}=(j \alpha\mod1)+x\mod1=j \alpha+x\mod 1= R^{j}_{\alpha}(x)$$for a unique $j$ (uniqueness from Kronecker's Theorem). This concludes the argument of (i) for $\mathcal{S}_{n}(k)$.

We see that the gaps of the scale $\mathcal{S}_{n}(1,x)$ are independent of $x$. In particular, the gaps of $\mathcal{S}_{n}(k)$ are the same for all $k\in \mathbb{N}$. We consider the case of $\mathcal{S}_{n}(1)$. Notice that the elements of $\mathcal{S}_{n}(1)$ form exactly the sequence $\{b_{m}\}_{m=1}^{n}$. Also it is best scale of the first kind if and only if either the first or $n$-th iterate is closest to 0. This is equivalent to Shiu's definition of $n$ being a node. So, Lemma \ref{b} gives (ii) for $\mathcal{S}_{n}(1)$ in particular. By the earlier comment, we see that it holds generally for $\mathcal{S}_{n}(k)$. 
