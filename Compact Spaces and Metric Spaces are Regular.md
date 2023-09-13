---
tag: topology
mathLink: compact spaces and metric spaces are regular
---
>[!prop]
>[[Hausdorff Space]] that are [[Compactness]] and [[Metric Space]]s are [[Regular]].

>[!proof]
Let $X$ be a [[Compactness]] [[Topological Space]]. Then, let $F$ be a [[Closed Set]] [[Subset]] of $X$. As $X$ is [[Compactness]], $F$ is [[Compactness]] by the [[Characterizations of Compactness]]. Let $x\notin F$. For each $y\in F$, let $U_{y}$ and $V_{y}$ be [[Disjoint]] [[Open Set]] [[Subset]]s of $X$ such that $x\in U_{y}$ and $y\in V_{y}$ by the [[Hausdorff Axiom]]. Then, $\{V_{y}:y\in F\}$ is an [[Open Cover]] of $F$. As $F$ is [[Compactness]], there is a finite [[Subcover]] of $F$ can be found from $y_{1},\ldots,y_{n}$. Let $$V=\bigcup_{i=1}^{n}V_{y_{i}}\supset F$$$$U=\bigcap_{i=1}^{n}U_{y_{i}}\ni x$$give the required sets to show that $X$ is [[Regular]].
>
Let $(X,d)$ be a [[Metric Space]]. Let $F$ be a [[Closed Set]] [[Subset]] of $X$. Let $x\notin F$. For $y\in F$, pick $\epsilon_{y}$ such that $$x\notin B_{d}(y,\epsilon_{y})$$
Then let $$V=\bigcup_{y\in F}B_{d}(y,\frac{\epsilon_{y}}{2})\supseteq F$$ Let $\epsilon=\text{dist}(x,V)$ where $\text{dist}$ is [[Distance]]. Then, $$x\in B_{d}(x,\epsilon)$$ and $B_{d}(x,\epsilon)\cap V=\emptyset$. So, $X$ is [[Regular]].
