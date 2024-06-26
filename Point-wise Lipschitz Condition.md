---
mathLink: point-wise Lipschitz
---
>[!def]
Let $A\subseteq \mathbb{R}$ be nonempty and let $f:A \rightarrow \mathbb{C}$ be a [[Function]]. $f$ is said to satisfy a *point-wise Lipschitz condition* at $x_{0}\in A$ if for some $\delta>0$, $$\sup_{x\in[x_{0}-\delta,x_{0}+\delta]\cap A-\{x_{0}\}}\left| \frac{f(x)-f(x_{0})}{x-x_{0})}\right|<\infty$$exists.
Equivalently, for some constant $0<L_{x_{0}}$, and $\delta>0$, $f$ satisfies $$|f(x)-f(x_{0})|\le L_{x_{0}}\cdot \left|x-x_{0}\right|$$for all $$x\in[x_{0}-\delta,x_{0}+\delta]\cap A$$

>[!note] 
>The second formulation immediately shows that $f$ Lipschitz at $x_{0}$ implies $f$ is [[Continuity at a Point]] $x_0$

We may phrase the Lipschitz condition as locally, all secant lines through $t_{0}$ have bounded slope