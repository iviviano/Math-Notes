---
tags:
  - topology
mathLink: metric on $C_b(X)$
---
>[!prop]
>Let $X$ be a [[Topological Space]]. Let $f:C_{b}(X)\times C_{b}(X)\rightarrow \mathbb{R}$ be defined by the [[Rule of Assignment]]:
>$$\rho(f,g)=\sup\{|f(x)-g(x)|:x\in X\}$$
>where $f,g\in$ [[Vector Space of Continuous Bounded Functions]]$(X)$. Then, $\rho$ is a [[Metric]] on $C_{b}(X)$.

>[!proof]
Let $f,g,h\in C_{b}(X)$. 
>1. If $f≠g$, then there exists $x$ such that $f(x)≠g(x)$, so $\rho(f,g)>0$. $\rho(f,f)=\sup\{0\}=0$
>2. $\rho(f,g)=\rho(g,f)$ because $|f(x)-g(x)|=|g(x)-f(x)|$.
>3. By the [[Triangle Inequality]], $$|f(x)-g(x)|≤|f(x)-h(x)|+|h(x)-g(x)|$$So, $$\begin{align*}\rho(f,g)&=\sup\{|f(x)-g(x)|\}≤\sup\{|f(x)-h(x)|+|h(x)-g(x)|\}\\&≤\sup\{|f(x)-h(x)|\}+\sup\{h(x)-g(x)\}\\
&=\rho(f,h)+\rho(h,g)
\end{align*}$$
