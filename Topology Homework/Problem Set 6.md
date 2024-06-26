<p align=center>
Topology <br>
Problem Set 6 <br>
Isaac Viviano
</p>

---

>[!note] 2.2.1
Let $\mathcal{T}$ be a [[Topology]] and let $\mathcal{B}$ be a [[Basis of a Topology]] for $\mathcal{T}$. Let $\mathcal{U}$ be some [[Topology]] containing $\mathcal{B}$. Let $U$ be [[Open Set]] in $\mathcal{T}$. Then, for each $x\in U$, pick $B_{x}\in \mathcal{B}$ such that $x\in B_{x}\subseteq U$. As $\mathcal{B}\subseteq \mathcal{U}$, $B_{x}$ is [[Open Set]] in $\mathcal{U}$. So, $$U=\bigcup_{x\in U}B_{x}$$is a [[Union]] of [[Open Set]] [[Set]]s in $\mathcal{U}$, so $U\in \mathcal{U}$ as $\mathcal{U}$ is a [[Topology]]. This shows that the [[Intersection]] of all topologies that contain $\mathcal{B}$ contains $\mathcal{T}$. As $\mathcal{T}$ also contains $\mathcal{B}$, this intersection is also a [[Subset]] of $\mathcal{T}$. 

>[!note] 2.2.4
(a) Let $a,b,c\in \mathbb{R}$. Clearly, $$(x,y)\in\{(x,y):ax+by>c\}\iff(x,y)\in\{(x,y):-ax-by<-c\}$$As $\{(x,y):-ax-by<-c\}$ is an open half plane, so is $\{(x,y):ax+by>c\}$.
>
(b) Let $a,b,c,d\in \mathbb{R},a<b,c<d$ be given. Then, the general [[Basis of a Topology]] element: $$(a,b)\times(c,d)$$can be written as the [[Intersection]] of four half-open planes: $$x>a,y>c,x<b,y<d$$

