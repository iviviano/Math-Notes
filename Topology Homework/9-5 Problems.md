From section 1.1: 5, 6, 8, prove prop 1.1.11

>[!note] 5
>Prove 1.1.8: Let $(X,d)$ be a [[Metric Space]], and let $Y$ be a [[Subset]] of $X$
>(a) Suppose $G$ is [[Open Set]] in the [[Subspace]] $Y$. Then, for each $x\in G$, there is a [[Ball]] in $Y$ $B_{d_Y}(x,\epsilon_x)\subseteq G$. Then, 
>$$B_{d_{Y}}(x,\epsilon_{x})=Y\cap B_{d_{X}}(x,\epsilon_x)$$ 
>Then, 
>$$G=\bigcup_{x\in G}B_{d_{Y}}(x,\epsilon_x)=\bigcup_{x\in G}\left(Y\cap B_{d_{X}}(x,\epsilon_{x})\right)=Y\cap U$$
>where $U$ is [[Open Set]] in $X$.
>Suppose there is an [[Open Set]] [[Set]] $U$ of $X$ with $G=U\cap Y$. For each $x\in G$ pick $\epsilon>0$ such that $B_{d_{X}}(x,\epsilon_{x})\subseteq U$. Then,
>$$G = Y\cap U=Y\cap\bigcup_{x\in U}B_{d_{X}}(x,\epsilon_x)=Y\cap\bigcup_{x\in G}B_{d_{Y}}(x,\epsilon_x)=\bigcup_{x\in G}B_{d_{Y}}(x,\epsilon_{x})$$
>so, $G$ is a [[Union]] of [[Open Set]] [[Ball]]s in $Y$, so $G$ is [[Open Set]] in $Y$.
>
>(b) Let $A$ be [[Closed Set]] in $Y$. Pick $U\in X$ such that $U$ is [[Open Set]] in $X$ and 
>$$A=U^{c}\cap Y$$
>by (a).
>Then,
>$$Y-A=Y-(Y\cap (X-U))=(Y-Y)\cup(Y-(X-U))=Y-(X-U)$$
>by [[DeMorgan's Laws]]
>Claim:
>$$Y-(X-U)=Y\cap U$$
>let $x\in Y-(X-U)$ be given. Then, $x\in Y$ and if $x\notin U^{c}$, so $x\in U$. So,
>$$Y-(X-U)\subseteq Y\cap U$$
>Let $x\in Y\cap U$ be given. Then $x\in U$, so $x\notin X-U$. As $x\in Y$ as well, $x\in Y-(X-U)$. So,
>$$Y-(X-U)\supseteq Y\cap U$$
>$$\therefore Y-A= Y\cap U$$
>So, $Y-A$ is [[Open Set]] in $Y$, and $A$ is [[Closed Set]] in $Y$.
>
>Now, suppose there is a [[Closed Set]] subset of $X$, $U$, such that 
>$$A=U\cap Y$$
>Then, 
>$$Y-A=Y-U\cap Y=Y-(X-U)$$
>As $X-U$ is [[Open Set]] in $X$, $Y-A$ is [[Open Set]] in $Y$ by (a), so $A$ is [[Closed Set]] in $Y$.

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
>Let $x\in\bigcap \text{int}A_{k}$ be given. Let
>$$E=\{\epsilon_{k}>0:B_{d}(x,\epsilon_{k})\subseteq A_k\}$$
>Taking $\epsilon=\min(E)$, for all $k$, 
>$$B_{d}(x, \epsilon)\subseteq A_k$$
>So, $B_{d}(x, \epsilon)\subseteq\bigcap A_{k}$. As $x$ is contained in an [[Open Set]] set contained in the [[Intersection]], $x\in \text{int}\left[\bigcap A_{k}\right]$.
>[[therefore]] $\bigcap \text{int}A_{k}\subseteq \text{int}\bigcap A_{k}$.
>

>[!note] Prove prop 1.1.11
>(a) Let $F_{1},\ldots, F_{n}$ be [[Closed Set]]. Then, 
>$$\bigcup F_{k}=\bigcup(X - (X - F_{k})) = X - \bigcap (X - F_{k})$$
>by [[DeMorgan's Laws]]. $X-F_{k}$ is [[Open Set]] for each $k$, so the finite [[Intersection]] of open sets: $\bigcap(X-F_{k})$ is [[Open Set]]. [[therefore]] $X-\bigcap X_{k}$ is [[Closed Set]]. 
>(b) Let $\{F_{i}:i\in I\}$ be a collection of sets. Then, 
>$$\bigcap F_{i}=\bigcap(X - (X - F_{i})) = X - \bigcup (X - F_{i})$$
>by [[DeMorgan's Laws]]. $X-F_{i}$ is [[Open Set]] for each $i$, so the arbitrary [[Union]] of open sets: $\bigcup(X-F_{i})$ is [[Open Set]]. [[therefore]] $X-\bigcup X_{i}$ is [[Closed Set]]. 



