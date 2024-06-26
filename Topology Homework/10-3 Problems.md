From 1.5: 4, 5

>[!note] 4
Suppose that $\chi_A$ is [[Continuous]]. As $\{1\}$ is [[Closed Set]] in $\mathbb{R}$, and $\chi^{-1}(\{1\})=A$, $A$ is [[Closed Set]] $X$ as [[Preimage]]s of [[Closed Set]] sets under continuous functions are closed by the [[Characterizations of Continuity Theorem]]. Similarly, $X-A$ is [[Closed Set]] in $X$ as $\chi_{A}^{-1}(\{0\})=X-A$. So, $A$ is both open and closed in $X$.
>
Suppose that $A$ is both [[Open Set]] and [[Closed Set]] in $X$. I will show that the [[Preimage]] of any [[Closed Set]] [[Subset]] of $\mathbb{R}$ is [[Closed Set]]. Let $V$ be [[Closed Set]] in $\mathbb{R}$. Suppose that $1,0\in V$. Then, $\chi_{A}^{-1}(V)=X$ which is [[Closed Set]] in $X$. Suppose that $1\notin V,0\in V$. Then, $\chi_{A}^{-1}(V)=X-A$ is [[Closed Set]] in $X$ as $A$ is [[Open Set]]. Suppose that $0\notin V,1\in V$. Then, $\chi_{A}^{-1}(V)=A$ is [[Closed Set]] in $X$. Otherwise, $0,1\notin V$. So, $\chi_{A}^{-1}(V)=\emptyset$ is [[Closed Set]] in $X$. [[therefore]] $\chi_{A}^{-1}(V)$ is [[Closed Set]] in $X$, so $\chi_{A}$ is [[Continuous]] by the [[Characterizations of Continuity Theorem]].

>[!note] 5
>
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
