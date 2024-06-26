From 3.1: 4 and 6

>[!note] 4
Let $\{f_{n}\}\subseteq C_{u}(X)$.
>
Suppose $f_{n}\rightarrow f\in C_{b}(X)$. Let $\epsilon>0$ be given. Pick $N$ such that for all $n≥N$, for all $x$, $$|f(x)-f_{n}(x)|<\frac{\epsilon}{3}$$Pick $\delta$ such that for all $x,y\in X$, $$d(x,y)<\delta\implies|f_{N}(x)-f_{N}(y)|<\frac{\epsilon}{3}$$
Then, if $x,y\in X$ and $d(x,y)<\delta$, $$\begin{align*}
|f(x)-f(y)|&=|f(x)-f_{N}(x)+f_{N}(x)-f_{N}(y)+f_{N}(y)-f(y)|\\
&\le |f(x)-f_{N}(x)|+|f_{N}(x)-f_{N}(y)|+|f_{N}(y)-f(y)|\\
&\lt \frac{\epsilon}{3}+ \frac{\epsilon}{3}+ \frac{\epsilon}{3}\\
&=\epsilon
\end{align*}$$Therefore, $f$ is [[Uniform Continuity]]. So, $f\in C_{u}(X)$. So, $C_{u}(X)$ contains all [[Sequence]] [[Limit of a Sequence]]s. Therefore, $C_{u}(X)$ is a [[Closed Set]] [[Subset]] of $C_{b}(X)$ since [[Closed Sets in Metric Spaces contain Sequence Limits]].

>[!note] 6
Let $f_{n}:[0,1]\rightarrow \mathbb{R}$ be given by $$f_{n}(x)=n(x-x^{2})e^{-nx^{2}}$$Clearly, $f_{n}$ is [[Continuous]] for all $n$. For each $x$, $$\lim_{n \rightarrow \infty}f_{n}(x)=ne^{-n}=0$$However, $f_{n}$ does not [[Uniform Convergence]]:
$$\sup f_{n}\sim n$$So, $\{\sup f_{n}\}$ is unbounded. Therefore, given $\epsilon>0$ there is no value $N$ such that $$|f_{N}(x)-\lim_{n \rightarrow \infty}f_{n}(x)|=|f_{N}(x)-0|=f_{N}(x)<\epsilon$$
