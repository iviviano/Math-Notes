<p align=center>
Topology<br>
Problem Set 5<br>
Isaac Viviano
</p>

---

>[!note] 1.5.4
Suppose that $\chi_A$ is [[Continuous]]. As $\{1\}$ is [[Closed Set]] in $\mathbb{R}$, and $\chi^{-1}(\{1\})=A$, $A$ is [[Closed Set]] $X$ as [[Preimage]]s of [[Closed Set]] sets under continuous functions are closed by the [[Characterizations of Continuity Theorem]]. Similarly, $X-A$ is [[Closed Set]] in $X$ as $\chi_{A}^{-1}(\{0\})=X-A$. So, $A$ is both open and closed in $X$.
>
Suppose that $A$ is both [[Open Set]] and [[Closed Set]] in $X$. I will show that the [[Preimage]] of any [[Closed Set]] [[Subset]] of $\mathbb{R}$ is [[Closed Set]]. Let $V$ be [[Closed Set]] in $\mathbb{R}$. Suppose that $1,0\in V$. Then, $\chi_{A}^{-1}(V)=X$ which is [[Closed Set]] in $X$. Suppose that $1\notin V,0\in V$. Then, $\chi_{A}^{-1}(V)=X-A$ is [[Closed Set]] in $X$ as $A$ is [[Open Set]]. Suppose that $0\notin V,1\in V$. Then, $\chi_{A}^{-1}(V)=A$ is [[Closed Set]] in $X$. Otherwise, $0,1\notin V$. So, $\chi_{A}^{-1}(V)=\emptyset$ is [[Closed Set]] in $X$. [[therefore]] $\chi_{A}^{-1}(V)$ is [[Closed Set]] in $X$, so $\chi_{A}$ is [[Continuous]] by the [[Characterizations of Continuity Theorem]].

>[!note] 1.5.5
(a) $\chi_{A}\chi_{B}$ maps $x$ to $1$ [[iff]] $\chi_{A}(x)=\chi_{B}(x)=1$, which is equivalent to $x\in A,x\in B$, so $$\chi_{A}\chi_{B}=\chi_{A\cap B}$$
(b) $\chi_{A}+\chi_{B}$ maps $x$ to $0$ [[iff]] $\chi_{A}(x)=\chi_{B}(x)=0$. It maps $x$ to $1$ [[iff]] either $\chi_{A}(x)=1$ or $\chi_{B}(x)=1$ but not both. It maps $x$ to $2$ only if $\chi_{A}(x)=1$ and $\chi_{B}(x)=1$. The [[Rule of Assignment]] is given by: $$\chi_{A}+\chi_{B}=\left\{
\begin{align}
&0\text{ if }x\notin A\cup B\\
&1\text{ if }x\in A\cup B-A\cap B\\
&2 \text{ if }x\in A\cap B\\
\end{align}\right.$$
This is equivalent to $$\chi_{A}+\chi_{B}=\chi_{A\cup B}+\chi_{A\cap B}$$
>
(c) $\chi_{\emptyset}$ is just the constant $0$ [[Function]] on $X$, since for all $x\in X,x\notin \emptyset$.


>[!note] 2.1.1
Let $X$ be a [[Topological Space]] satisfying the [[Hausdorff Axiom]]. Let $x,y\in X$ be given. $y\in X-\{x\}$. Pick [[Neighborhood]]s $U,V$ of $x,y$ respectively, such that $U\cap V=\emptyset$. As $x\notin V$, $V\subseteq X-\{x\}$. So, $X-\{x\}$ is [[Open Set]]. [[therefore]] $\{x\}$ is [[Closed Set]].

>[!note] 2.1.2
Let $\{(X_{i},T_{i}):i\in I\}$ be a [[Collection]] of [[Topological Space]]s where $X_{i}$ are [[Pairwise Disjoint]] sets and $$X=\bigcup_{i\in I} X_{i}$$Let $T=\{U\subseteq X:U\cap X_{i}\in T_{i}\}$. As $\emptyset\subseteq X$ and $\emptyset\in T_{i}$ for all $i\in I$, $\emptyset\in T$. As $X\subseteq X$ and $X_{i}=X\cap X_{i}\in T_{i}$ for all $i\in I$, $X\in T$.
>
Let $\mathcal{U}\subseteq T$ be given. For each $U\in \mathcal{U}$, for all $i\in I$, $U\cap X_{i}\in T_{i}$. Note: $$\bigcup_{i\in I}U\cap X_{i}=U\cap\bigcup_{i\in I}X_{i}=U\cap X=U$$
Then, $$\bigcup_{U\in \mathcal{U}}U=\bigcup_{U\in \mathcal{U}}\left(\bigcup_{i\in I}U\cap X_{i}\right)=\bigcup_{i\in I}\left(\bigcup_{U\in \mathcal{U}}U\cap X_{i}\right)$$As $T_i$ is a [[Topology]] and $U\cap X_{i}\in T_{i}$, $$\bigcup_{U\in \mathcal{U}}U\cap X_{i}=U_{i}\in T_{i}$$Let $$U=\bigcup_{i\in I}U_{i}=\bigcup_{U\in \mathcal{U}}U$$As $X_{i}$ are [[Pairwise Disjoint]], $U\in T$.
>
Let $U_{1},U_{2}\in T$. Then, $$\begin{align}
U_{1}\cap U_{2}&=\left(\bigcup_{i\in I} U_{1}\cap X_{i}\right) \cap\left(\bigcup_{i\in I} U_{2}\cap X_{i}\right)=\bigcup_{i\in I}\left(U_{1}\cap X_{i}\right)\cap(U_{2}\cap X_{i})\\
\end{align}$$ 
>As $(U_{1}\cap X_{i})\in T_{i}$ and $(U_{2}\cap X_{i})\in T_i$ ($T_i$ is a [[Topology]]), $U_{1}\cap U_{2}\cap X_{i}=(U_{1}\cap X_{i})\cap(U_{2}\cap X_{i})\in T_{i}$. As $X_{i}$ are [[Pairwise Disjoint]], $$U=\bigcup_{i\in I}U_{1}\cap U_{2}\cap X_{i}=U_{1}\cap U_{2}\in \mathcal{T}$$
[[therefore]] $T$ is a [[Topology]].

>[!note] 2.1.6
(a) 
>>[!proof]
Let $A$ be [[Closed Set]]. Let $x\in A$. As $x\in A$ and $A$ is [[Closed Set]], $x$ is in all [[Closed Set]] [[Set]]s containing $A$, so $x\in\bar{A}$. Let $x\in\bar{A}$. Then, $x$ is in all [[Closed Set]] sets containing $A$. As $A$ is a [[Closed Set]] set containing $A$, $x\in A$. [[therefore]] $A=\bar{A}$
Let $A=\bar{A}$. $\bar{A}$ is an [[Intersection]] of [[Closed Set]] sets, so it is [[Closed Set]] by the [[Closed Characterization of Topology Theorem]]. [[therefore]] $A$ is [[Closed Set]].
>
(b)
>>[!proof]
Let $A$ be [[Open Set]] in $X$. Let $x\in A$. As $x\in A$ and $A$ is [[Open Set]], $X$ is in an [[Open Set]] [[Set]] contained in $A$, so $x\in \text{int } A$. Let $x\in \text{int }A$. Then, $x$ is in an [[Open Set]] set contained in $A$, so $x\in A$. [[therefore]] $A=\text{int }A$.
Let $A=\text{int }A$. $\text{int }A$ is a [[Union]] of [[Open Set]] sets. [[therefore]] $A$ is [[Open Set]].
>
(c) 
>>[!proof]
Let $x\in \text{cl }[\bigcup A_{k}]$. Then, $x$ is in every [[Closed Set]] set containing $\bigcup A_{k}$. If $C_{k}$ are [[Closed Set]] for each $k$ and $A_{k}\subseteq C_{k}$, then $\bigcup C_{k}$ is [[Closed Set]] and contains $\bigcup A_{k}$, so $x\in\bigcup C_{k}$.
[[therefore]] $x\in\bigcup \text{cl }A_{k}$. 
Let $x\in \text{cl }A_{k}$ be given. Then, if $C$ is a [[Closed Set]] set containing $\bigcup A_k$, then for each $k$, $A_{k}\subseteq C$. So, $x\in C$
[[therefore]] $x\in \text{cl }\bigcup A_k$