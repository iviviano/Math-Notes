From section 1.1: 5, 6, 8, prove prop 1.1.11

>[!note] 5
>Prove 1.1.8: Let $(X,d)$ be a [[Metric Space]], and let $Y$ be a [[Subset]] of $X$
>(a) Suppose $G$ is [[Open Set]] in the [[Subspace]] $Y$. Then, for each $x\in G$, there is a [[Ball]] in $Y$ $B_{d_Y}(x,\epsilon_x)\subseteq G$. Then, 
>$$B_{d_{Y}}(x,\epsilon_{x})=Y\cap B_{d_{X}}(x,\epsilon_x)$$ 
>Then, 
>$$G=\bigcup_{x\in G}B_{d_{Y}}(x,\epsilon_x)=\bigcup_{x\in G}\left(Y\cap B_{d_{X}}(x,\epsilon_{x})\right)=Y\cap U$$
>where $U$ is [[Open Set]] in $X$ as [[Unions and Intersections Commute]].
>Suppose there is an [[Open Set]] [[Set]] $U$ of $X$ with $G=U\cap Y$. For each $x\in G$ pick $\epsilon>0$ such that $B_{d_{X}}(x,\epsilon_{x})\subseteq U$. Then,
>$$G = Y\cap U=Y\cap\bigcup_{x\in U}B_{d_{X}}(x,\epsilon_x)=Y\cap\bigcup_{x\in G}B_{d_{Y}}(x,\epsilon_x)=\bigcup_{x\in G}B_{d_{Y}}(x,\epsilon_{x})$$
>so, $G$ is a [[Union]] of [[Open Set]] [[Ball]]s in $Y$, so $G$ is [[Open Set]] in $Y$.
>
>(b) Let $A$ be [[Closed Set]] in $Y$. 
Then, pick $Y-A$ is [[Open Set]] in $Y$, so pick $U\subseteq X$ such that $Y-A=U\cap Y$ and $U$ is [[Open Set]] by (a). Then
$$A=Y-(Y-A)=Y-(U\cap Y)$$
As $U\cap Y$ is [[Open Set]] in $Y$ by (a), $A$ is the [[Compliment]] of a [[Open Set]] set in $Y$, so $A$ is [[Closed Set]] in $Y$.
Suppose $A=Y\cap F$ where $F$ is [[Closed Set]] in $X$. Then,
$$A=Y-(Y-Y\cap F)$$
Claim: 
$$Y-Y\cap F=Y\cap(X-F)$$
Justification: Let $x\in Y-Y\cap F$ be given. Then, $x\in Y\subseteq X$ and $x\notin F$, so $x\in X-F$. $\therefore x\in Y\cap(X-F)$. Let $x\in Y\cap(X-F)$ be given. $x\in X-F$, so $x\notin F$, so $x\notin Y\cap F$. A $x\in Y$, $x\in Y- Y\cap F$.
So, 
$$A=Y-(Y\cap(X-F))$$
As $F$ is [[Closed Set]], $X-F$ is [[Open Set]], so $Y\cap(X-F)$ is [[Open Set]] in $Y$ by (a). As the [[Compliment]] of an [[Open Set]] set is [[Closed Set]], $A$ is [[Closed Set]] in $Y$.

>[!note] 6
>Let $(X,d)$ be a [[Metric Space]], let $Y\subseteq X$. Now consider the [[Metric Space]] $(Y,d)$ with $Z\subseteq Y$. Then, let $H$ be [[Open Set]] in the [[Subspace]] $Z$. Then, there exists an [[Open Set]] [[Set]] $H_{1}\subseteq Y$ such that 
>$$H=H_{1}\cap Z$$
>Suppose the set $H_{1}$ is [[Open Set]] in $Y$. Then,
>$$H=H_{1}\cap Z$$
>is [[Open Set]] in $Z$. (5.a/definition of [[Subspace Topology]])
>Let $D$ be [[closed Set]] in the [[Subspace]] $Z$. Then, there exists an [[closed Set]] [[Set]] $D_{1}\subseteq Y$ such that 
>$$D=D_{1}\cap Z$$
>Suppose the set $D_{1}$ is [[closed Set]] in $Y$. Then,
>$$D=D_{1}\cap Z$$
>is [[closed Set]] in $Z$. (5.b/[[Closed Sets in Subspace Theorem]])

>[!note] 8
>Let $x\in \text{int}\left[\bigcap A_{k}\right]$ be given. Note: $x\in A_{k}$ for all $k$. Pick $\epsilon>0$ such that 
>$$B_{d}(x,\epsilon)\subseteq \text{int}\left[\bigcap A_{k}\right]\subseteq\bigcap A_{k}$$
>So, $B_{d}(x,\epsilon)$ is contained in each $A_{k}$, a [[Neighborhood]] of $x$ is contained in $\bigcap A_k$.
>[[therefore]] $\text{int}\left[\bigcap A_{k}\right]\subseteq\bigcap \text{int}A_{k}$. 
>Let $x\in\bigcap \text{int}A_{k}$ be given. For each $k$, pick $\epsilon_{k}>0$ such that 
>$$B_{d}(x,\epsilon_{k})\subseteq A_k$$
>Let
>$$\epsilon=\min\{\epsilon_{k}:1≤k≤n\}$$
>For all $k$, 
>$$B_{d}(x, \epsilon)\subseteq B_{d}(x,\epsilon_k)\subseteq A_k$$
>So, $B_{d}(x, \epsilon)\subseteq\bigcap A_{k}$. As $x$ is contained in an [[Open Set]] set contained in the [[Intersection]], $x\in \text{int}\left[\bigcap A_{k}\right]$.
>[[therefore]] $\bigcap \text{int}A_{k}\subseteq \text{int}\bigcap A_{k}$.
>

>[!note] Prove prop 1.1.11
>(a) Let $F_{1},\ldots, F_{n}$ be [[Closed Set]]. Then, 
>$$\bigcup_{k=1}^{n} F_{k}=\bigcup_{k=1}^{n}(X - (X - F_{k})) = X - \bigcap_{k=1}^{n} (X - F_{k})$$
>by [[DeMorgan's Laws]]. $X-F_{k}$ is [[Open Set]] for each $k$, so the finite [[Intersection]] of open sets: $\bigcap(X-F_{k})$ is [[Open Set]]. [[therefore]] $X-\bigcap X_{k}$ is [[Closed Set]]. 
>
>(b) Let $\{F_{i}:i\in I\}$ be a collection of [[Closed Set]] sets. Then, 
>$$\bigcap_{i\in I} F_{i}=\bigcap_{i\in I}(X - (X - F_{i})) = X - \bigcup_{i\in I} (X - F_{i})$$
>by [[DeMorgan's Laws]]. $X-F_{i}$ is [[Open Set]] for each $i$, so the arbitrary [[Union]] of open sets: $\bigcup(X-F_{i})$ is [[Open Set]]. [[therefore]] $X-\bigcup X_{i}$ is [[Closed Set]]. 
