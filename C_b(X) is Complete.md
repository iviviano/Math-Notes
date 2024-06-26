---
tag: topology
mathLink: $C_{b}(X)$ is complete for any topological space $X$
---
>[!thm]
>Let $X$ be a [[Topological Space]]. Then [[Vector Space of Continuous Bounded Functions]]$(X)$ is a [[Complete]] [[Metric Space]].

>[!proof]
Let $\{f_{n}\}\subseteq C_{b}(X)$ be a [[Cauchy Sequence]]. For each $x\in X$, $|f_{n}(x)-f_{m}(x)|≤\rho(f_{n},f_{m})$. So, $\{f_{n}(x)\}\subseteq \mathbb{R}$ is [[Cauchy Sequence]]. So, $f(x)=\lim_{n \rightarrow \infty}f_{n}(x)$ exists since $\mathbb{R}$ is [[Complete]]. We must show that $f\in C_{b}(X)$ and $\rho(f_{n},f)\rightarrow 0$.
>
Let $N$ such that $\rho(f_{n},f_{m})<1$ for all $n,m>N$ since $f_{n}$ is [[Cauchy Sequence]]. Since $f_{1},\ldots,f_N$ are [[Bounded Function into R]], there exists $M$ such that $|f_{k}(x)|<M$ for all $x\in X$ and $k=1,\ldots,N$. If $n≥N$ and $x\in X$, then $$|f_{n}(x)|<\rho(f_{n},f_N)+f_{N}(x)<1+M$$Therefore, $\{f_{n}(x):n≥N\text{ and }x\in X\}\subseteq[-(M+1),M+1]$. Since [[Closed Sets in Metric Spaces contain Sequence Limits]], $\{f(x):x\in X\}\subseteq[-(M+1),M+1]$. Therefore, $f$ is [[Bounded Function into R]].
>
Fix $\epsilon>0$ and let $N$ be such that $$\rho(f_{n},f_{m})< \frac{\epsilon}{3}$$for all $n,m≥N$. If $x\in X$ and $n≥N$, then $$|f(x)-f_N(x)|≤|f(x)-f_{m}(x)|+\rho(f_{m},f_{n})<|f(x)-f_{m}(x)|+ \frac{\epsilon}{3}$$for all $m≥N$. Let $m \rightarrow \infty$. Then, $|f(x)-f_{m}(x)|\rightarrow 0$ so, $$|f(x)-f_n(x)|<\frac{\epsilon}{3}$$Therefore, $\rho(f_{n},f)\rightarrow 0$ (WHY?). 
>
Fix $x$ and $n≥N$. Since $f_{n}$ is [[Continuous]], there exists a [[Neighborhood]] $U$ of $x$ such that $$|f_{n}(y)-f_{n}(x)|<\frac{\epsilon}{3}$$ for all $y\in U$ by the [[Ep-de Formulation of Continuity]]. Therefore, $$|f(y)-f(x)|≤|f(y)-f_{n}(y)|+|f_{n}(y)-f_{n}(x)|+|f_{n}(x)-f(x)|<\epsilon$$So, $f$ is [[Continuous]]. 
>
Therefore, $f_{n}\rightarrow f\in C_{b}(X)$, so $C_{b}(X)$ is [[Complete]].

