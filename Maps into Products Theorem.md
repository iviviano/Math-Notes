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
Suppose $f$ is [[Continuous]]. Let $V$ be [[Open Set]] in $X$. Then, 
$$f^{-1}(V\times\emptyset)=f_{1}^{-1}(V)\cup f_{2}^{-1}(\emptyset)=f_{1}^{-1}(V_{1})$$
As $V$ is [[Open Set]] in $X$, $V\times\emptyset$ is [[Open Set]] in $X\times Y$, so $f^{-1}(V\times\emptyset)=f_{1}^{-1}(V)$ is [[Open Set]] in $A$.
[[therefore]] $f_{1}$ is [[Continuous]]. Parallel reasoning shows that $f_{2}$ is also [[Continuous]].
