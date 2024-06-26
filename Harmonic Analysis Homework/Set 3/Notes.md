Don't Forget:
- periodic function properties


>[!note] 1

Let $\epsilon>0$ be given. Since $\frac{\partial f}{\partial y}$ is continuous, $\frac{\partial f}{\partial y}:[c,d]\rightarrow \mathbb{C}$ is uniformly continuous. Pick $\delta>0$ such that for all $x\in[a,b]$ and all $y_{0},y_{1}\in[c,d]$, $$|y_{0}-y_{1}|<\delta\implies \left|\frac{\partial f}{\partial y}(x,y_{0})- \frac{\partial f}{\partial y}(x,y_{1})\right|$$Fix $x\in[a,b]$. At $y_{0}$,
$$\begin{align*}
\frac{d}{dy}\int_{a}^{b}f(x,y)&:=  \frac{d}{dy}F(y_{0})\\
&\ = \lim_{y\rightarrow y_{0}}\frac{F(y)-F(y_{0})}{y-y_{0}}\\
\end{align*}$$
To show the limit
$$\begin{align*}
\left|\frac{F(y)-F(y_{0})}{y-y_{0}}-\int_{a}^{b} \frac{\partial  f}{\partial y}(x,y_{0})\ dx\right|&= \left|\frac{\int_{a}^{b}f(x,y)\ dx-\int_{a}^{b}f(x,y_{0})}{y-y_{0}}\ dx-\int_{a}^{b} \frac{\partial  f}{\partial y}(x,y_{0})\ dx\right|\\
&= \left|\int_{a}^{b}\frac{f(x,y)-f(x,y_{0})}{y-y_{0}}\ dx-\int_{a}^{b} \frac{\partial  f}{\partial y}(x,y_{0})\ dx\right|\\
&= \left|\int_{a}^{b} \frac{f(x,y)-f(x,y_{0})}{y-y_{0}}-\frac{\partial  f}{\partial y}(x,y_{0})\ dx\right|\\
&\le\int_{a}^{b}\left|\frac{f(x,y)-f(x,y_{0})}{y-y_{0}}- \frac{\partial  f}{\partial y}(x,y_{0})\right|\ dx\\
\end{align*}$$
By the (MVT), pick $y_{1}\in[y,y_{0}]$ with $$\frac{f(x,y)-f(x,y_{0})}{y-y_{0}}= \frac{\partial f}{\partial y}(x,y_{1})$$Since $|y_{0}-y|<\delta$ and $y_{1}\in[y,y_{0}]$, $|y_{0}-y_{1}|\le|y_{0}-y|<\delta$ $$\begin{align*}
\int_{a}^{b}\left|\frac{f(x,y)-f(x,y_{0})}{y-y_{0}}- \frac{\partial  f}{\partial y}(x,y_{0})\right|\ dx&= \int_{a}^{b} \left|\frac{\partial f}{\partial y}(x,y_{1})-\frac{\partial f}{\partial x}(x,y_{0})\right|\ dx\\
&\le \int_{a}^{b} \frac{\epsilon}{b-a}\ dx\\
&= \epsilon
\end{align*}$$

>[!note] 2

(c-1) suppose $f\in \mathcal{R}_{1}(\mathbb{R};\mathbb{C})$ and $g\in \mathcal{C}_{1}(\mathbb{R};\mathbb{C})$. Let $$h(t):=(f\star g)(t)=\int_{0}^{1}f(s)g(t-s)\ ds$$
Note that $f$ is Riemann integrable and thus bounded, and $g$ is periodic and continuous and thus uniformly continuous.

Let $\epsilon>0$ be given and fix $t_{0}\in \mathbb{R}$. Since $g$ is [[Uniform Continuity]], pick $\delta>0$ such that for all $x,y\in \mathbb{R}$, if $|x-y|<\delta$, $|g(x)-g(y)|< \frac{\epsilon}{\|f\|_{\infty}}$. Let $t\in \mathbb{R}$ with $|t-t_{0}|<\delta$. Then for all $s\in[0,1]$, $$|(t-s)-(t_{0}-s)|=|t-s-t_{0}+s|=|t-t_{0}|<\delta$$So, 
$$\begin{align*}
|h(t)-h(t_{0})|&= \left|\int_{0}^{1}f(s)g(t-s)\ ds-\int_{0}^{1}f(s)g(t_{0}-s)\ ds\right|\\
&= \left|\int_{0}^{1}f(s)g(t-s)- f(s)g(t_{0}-s)\ ds\right|\\
&= \left|\int_{0}^{1}f(s)(g(t-s)- g(t_{0}-s))\ ds\right|\\
&\le \int_{0}^{1}\left|f(s)\right|\cdot\left|g(t-s)-g(t_{0}-s)\right|\ ds\\
&< \int_{0}^{1}|f(s)|\cdot \frac{\epsilon}{\|f\|_{\infty}}\ ds\\
	&= \frac{\epsilon}{\|f\|_{\infty}}\int_{0}^{1}\left|f(s)\right|\ ds\\
&\le \frac{\epsilon}{\|f\|_{\infty}}\cdot\|f\|_{\infty}\quad(\text{ML estimate})\\
&= \epsilon
\end{align*}$$
Therefore, $h$ is [[Continuous]].

For all $t$, we have
$$\begin{align*}
h(t)&= \int_{0}^{1}f(s)g(t-s)\ ds\\
&= \int_{0}^{1}f(s)g(t-s+1)\ ds\quad(g\text{ is }1\text{-periodic})\\
&= \int_{0}^{1}f(s)g((t+1)-s)\ ds\\
&= h(t+1)
\end{align*}$$showing that $h$ is also $1$-periodic.

(c-2)

Let $f\in\mathcal{C}_{1}(\mathbb{R};\mathbb{C})$ and $g\in \mathcal{C}^{k}_{1}(\mathbb{R};\mathbb{C})$. Let $h=f\star g$. We have

Note that $f(s)g(t-s)$ is $k$-times continuously differentiable with respect to $t$. By problem (1), $$\begin{align*}
\frac{d }{d t}h(t)&= \int_{0}^{1}\frac{\partial }{\partial t}(f(s)g(t-s))\ ds\\
&= \int_{0}^{1} f(s)g'(t-s)\ ds
\end{align*}
$$We may do this $k$ times iteratively, showing $$h^{(k)}(t)=\int_{0}^{1}f(s)g^{(k)}(t-s)\ ds$$Since $f$ and $g^{(k)}$ are continuous and $1$-periodic, $h^{(k)}$ is continuous and $1$-periodic. Therefore, $$f\star g=h\in\mathcal{C}_{1}^{k}(\mathbb{R};\mathbb{C})$$ 



(d)

It suffices to show that $$\|f\star g\|_{\infty}\le\|g\|_{\infty}\cdot\|f\|_{1}$$Then, the symmetry property in part (a) gives $$\begin{align*}
\|f\star g\|_{\infty}&= \|g\star f\|_\infty\le \|f\|_{\infty}\cdot\|g\|_{1}
\end{align*}$$
Proof: $$\begin{align*}
\|f\star g\|_{\infty}&= \left\|\int_{0}^{1}f(s)g(t-s)\ ds\right\|_{\infty}\\
&= \sup_{t\in\mathbb{R}} \left\{\left|\int_{0}^{1}f(s)g(t-s)\ ds\right|\right\}\\
&\le \sup_{t\in \mathbb{R}}\left\{\int_{0}^{1}|f(s)|\cdot|g(t-s)|\ ds\right\}\\
&\le \sup_{t\in \mathbb{R}}\left\{\|g\|_{\infty}\int_{0}^{1}|f(s)|\ ds\right\}\\
&= \|g\|_{\infty}\int_{0}^{1}|f(s)|\ ds\\
&= \|g\|_{\infty}\cdot\|f\|_{1}
\end{align*}$$



(e) 
Suppose $g_{n}\rightarrow g$ with respect to the [[L1 Norm]] and let $\epsilon>0$ be given. Pick $N\in \mathbb{N}$ such that for all $n\ge N$, $$\|g_{n}-g\|_{1}< \frac{\epsilon}{\|f\|_{\infty}}$$Then, 
$$\begin{align*}
\|f\star g_{n}-f\star g\|_{\infty}&= \|f\star(g_{n}-g)\|_{\infty}\\
&\le \min\{\|f\|_{\infty}\cdot \|g_{n}-g\|_{1}, \|g_{n}-g\|_{\infty}\cdot\|f\|_{1}\}\\
&\le \|f\|_{\infty}\cdot \|g_{n}-g\|_{1}\\
&< \|f\|_{\infty}\cdot \frac{\epsilon}{\|f\|_{\infty}}\\
&= \epsilon
\end{align*}$$So, $f\star g_{n}$ converges to $f\star g$ uniformly.




>[!note] 3

(a)

Note that for $a,b\ge 1$, $$\sup\{f(x):x\in[a,b]\}=f(a)$$and $$\inf\{f(x):x\in [a,b]\}=f(b)$$because $f$ is monotone decreasing.

Thus, for any partition $s_{1},\ldots,s_{N+1}$ of $[1,N+1]$, our upper and lower bounds are given by $$\begin{align*}
M_{i}&= f(s_{i})\\
m_{i}&= f(s_{i+1})\\
\end{align*}$$Consider the partition given by $s_{i}=i$ for all $1\le i\le N+1$. By definition, $$\begin{align*}
\int_{1}^{N+1}f(x)\ dx&\le \sum_{i=1}^{N}M_{i}(s_{i+1}-s_{i})\\
&= \sum_{i=1}^{N}f(s_{i})(i+1-i)\\
&= \sum_{i=1}^{N}f(i)
\end{align*}$$and $$\begin{align*}
f(1)+\int_{1}^{N}f(x)\ dx&\ge f(1)+\sum_{i=1}^{N-1}m_{i}(s_{i+1}-s_{i})\\
&= f(1)+\sum_{i=1}^{N-1}f(s_{i+1})(i+1-i)\\
&= f(1)+\sum_{i=1}^{N-1}f(i+1)\\
&= f(1)+\sum_{i=2}^{N}f(i)\quad(\text{change index})\\
&= \sum_{i=1}^{N}f(i)
\end{align*}$$
(b) 

First note that $|D_{n}(x)|$ is even:

$$\begin{align*}
|D_{n}(-x)|&= \left|\frac{\sin(\pi(2n+1)(-x))}{\sin(-\pi x)}\right|\\
&= \left|\frac{-\sin(\pi(2n+1)x)}{-\sin(\pi x)}\right|\\
&= \left|\frac{\sin (\pi(2n+1)x)}{\sin(\pi x)}\right|\\
&= |D_{n}(x)|
\end{align*}$$Therefore, $$\begin{align*}
\int_{- \frac{1}{2}}^{\frac{1}{2}}|D_{n}(x)|\ dx&= 2\int_{0}^{\frac{1}{2}}\left|D_{n}(x)\right|\ dx:=2I_{n}
\end{align*}$$
Let $$4a_{n}= \frac{2}{2n+1}$$be the period of $f_{n}:=|\sin(\pi(2n+1)x)|$. $f_n$ has zeros when $\pi(2n+1)x$ is an integer multiple of $\pi$, that is, $(2n+1)x$ is an integer, or $x=2ka_n$ for some $k\in \mathbb{N}$. It has maxima at $\pi(2n+1)x- \frac{\pi}{2}$ is an integer. These occur when $x=(2k+1)a_n$ for some $k\in \mathbb{N}$. The only extrema are these zeros and maxima. Since $f_{n}$ is continuous, it is monotonic non-decreasing from a zero to a maximum and monotonic non-increasing from a maximum to a zero. These intervals of monotonicity are $$\begin{align*}
[0,a_{n}]\\
[a_{n},2a_{n}]\\
[2a_{n},3a_{n}]\\
[3a_{n},4a_{n}]
\end{align*}$$on its period interval $[0,4a_n ]$. 
$$\begin{align*}
I_{n}&= \int_{0}^{\frac{1}{2}}|D_{n}(x)|\ dx\\
&= \int_{0}^{\frac{1}{2}}\frac{|\sin (\pi(2n+1)x)|}{|\sin(\pi x)|}\ dx\\
&= \sum_{j=0}^{2n}\int_{ja_{n}}^{(j+1)a_{n}} \frac{|\sin(\pi(2n+1)x)|}{\sin \pi x}\ dx\\
&\ge \sum_{j=0}^{2n}\int_{ja_{n}}^{(j+1)a_{n}} \frac{|\sin(\pi(2n+1)x)|}{\pi x}\ dx\\
&\ge \sum_{j=0}^{2n} \frac{1}{\pi(j+1)a_{n}}\int_{ja_{n}}^{(j+1)a_{n}} |\sin(\pi(2n+1)x)|\ dx\\
\end{align*}$$
From the previous observation, $$\begin{align*}
\int_{ja_{n}}^{(j+1)a_{n}}|\sin(\pi(2n+1)x)\ dx&= \int_{0}^{a_{n}}\sin(\pi(2n+1)x)\ dx
\end{align*}$$

We may use the change of variables $u= \pi(2n+1)x$ to write $$\begin{align*}
\int_{ja_{n}}^{(j+1)a_{n}}\sin(\pi(2n+1)x)&= \int_{0}^{a_{n}}\sin(\pi(2n+1)x)\ dx\\
&= \int_{0}^{\frac{\pi}{2}} \frac{1}{\pi(2n+1)}\sin u\ du\\
&= \frac{-\cos u}{\pi(2n+1)}\bigg|_{0}^{\frac{\pi}{2}}\\
&= 0 - \frac{-1}{\pi(2n+1)}\\
&= \frac{2a_{n}}{\pi}
\end{align*}$$
Thus, $$\begin{align*}
I_{n}&\ge \sum_{j=0}^{2n} \frac{1}{\pi(j+1)a_{n}}\cdot \frac{2a_{n}}{\pi}\\
&= \sum_{j=1}^{2n+1} \frac{2}{\pi^{2}j}\\
&= \frac{2}{\pi^{2}}\sum_{j=1}^{2n+1} \frac{1}{j}\\
&\ge \frac{2}{\pi^{2}}\int_{1}^{2n+2} \frac{1}{x}\ dx\quad\quad(\text{a})\\
&= \frac{2}{\pi^{2}}\ln x\bigg|^{2n+2}_{1}\\
&= \frac{2}{\pi^{2}}\ln(2n+2)\\
&\ge \frac{2}{\pi^{2}}\ln n
\end{align*}$$
For the upper bound,
$$
\begin{align*}
I_{n} &= \int_{0}^{\frac{1}{2}}\frac{|\sin (\pi(2n+1)x)|}{|\sin(\pi x)|}\ dx\\
&= \int_{0}^{a_{n}}\frac{|\sin (\pi(2n+1)x)|}{|\sin(\pi x)|}\ dx+\sum_{j=1}^{2n}\int_{ja_{n}}^{(j+1)a_{n}} \frac{|\sin (\pi(2n+1)x)|}{|\sin(\pi x)|}\ dx\\
&= \int_{0}^{a_{n}}\left|\frac{\sin(\pi(2n+1)x)}{\pi(2n+1)x}\right| \cdot\left| \frac{\pi(2n+1)x}{\pi x}\right|\cdot \left| \frac{\pi x}{\sin(\pi x)}\right|\ dx+\\
&\quad\quad\quad\sum_{j=1}^{2n}\int_{ja_{n}}^{(j+1)a_{n}} \frac{|\sin (\pi(2n+1)x)|}{|\sin(\pi x)|}\ dx\\
&\le \int_{0}^{a_{n}}2n+1\ dx+\sum_{j=1}^{2n}\int_{ja_{n}}^{(j+1)a_{n}} \frac{|\sin (\pi(2n+1)x)|}{|\sin(\pi x)|}\ dx\\
&\le \int_{0}^{\frac{1}{2(2n+1)}}2n+1 \ dx+\sum_{j=1}^{2n}\int_{ja_{n}}^{(j+1)a_{n}} \frac{1}{2x}\ dx\\
&= \frac{1}{2}+\sum_{j=1}^{2n} \frac{1}{2ja_{n}}\cdot a_{n}\quad(\text{ML-estimate})\\
&= \frac{1}{2}+ \frac{1}{2}\sum_{j=1}^{2n} \frac{1}{j}\\
&\le \frac{1}{2}+ \frac{1}{2}\left(1+\int_{1}^{2n} \frac{1}{x}\ dx\right)\\
&= \frac{1}{2}+ \frac{1}{2}\left( \ln x\bigg|_{1}^{2n}\right)\\
&= \frac{1}{2}+ \frac{1}{2}(\ln 2n)
\end{align*}
$$
We have $$\begin{align*}
I_{n}&\ge \frac{2}{\pi^{2}}\log n\\
I_{n}&\le \frac{1}{2}+ \frac{1}{2}(\ln 2n)\\
2I_{n}&\le 1+\ln (2n)\\
&= 1+\ln 2+\ln n\\
&\le 3+\ln n\\
2I_{n}&\ge \frac{4}{\pi^{2}}\log n
\end{align*}$$
showing the desired bounds.




>[!note] 4


Suppose $f:\mathbb{R}\rightarrow \mathbb{C}$ is periodic, non-constant, and has at least point of continuity. 

Let $$P=\{|p|:f \text{ is }p \text{-periodic}\}$$
Note that $P$ is nonempty since $f$ is periodic and $P$ is bounded below by zero, so $P$ has an infimum $\alpha=\inf P$



Let $x_{0}$ be a point of continuity of $f$. Since $f$ is not constant, pick $y\in \mathbb{R}$ with $f(x_{0})\ne f(y)$. Pick $\delta>0$ such that for all $x\in \mathbb{R}$ with $|x_{0}-x|<\delta$, $$|f(x_{0})-f(x)|<|f(x_{0})-f(y)|$$ 
Claim: $\frac{\delta}{2}$ is a lower bound for $P$. If $p\le \frac{\delta}{2}$ is a period of $f$, then for all $n\in \mathbb{Z}$, $$f(y+np)=f(y)$$Taking $$n=\left\lfloor \frac{1}{p}(x_{0}-y)\right\rfloor$$we have $$\begin{align*}
y+np &= y+p\left\lfloor \frac{1}{p}(x_{0}-y)\right\rfloor\\
&\le y+p\cdot \frac{1}{p}(x_{0}-y)\\
&= y+x_{0}-y\\
&= x_{0}\\
&< x_{0}+\delta
\end{align*}$$
and $$\begin{align*}
y+np&= y+p\left\lfloor \frac{1}{p}(x_{0}-y)\right\rfloor\\
&\ge y+p\left(\frac{1}{p}(x_{0}-y)-1\right)\\
&= y+x_{0}-y-p\\
&= x_{0}-p\\
&\ge x_{0}- \frac{\delta}{2}\\
&> x_{0}-\delta
\end{align*}$$
Therefore, $$
y+np\in(x_{0}-\delta,x_{0}+\delta)
$$since $$y+np\lt x_{0}+\delta$$and $$y+np\gt x_{0}-\delta$$
But $f(y+np)\in(x_{0}-\delta,x_{0}+\delta)$ implies that $$
|f(x_{0})-f(y+np)|<|f(x_{0})-f(y)|
$$In particular, $$|f(x_{0})-f(y+np)|\ne|f(x_{0})-f(y)|$$Thus, $$f(y+np)\ne f(y)$$contradicting that $p$ is a period. By contradiction, for all $p\in P$, $\frac{\delta}{2}<p$.


Since $\alpha$ is greater than or equal to any lower bound for $P$, $$\alpha\ge \frac{\delta}{2}>0$$Suppose 0 were a limit point of $\Pi_f$. Then we would have a sequence $p_{n}$ in $\Pi_f$ with $\pi_{n}\rightarrow 0$. But $|p_{n}|$ is a sequence in $P$ and $|p_{n}|\rightarrow 0$, contradicting that $\alpha\ge0$. Therefore, $0$ is a not a limit point of $\Pi_f$, and $f$ is has a minimal positive period by Lemma NUMBER.









>[!prop] Lemma
Let $f:\mathbb{R}\rightarrow \mathbb{C}$ be [[Periodic]] and let $\Pi_f$ denote the [[Set]] of all [[Period]]s of $f$. Then, 
>1. $\Pi_f\cup\{0\}$ is an additive [[Subgroup]] of $\mathbb{R}$
>2. If $0\notin \text{cl }\Pi_f$, then $\Pi_f$ has no other [[Limit Point]] and $f$ has a minimal period

(1)

Let $a,b\in \Pi_{f}\cup\{0\}$. We have that for all $x\in \mathbb{R}$, $$f(x)=f(a+x)$$and $$f(x)=f(b+x)=f(b+(x-2b))=f(x-b)$$

Then, $$\begin{align*}
f(x+a-b)&= f((x+a)-b)\\
&= f(x+a)\\
&= f(x)
\end{align*}
$$So, $a-b\in \Pi_f\cup\{0\}$, showing that $\Pi_f\cup\{0\}$ is an additive subgroup of $\mathbb{R}$. 

(2)

For contradiction, suppose $0\notin \text{cl }\Pi_{f}$ and $\Pi_f$ has a limit point. Let $a\in \text{cl }\Pi_{f}$ be a limit point of $\Pi_{f}$. Then, there exists a sequence $$\{a_{n}\}\subseteq \Pi_f$$with $a_{n}\rightarrow a$. Let $\epsilon>0$ be given. Pick $N$ such that for all $n,m\ge N$, $$|a_{n}-a_{m}|<\epsilon$$Fix $n\ge N$. We have $a_{n}-a_{m},a_{m}-a_{n}\in \Pi_{f}$ by (1). Let $$b_{n}=\max\{a_{n}-a_{m},a_{m}-a_{n}\}=|a_{n}-a_{m}|$$So, $0\le b_{n}<\epsilon$. Therefore, $b_{n}\in \Pi_{f}$ and $b_{n}\rightarrow 0$. This shows that $0$ is a limit point of $\Pi_{f}$ and thus $0\in \text{cl }\Pi_{f}$.

Now suppose $0\notin \text{cl }\Pi_f$. Let $T$ be a period of $f$. If $$[0,T]\cap \Pi_{f}$$is infinite, it has a limit point. But, this would be a limit point of $\Pi_f$, which has no limit points. Thus, $[0,T]\cap \Pi_f$ is finite and nonempty. $[0,T]\cap \Pi_f$ must have a minimum, showing that $f$ has a minimal positive period. 