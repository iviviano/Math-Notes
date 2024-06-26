---
tag: topology
mathLink: maps into products theorem
---
> [!thm]
> Let $f:A\rightarrow X$ [[notation for cartesian product]] $Y$ be given by the [[Rule of Assignment]]:
> $$f(a) = (f_1(a), f_2(a))$$
> 
> Then, $f$ is [[Continuous]] [[iff]] the [[Function]]s
> $$f_1:A\rightarrow X\text{   and   }f_2 :A\rightarrow Y$$
> 
> are [[Continuous]]. The maps $f_1$ and $f_2$ are called the *coordinate functions* of $f$.

>[!proof]
> Assume the coordinate functions are continuous. Then, if $V_1$ is [[Open Set]] in $X$ and $V_2$ is [[Open Set]] in $Y$, the set 
> $$U = f^{-1}(V_1\times V_2) = f_1^{-1}(V_1)\cup f_2^{-1}(V_2)$$
> is [[Open Set]] in $A$. [[therefore]] $f$ is [[Continuous]].
> 
Suppose $f$ is [[Continuous]]. Then, $\pi_{1}\circ f$ is [[Continuous]] by the [[Constructing Continuous Functions Theorem]]. As $f_{1}=\pi_{1}\circ f$, $f_{1}$ is [[Continuous]].
