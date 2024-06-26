---
tag: topology
mathLink: subspaces of the metric topology theorem
---
> [!thm]
> Let $d$ be a [[Metric]] on $X$; $A$ be a [[Subset]] of $X$. Then, the [[Topology]] induced by the [[Restriction]] of $d$ to $A\times A$ is the same as the [[Subspace Topology]] on $A$.

>[!proof]
>Let $\mathcal{B}$ be the standard [[Basis of a Topology]] of $X$. Then
>$$\mathcal{C}=\{B\cap A|B\in \mathcal{B}\}$$
>is a [[Basis of a Topology]] for the [[Subspace Topology]] on $A$. Let $d'=d$ [[notation for restriction]] $A$ [[notation for cartesian product]] $A$. Then,
>$$\mathcal{C}'=\{B_{d'}(x,\epsilon)|x\in A \text{ and }\epsilon>0\}$$
>is a [[Basis of a Topology]] for the [[Topology]] induced by $d'$. 
>Let $C\in \mathcal{C}$, $x\in C$ be given. Then, pick $\epsilon>0$ such that $B_{d}(x,\epsilon)\cap A=C$. 
>$$B_{d'}(x,\epsilon) \subseteq B_{d}(x,\epsilon)\cap A = C$$
>Let $y\in B_{d'}(x,\epsilon)$ be given. Then, $d'(x,y)=d(x,y)<\epsilon$ and $y\in A$, so $y\in B_{d}(x,\epsilon)$ and $y\in A$. 
>[[therefore]] the [[Finer Bases Lemma]] implies that $\mathcal{C}$ is [[Finer]] than $\mathcal{C'}$ since $B_{d'}(x,\epsilon)\in \mathcal{C'}$
>Let $C'\in \mathcal{C'}$, $x\in C'$ be given. Then, pick $\epsilon>0$ such that 
>$$C'=B_{d'}(x,\epsilon)$$
>$B_{d'}(x,\epsilon)\supseteq B_{d}(x,\epsilon)\cap A$: Let $y\in B_{d}(x,\epsilon)\cap A$ be given. Then, $y\in A$, so $d'(x, y)=d(x,y)<\epsilon$, so $y\in B_{d'}(x, \epsilon)$.
>[[therefore]] the [[Finer Bases Lemma]] implies that $\mathcal{C}$ is [[Finer]] than $\mathcal{C'}$
