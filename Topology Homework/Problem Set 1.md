<p align="center">
Topology <br>
Problem Set 1 <br>
Isaac Viviano
</p>
---

I will use the following proposition to prove proposition 1.1.5, which I do not think is in the book.
>[!prop] Proposition: Unions and Intersections Commute (When One is Binary)
Let $\mathcal{A}$ be a collection of [[Set]]s, let $B$ be a set. Then,
$$B\cap\bigcup_{A\in \mathcal{A}}A=\bigcup_{A\in \mathcal{A}}B\cap A$$
and
$$B\cup\bigcap_{A\in \mathcal{A}}A=\bigcap_{A\in \mathcal{A}}B\cup A$$

>[!proof]
Let $x\in B\cap\bigcup A$ be given. Then, pick $A_0\in \mathcal{A}$ such that $x\in A_{0}$. $x\in B$, so $x\in A_{0}\cap B$. As $A_{0}\in A$, 
$$x\in\bigcup_{A\in \mathcal{A}}B\cap A$$
Let $x\in\bigcup B\cap A$. Then, pick $A_{0}\in \mathcal{A}$ such that $x\in A_{0}\cap B$. As $x\in A_{0}$, $x\in \bigcup A$. As $x\in B$ as well,
$$x\in B\cap\bigcup_{A\in \mathcal{A}}A$$
$$\therefore B\cap\bigcup_{A\in \mathcal{A}}A=\bigcup_{A\in \mathcal{A}}B\cap A$$
Let $x\in B\cup\bigcap A$. Suppose $x\in B$. Then,
$$\forall A\in \mathcal{A}:x\in B\cup A$$
Suppose $x\in\bigcap A$. Then,
$$\forall A\in \mathcal{A}:x\in B\cup A$$
so,
$$x\in \bigcap_{A\in \mathcal{A}}B\cup A$$
Let $x\in \bigcap B\cup A$ be given. Then, $\forall A\in \mathcal{A}:x\in B\cup A$. Suppose $x\in B$. Then, $x\in B\cup\bigcap A$. Suppose $x\notin B$. Then, for all $A\in \mathcal{A}:x\in A$. [[therefore]] $x\in\bigcap A$, so $x\in B\cup\bigcap_{A\in \mathcal{A}}A$.
$$\therefore B\cup\bigcap_{A\in \mathcal{A}}A=\bigcap_{A\in \mathcal{A}}B\cup A$$

>[!note] 1.1.5
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

>[!note] 1.1.8
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

>[!note] Prove prop 1.1.11
>(a) Let $F_{1},\ldots, F_{n}$ be [[Closed Set]]. Then, 
>$$\bigcup_{k=1}^{n} F_{k}=\bigcup_{k=1}^{n}(X - (X - F_{k})) = X - \bigcap_{k=1}^{n} (X - F_{k})$$
>by [[DeMorgan's Laws]]. $X-F_{k}$ is [[Open Set]] for each $k$, so the finite [[Intersection]] of open sets: $\bigcap(X-F_{k})$ is [[Open Set]]. [[therefore]] $X-\bigcap X_{k}$ is [[Closed Set]]. 
>
>(b) Let $\{F_{i}:i\in I\}$ be a collection of [[Closed Set]] sets. Then, 
>$$\bigcap_{i\in I} F_{i}=\bigcap_{i\in I}(X - (X - F_{i})) = X - \bigcup_{i\in I} (X - F_{i})$$
>by [[DeMorgan's Laws]]. $X-F_{i}$ is [[Open Set]] for each $i$, so the arbitrary [[Union]] of open sets: $\bigcup(X-F_{i})$ is [[Open Set]]. [[therefore]] $X-\bigcup X_{i}$ is [[Closed Set]]. 

>[!note] 7: Prove the [[Interior, Closure, and Boundary Proposition]] for [[Metric Space]]s
>>[!proof] Proof of 1.
>>Let $A$ be [[Closed Set]]. Let $x\in A$. As $x\in A$ and $A$ is [[Closed Set]], $x$ is in all [[Closed Set]] [[Set]]s containing $A$, so $x\in\bar{A}$. Let $x\in\bar{A}$. Then, $x$ is in all [[Closed Set]] sets containing $A$. As $A$ is a [[Closed Set]] set containing $A$, $x\in A$. [[therefore]] $A=\bar{A}$
>>Let $A=\bar{A}$. $\bar{A}$ is an [[Intersection]] of [[Closed Set]] sets, so it is [[Closed Set]]. [[therefore]] $A$ is [[Closed Set]].
>
>>[!proof] Proof of 2.
>>Let $A$ be [[Open Set]] in $X$. Let $x\in A$. As $x\in A$ and $A$ is [[Open Set]], $x$ is in an [[Open Set]] [[Set]] contained in $A$, so $x\in \text{int } A$. Let $x\in \text{int }A$. Then, $x$ is in an [[Open Set]] set contained in $A$, so $x\in A$. [[therefore]] $A=\text{int }A$.
>>Let $A=\text{int }A$. $\text{int }A$ is a [[Union]] of [[Open Set]] sets. [[therefore]] $A$ is [[Open Set]].

My proof of (a) of 1.2.5 uses the following theorem which I don't think is in our textbook.
> [!thm]
> Let $A$ be a [[Subset]] of the [[Topological Space]] $X$.
> 1. Then $x\in$ [[notation for closure]] [[iff]] every [[Open Set]] set $U$ containing $x$ [[Intersects]] $A$ (Every [[Neighborhood]] of $x$ [[Intersects]] $A$)

> [!proof]
> 1. Suppose $x\in\bar{A}$. Then $x$ is in every [[Closed Set]] set containing $A$. So, if an [[Open Set]] set $U$ contains $x$, its [[Compliment]] does not contain $A$, so $U$ [[Intersects]] $A$.
> Suppose every [[Open Set]] set containing $x$ [[Intersects]] $A$. Then, no [[Closed Set]] set containing $A$ does not contain $x$. Therefore, $x\in$ [[notation for closure]]
> 

>[!note] 1.2.5
>(a) Prove that $x\in \text{cl }A$ [[iff]] $x$ is either a [[Limit Point]] of $A$ or an isolate point of $A$.
>>[!proof]
>>Suppose $x\in \text{cl }A$. Then, for all $\epsilon>0$, $B_{d}(x,\epsilon)$ [[Intersects]] $A$ by the [[Open Sets Intersecting the Closure Intersect the Set Theorem]]. Suppose additionally that for all $\epsilon>0$
>>$$B_{d}(x,\epsilon)\cap (A-\{x\})≠\emptyset$$
>>Then, $x$ is a [[Limit Point]] of $A$. Otherwise, pick $\epsilon>0$ such that $B_{d}(x,\epsilon)\cap(A-\{x\})=\emptyset$. As $B_{d}(x,\epsilon)\cap A≠\emptyset$, $x\in A$. but is not a limit point. 
>>[[therefore]] $x$ is a [[Limit Point]] of $A$ or $x$ is an [[Isolated Point]] of $A$.
>>
>>Suppose $x$ is a limit point of $A$. Then, for all $\epsilon>0$, 
>>$$B_{d}(x,\epsilon)\cap (A-\{x\})\ne\emptyset$$
>>Let $U$ be any [[Neighborhood]] of $x$. Then, there exists an $\epsilon>0$ such that $B_{d}(x,\epsilon)\subseteq U$. So any [[Neighborhood]] of $x$ [[Intersects]] $A$ at some point besides $x$. [[therefore]] $x\in U$ by the [[Open Sets Intersecting the Closure Intersect the Set Theorem]].
>>Suppose $x$ is an [[Isolated Point]] of $A$. Then, $x\in A$, so $x\in\bar{A}$.
>
>
>(b) Show that a set having no [[Limit Point]]s is [[Closed Set]]:
>Let $A$ be a set of only [[Isolated Point]]s. Then, for all $x\in \bar{A}$, $x\in A$. So, $\bar{A}\subseteq A$. As $A\subseteq \bar{A}$, $A=\bar{A}$, so $A$ is [[Closed Set]] by the [[Interior, Closure, and Boundary Proposition]].
>(c) $\mathbb{N}$ is an infinite [[Subset]] of $\mathbb{R}$ with no [[Limit Point]]s