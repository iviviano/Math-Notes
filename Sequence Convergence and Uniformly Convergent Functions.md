---
tag: topology
mathLink: sequence convergence and uniformly continuous functions proposition
---
>[!prop]
Let $X$ be a [[Topological Space]] and let $\{f_{n}\}$ be a [[Sequence]] in [[Vector Space of Continuous Bounded Functions]]$(X)$. If $f\in C_{b}(X)$, then $f_{n}$ [[Converges (Sequence)]]s to $f$ in the [[Metric Space]] $C_{b}(X)$ [[iff]] the [[Sequence]] [[Uniform Convergence]] to $f$.
>
$f_{n}$ is [[Cauchy Sequence]] in $C_{b}(X)$ [[iff]] it a [[Uniformly Cauchy Sequence]].

>[!proof]
Let $\rho$ be the [[Metric on C_b(X)]]. Suppose $f_{n}$ [[Converges (Sequence)]]s to $f$. Let $\epsilon>0$ be given. Pick $N\in \mathbb{N}$ such that if $n≥N$, $\rho(f,f_{n})<\epsilon$. Then, if $n≥N$, for all $x\in X$, $|f(x)-f_{n}(x)|<\epsilon$, so $f_{n}$ does [[Uniform Convergence]] to $f$.
>
Suppose $f_{n}$ does [[Uniform Convergence]] to $f$. Then, pick $N\in \mathbb{N}$ such that if $n≥N$, for all $x\in X$, $|f_{n}(x)+f(x)|<\frac{\epsilon}{2}$. Then, $\rho(f,f_{n})=\sup\{|f(x),f_{n}(x)|:x\in \frac{X\}≤\epsilon}{2}<\epsilon$, so $f_{n}\rightarrow f$ in $C_{b}(X)$