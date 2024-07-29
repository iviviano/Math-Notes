From 2.1: 7, 9

>[!note] 7
Let $X$ be a [[Hausdorff Space]]. Let $x,y\in X$ be given. Let $U, V$ be [[Disjoint]] [[Neighborhood]]s of $x,y$, respectively. As [[Open Sets Intersecting the Closure Intersect the Set Theorem]], $V\cap \text{cl }U=\emptyset$. So, $y\notin \text{cl }U$. 
>
Let $X$ be a [[Topological Space]] satisfying: $\forall x,y\in X$, there is a [[Neighborhood]] $U$ of $y$ such that $x\notin \text{cl }U$. Then, $x\in X-\text{cl }U$, an [[Open Set]] [[Set]] by [[10-5 Problems]]. As $U\subseteq \text{cl }U$, $U\cap X- \text{cl }U=\emptyset$, so $X$ satisfies the [[Hausdorff Axiom]].

>[!note] 9
(a) 
>1. Let $A\subseteq Y$ be [[Closed Set]] in $Y$. Then, there is an [[Open Set]] [[Set]] $U\subseteq X$ in $X$ such that $Y-A=Y\cap U$. $$A=Y-(Y-A)=Y - Y\cap U$$Let $x\in Y\cap(X-U)$. Then, $x\in Y$ and $x\notin U$, so $x\notin Y\cap U$. Clearly, $x\in Y-Y\cap U$, so $$Y\cap(X-U)\subseteq Y-Y\cap U$$Let $x\in Y-Y\cap U$. Then, $x\in Y$ and $x\notin U$, so $x\in X-U$. As $x\in Y\cap(X-U)$, $$Y-Y\cap U\subseteq Y\cap(X-U)$$Therefore, $$A=Y-Y\cap U=Y\cap(X-U)$$As $X-U$ is [[Closed Set]] in $Y$, this gives the desired result$$$$Suppose that $A=Y\cap (X-U)$ where $U$ is [[Open Set]] in $X$. Then, $$A=Y-Y\cap U$$As $U$ is [[Open Set]] in $X$, $Y\cap U$ is [[Open Set]] in $Y$, so $A$ is [[Closed Set]] in $Y$.
>2. Let $x\in \text{cl }_{X}A\cap Y$. Let $F$ be a [[Closed Set]] [[Subset]] of $Y$ that contains $A$. Then, $F=D\cap Y$ for some [[Closed Set]] [[Set]] $D$ in $X$. $$x\in D\cap Y=F\subseteq F$$so $x$ is in all [[Closed Set]] [[Set]]s of $Y$ containing $A$. [[therefore]] $x\in \text{cl }_{Y}A$. $$$$Let $x\in \text{cl }_{Y}A$. Let $F$ be a [[Closed Set]] [[Subset]] of $X$ that contains $A$. Then, the [[Set]] $F\cap Y$ is a [[Closed Set]] [[Subset]] of $Y$ containing $A$, so $$x\in F\cap Y\subseteq F,Y$$so $x$ is in all [[Closed Set]] [[Set]]s in $X$ containing $A$ and $x\in Y$. [[therefore]] $x\in \text{cl }_{X}A\cap Y$. $$\therefore \text{cl }_{X}A\cap Y=\text{cl }_{Y}A$$
>3. Let $x\in Y\cap \text{int}_{X}A$. Then, some [[Neighborhood]] $U$ of $x$ in $X$ is contained in $A$. As $x\in Y$, the [[Neighborhood]] $U\cap Y$ of $x$ in $Y$ is also contained in $A$. So, $x$ is in some [[Open Set]] [[Subset]] of $Y$ contained in $A$. $$\therefore Y\cap \text{int}_{X}A\subseteq \text{int}_{Y}A$$
>
(b) Let $X=\mathbb{R},Y=\{0\}$. Then the set $U=\{0\}\subseteq Y$ is [[Open Set]] in $Y$ as $Y$ is a [[Topological Space]]. However, the [[Interior]] of $U$ in $X$ is empty, as no [[Open Set]] [[Set]]s in $X$ are contained in $U$.

From 2.2: 1, 4, 5

>[!note] 1
Let $\mathcal{T}$ be a [[Topology]] and let $\mathcal{B}$ be a [[Basis of a Topology]] for $\mathcal{T}$. Let $\mathcal{U}$ be some [[Topology]] containing $\mathcal{B}$. Let $U$ be [[Open Set]] in $\mathcal{T}$. Then, for each $x\in U$, pick $B_{x}\in \mathcal{B}$ such that $x\in B_{x}\subseteq U$. As $\mathcal{B}\subseteq \mathcal{U}$, $B_{x}$ is [[Open Set]] in $\mathcal{U}$. So, $$U=\bigcup_{x\in U}B_{x}$$is a [[Union]] of [[Open Set]] [[Set]]s in $\mathcal{U}$, so $U\in \mathcal{U}$ as $\mathcal{U}$ is a [[Topology]]. This shows that the [[Intersection]] of all topologies that contain $\mathcal{B}$ contains $\mathcal{T}$. As $\mathcal{T}$ also contains $\mathcal{B}$, this intersection is also a [[Subset]] of $\mathcal{T}$. 

>[!note] 4
(a) Let $a,b,c\in \mathbb{R}$. Let $x,y:ax+by>c$. Pick $\epsilon>0$ such that $ax+by>c+\epsilon$. Then if $d((x_{1},y_{1}),(x,y))< \frac{\epsilon}{ab}$, 
>$$\begin{align}
&\epsilon>ab|x-x_{1}|+ab|y-y_{1}|≥a|x-x_{1}|+b|y-y_{1}|\\
&≥ax-ax_{1}+by-by_{1}=ax+by-(ax_{1}+by_{1})
\end{align}$$
So, $\epsilon>ax+by-(ax_{1}+by_{1})$. So, $$ax_{1}+by_{1}>ax+by-\epsilon>c+\epsilon-\epsilon=c$$
So, $B((x,y),\frac{\epsilon}{ab})$ is contained in the half-open plane, showing that the half-open plane is [[Open Set]].
>
(b) Let $a,b,c,d\in \mathbb{R},a<b,c<d$ be given. Then, the general [[Basis of a Topology]] element: $$(a,b)\times(c,d)$$can be written as the [[Intersection]] of four half-open planes: $$x>a,y>c,x<b,y<d$$

>[!note] 5
(a) Must show that $S$ is a [[Cover]] of $X$. But if $X$ has only $1$ element, then $\mathcal{S}$ is empty?
>
(b) As every [[Topological Space]] with less than two elements is a [[Hausdorff Space]], we must only consider the case where $X$ has at least $2$ elements. Let $x,y\in X$ with $x≠y$ and suppose $x≤y$. Suppose there is a $c\in X$ such that $x≤c≤y$ and $x≠c≠y$. Then, $x\in\{z:z≤c \text{ and }z≠c\}\in \mathcal{S}$ and $y\in\{z:z>c \text{ and }z≠c\}\in \mathcal{S}$. As these are two [[Disjoint]] [[Neighborhood]]s the [[Topology]] generated by $\mathcal{S}$ satisfies the [[Hausdorff Axiom]]. Otherwise, $\forall c\in X$, $x≤c≤y\implies x=c\lor y=c$. So, $x\in\{z:z≤y \text{ and }z≠y\}\in \mathcal{S}$ and $y\in \{z:x≤z \text{ and }z≠x\}\in \mathcal{S}$ are [[Disjoint]] [[Neighborhood]]s of $x,y$, so the [[Topology]] generated by $\mathcal{S}$ satisfies the [[Hausdorff Axiom]].
>
(c) Clearly if $a,b\in X$, $$(a,b)=\{x\in X:a≤x \text{ and }x≠a\}\cap\{x:\in X:x≤b \text{ and }x≠b\}=I$$is a finite [[Intersection]] of [[Subbasis]] elements. Let $x\in(a,b)$. As $a<x<b$, $a≤x$, $a≠x$, $x≤b$, and $x≠b$. So, $x\in I$. Let $x\in I$. As $a≤x$ and $x≠a$, $a<x$. Similarly, $x≤b$ and $x≠b$ [[implies]] $x<b$. So, $x\in(a,b)$. So, the [[Collection]] of intervals is a [[Basis of a Topology]] for the [[Order Topology]].
