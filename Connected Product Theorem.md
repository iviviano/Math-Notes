---
tag: topology
mathLink: connected product theorem
---
>[!thm]
Let $\{X_{i}:i\in I\}$ be a [[Collection]] of [[Topological Space]]s. Then, if the [[Cartesian Product]] $X$ is given the [[Product Topology]], $X$ is [[Connected]] [[iff]] $X_i$ is [[Connected]] for all $i\in I$.

>[!note]
>This is probably not true if $X$ is given the [[Box Topology]], as the proof of the [[Dense Subsets of Product Spaces Lemma]] uses this fact.

>[!proof]
If $X$ is [[Connected]], then each $X_{i}$ is [[Connected]] as it is the [[Image Set]] of a [[Projection]] map.
>
Claim: Finite products of [[Connected]] [[Topological Space]]s are [[Connected]]. 
Let $X,Y$ be [[Connected]]. Fix $y_{0}\in Y$. Then, $$X\times Y=\bigcup_{x\in X}(X\times\{y_{0}\}\cup\{x\}\times Y)$$$X\times\{y_0\}$ is [[Connected]] by the [[Intermediate Value Theorem]], since it is [[Homeomorphic]] to $X$. Similarly, $\{x\}\times Y$ is [[Connected]] for all $x\in X$. And, $X\times \{y_{0}\}\cap\{x\}\times Y$ contains $(x,y_{0})$. So, $X\times Y$ is [[Connected]] as [[Unions of Overlapping Connected Sets are Connected]]. Therefore, any finite [[Cartesian Product]] of finitely many [[Connected]] [[Topological Space]]s is [[Connected]] by [[Principle of Mathematical Induction]].
>
Now suppose $I$ is infinite. Fix $p_{i}\in X_{i}$ for each $i\in I$. Define $$Y=\{x:I \rightarrow X|\{i:x(i)≠p_{i}\}\text{ is finite}\}$$by the [[Dense Subsets of Product Spaces Lemma]], $Y$ is [[Dense]] in $X$. For all finite [[Subset]]s $F\subseteq I$, define $$Y_{F}=\{x\in X|\forall i\not\in F:x(i)=p_{i}\}$$Then, $$Y_{F}\approx\prod_{i\in F}X_{i}$$Since $F$ is [[Connected]], $Y_{F}$ is [[Connected]]. All $Y_{F}$ contain $p$. So, $$Y=\bigcup_{\text{finite }F\subseteq I}Y_{F}$$is [[Connected]]. Since $Y$ is [[Dense]] in $X$, $\text{cl }Y=X$. But, $\text{cl }Y$ is [[Connected]] by the [[Closure of Connected Sets Proposition]]. Therefore, $X$ is [[Connected]]. 
