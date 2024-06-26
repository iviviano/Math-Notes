From 2.4: 5, 6

>[!note] 5
Claim: the [[Connected]] [[Subset]]s of $\{0,1\}$ under the [[Discrete Topology]] are $\emptyset ,\{0\},\{1\}$. Obviously, these three sets are [[Connected]]. For each, the only subsets are the empty set and the set itself, so these are the only sets that are clopen in the [[Subspace]]s. $\{0\}$ is [[Open Set]] in $\{0,1\}$ as all sets are [[Open Set]] in the [[Discrete Topology]]. $\{0\}$ is [[Closed Set]] in $\{0,1\}$ as all [[Set]]s are [[Closed Set]] in the [[Discrete Topology]]. As $\{0\}$ is clopen, $\{0,1\}$ is not [[Connected]].
>
Suppose $X$ is [[Connected]]. Let $f:X \rightarrow \{0,1\}$ be [[Continuous]]. As $f$ is [[Continuous]] and $X$ is [[Connected]], $f(X)$ is [[Connected]] by the [[Intermediate Value Theorem]]. This implies that $f(X)\ne\{0,1\}$. Only if $X=\emptyset$ can $f(X)=\emptyset$. So, $f$ is constant by the claim.
>
Suppose that every continuous function from $X$ into $\{0,1\}$ is constant, and assume $X$ is not connected. So, $X=A\cup B$ where $A$ and $B$ are both [[Open Set]] or both [[Closed Set]], [[Disjoint]], and nonempty. Let $f:X \rightarrow \{0,1\}$ be given by the [[Rule of Assignment]] $$f(x)=\begin{cases}0\text{ if }x\in A \\
1\text{ if }x\in B\end{cases}$$Then, $f$ is [[Continuous]]: first assume $A, B$ both [[Open Set]]:
>- $f^{-1}(\emptyset )=\emptyset$ is [[Open Set]] in $X$
>- $f^{-1}(\{0\})=A$ is [[Open Set]] in $X$
>- $f^{-1}(\{1\})=B$ is [[Open Set]] in $X$
>- $f^{-1}(\{0,1\})=X$ is [[Open Set]] in $X$
>
so the [[Preimage]] of every [[Open Set]] [[Subset]] of $X$ is [[Open Set]] under $f$, so $f$ is [[Continuous]]. Now, if $A, B$ are both [[Closed Set]]:
>- $f^{-1}(\emptyset )=\emptyset$ is [[Closed Set]] in $X$
>- $f^{-1}(\{0\})=A$ is [[Closed Set]] in $X$
>- $f^{-1}(\{1\})=B$ is [[Closed Set]] in $X$
>- $f^{-1}(\{0,1\})=X$ is [[Closed Set]] in $X$
>
so the [[Preimage]] of every [[Closed Set]] [[Subset]] of $X$ is [[Open Set]] under $f$, so $f$ is [[Continuous]] by the [[Characterizations of Continuity Theorem]]. As $f$ is not constant since $A$ and $B$ are nonempty, this contradicts the assumption that $X$ is not [[Connected]].



Prove this with [[Intermediate Value Theorem]] and [[Unions of Overlapping Connected Sets are Connected]]

>[!note] 6
Let $X=\mathbb{R}^{2}$. Let $A=\{(x,y)\in \mathbb{R}^{2}:x^{2}+y^{2}=1,x\ge0\}$. $A$ is the [[Image]] of a [[Continuous]] [[Function]] $f:\mathbb{R}\rightarrow \mathbb{R}^{2}$ mapping $x\mapsto(\sqrt{1-x^{2}},x)$. As $\mathbb{R}$ is [[Connected]], $A=f(\mathbb{R})$ is [[Connected]] by the [[Intermediate Value Theorem]]. Let $B=\{(x,y)\in \mathbb{R}^{2}:x=0\}$. $B$ is the [[Image]] of the [[Continuous]] [[Function]] $f:\mathbb{R}\rightarrow \mathbb{R}^{2}$ mapping $x\mapsto(0,x)$. As $\mathbb{R}$ is [[Connected]], $B=f(\mathbb{R})$ is [[Connected]] by the [[Intermediate Value Theorem]]. Then, $A,B$ are [[Connected]]. However, $A\cap B=\{(0,1),(0,-1)\}$. As $\{(0,1)\}\cup\{(0,-1)\}=A\cap B$, $A\cap B$ is not connected.

