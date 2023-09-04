---
tag: topology
mathLink: metrics induce the product topology on $\mathbb{R}^n$
---
> [!thm]
> The [[Topology]]s on $\mathbb{R}^n$ induced by the [[Euclidean Metric]] $d$ and the [[Square Metric]] $\rho$ are the same as the [[Product Topoplogy]] on $\mathbb{R}^n$.

Note: as the [[Box Topology]] is the same as the [[Product Topoplogy]] on $\mathbb{R}^n$, it is also the same as the [[Topology]] induced by the [[Euclidean Metric]] and the [[Square Metric]].

> [!proof]
> Equivalence of the two [[Metric Topology]]s:
> Let $\mathbf{x} = (x_1, \ldots, x_n)$ and $\mathbf{y} = (y_1, \ldots, y_n)$. Let $\epsilon > 0$ be given. Then, 
> $\rho(\mathbf{x},\mathbf{y})\le d(\mathbf{x}, \mathbf{y})$
> Pick $i$ such that $|x_{i}- y_{i}|=\rho(\mathbf{x},\mathbf{y})$. Then, 
> $\rho(\mathbf{x}, \mathbf{y})=\sqrt{|x_{i} - y_{i}|^{2}}\le\sqrt{(x_{1}-y_1)^2+\ldots(x_{n}-y_{n})^2}=d(\mathbf{x},\mathbf{y})$
> and,
> $d(\mathbf{x},\mathbf{y})\le \sqrt{n(x_{i}- y_{i})^{2}}=\sqrt{n}|x_{i}- y_{i}| = \sqrt{n}\rho(\mathbf{x},\mathbf{y})$
> [[therefore]] for any $\epsilon$ $>0$, 
> $B_{\rho}(\mathbf{x},\epsilon)\subseteq B_{d}(\mathbf{x},\epsilon)$
> and, if $\delta>\frac{\epsilon}{\sqrt{n}}$,
> $B_{d}(\mathbf{x},\delta)\subseteq B_{\rho}(\mathbf{x},\epsilon)$
> [[therefore]] by the [[Finer Metrics Lemma]], the [[Topology]] induced by $d$ is the same as the topology induced by $\rho$. 
> 
> Equivalence of metric and [[Order Topology]] on $\mathbb{R}$:
> Let $x\in \mathbb{R}$ be given. Suppose $U$ is [[Open Set]] in $\mathbb{R}$ under the [[Order Topology]]. Then, $U$ can be written as a [[Union]] of [[Open Interval]]s. Pick one of these intervals $U_{x}=(a,b)$ with $x\in U_x$. Then if $\epsilon<\min(x-a,b-x)$, $B_d(x,\epsilon)$ [[subset]] $U_{x} \subseteq U$. So, the [[Euclidean Topology]] is [[Finer]] than the [[Order Topology]] on $\mathbb{R}$ by the [[Finer Bases Lemma]]. 
> Let $B$ be a [[Ball]] containing $x$. Then, pick $\epsilon>0$ such that $B_{d}(x,\epsilon)\subseteq B$. $B_d(x,\epsilon)=(x-\epsilon,x+\epsilon)$, which is [[Open Set]] in $\mathbb{R}$, so the [[Order Topology]] on $\mathbb{R}$ is [[Finer]] than the [[Euclidean Topology]] by the [[Finer Bases Lemma]]. 
> 
> Product of metrics is metric of product:
> By the [[Basis for the Product Topology Theorem]], a [[Basis]] for the [[Product Topoplogy]] on $\mathbb{R}^n$ is the collection $\mathcal{B}$ of sets $\prod B_\rho(x_{i},\epsilon_{i})$ where $x_{i}\in \mathbb{R}$. A [[Basis]] for the [[Metric Topology]] on $\mathbb{R}^n$ is the collection $\mathcal{B}'$ of [[Ball]]s $B_{\rho}(\mathbf{x},\epsilon)$, where $\mathbf{x}\in \mathbb{R}^n$. Let $\mathbf{x}\in \mathbb{R}^n$ be given. Let $B\in \mathcal{B}$ be given with $\mathbf{x}\in B$. Pick $\epsilon>0$ such that $\forall i : B_{\rho}(x_{i},\epsilon)\subseteq B_i$. Then, 
> $B_{\rho}(\mathbf{x},\epsilon)\subseteq B$
> As $B_{\rho}(\mathbf{x},\epsilon)\in \mathcal{B}'$, the [[Metric Topology]] on $\mathbb{R}^n$ is [[Finer]] than the [[Product Topoplogy]] on $\mathbb{R}^n$ by the [[Finer Bases Lemma]].
> Let $B'\in \mathcal{B}'$ be given with $\mathbf{x}\in B'$. Then, for some $\epsilon > 0$
> $\prod B_{i}=\prod B_{\rho}(x_i,\epsilon)\in \mathcal{B}$
> [[therefore]] the [[Product Topoplogy]] is [[Finer]] than the [[Metric Topology]] on $\mathbb{R}^n$ by the [[Finer Bases Lemma]].
> 
> [[therefore]] The [[Metric Topology]]s induced by the [[Euclidean Metric]] and the [[Square Metric]] are the same as the [[Product Topoplogy]] of $\mathbb{R}^n$ under the [[Order Topology]].
