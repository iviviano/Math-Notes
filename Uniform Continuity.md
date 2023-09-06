---
tag: topology
mathLink: uniformly continuous
---
>[!def]
Let $(X,d),(Y,\rho)$ be [[Metric Space]]s. Then a [[Continuous]] [[Function]] $f:X \rightarrow Y$ is *uniformly continuous* if for all $\epsilon>0$, there exists a $\delta=\delta(\epsilon)>0$, such that 
$$\forall x\in X:d(x,y)<\delta\implies \rho(f(x),f(y))<\epsilon$$

>[!note]
>For a [[Function]] to be [[Uniform Continuity]], $\delta$ must depend only on $\epsilon$ and not on the point $x$.
