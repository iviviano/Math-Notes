---
tag: topology
mathLink:
---
> [!thm]
> Let $\bar{d}(a,b)=\min\{|a-b|,1\}$ be the [[Standard Bounded Metric]] on $\mathbb{R}$. If $\mathbf{x}$ and $\mathbf{y}$ are two points of $\mathbb{R}^{\omega}$, define
> $$D(\mathbf{x},\mathbf{y})=\sup\{\frac{\bar{d}(x_{i},y_{i})}{i}\}$$
> Then, $D$ is a [[Metric]] that induces the [[Product Topology]] on $\mathbb{R}^{\omega}$.

$D$ is a [[Metric]]:
1. nonnegative is trivial
2. symmetry is trivial
3. Triangle inequality:
For all $i$, 
$$\frac{\bar{d}(x_{i},z_{i})}{i}\le \frac{\bar{d}(x_{i}, y_{i})}{i}+\frac{\bar{d}(y_{i},z_{i})}{i}\le D(\mathbf{x},\mathbf{y})+D(\mathbf{y},\mathbf{z})$$
as $\bar{d}$ is a [[Metric]]. [[therefore]]
$$\sup \{\frac{\bar{d}(x_{i},z_{i})}{i}\}\le D(\mathbf{x},\mathbf{y})+D(\mathbf{y},\mathbf{z})$$
[[therefore]] $D$ is a [[Metric]].

$D$ induces the [[Product Topology]] on $\mathbb{R}^n$


$$A\cup B=\{a:a\in A\text{ or }a\in B\}=\text{smallest set }C \text{ such that }A\subseteq C \text{ and }B\subseteq C$$

suppose $\texttt{true}$ is larger $\texttt{false}$ -> $\texttt{false}$ is smaller than $\texttt{true}$


$$A\lor B=\text{smallest value }C \text{ such that }A \text{ is smaller than }C \text{ and }B \text{ is smaller than }C$$
