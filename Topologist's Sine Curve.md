>[!def]
>Graph of $$f(x)=\begin{cases}\sin\left(\frac{1}{x}\right)\text{ if }0<x<1 \\
0\text{ if }x=0\end{cases}$$in $\mathbb{R}^{2}$.

>[!prop]
>This is [[Connected]] but not [[Locally Connected]].

>[!proof]
Let $X=A\cup B$ with $A,B$ [[Open Set]] and [[Disjoint]]. Suppose $\left(x,\sin\left(\frac{1}{x}\right)\right)\in B$ for some $x>0$. Then $(x,f(x))\in B$ for all $x>0$, since it is the [[Continuous]] [[Image]] of $[0,1]$. If $A$ were not empty, then $A=\{0\}$. But any [[Open Set]] [[Set]] containing $(0,0)$. But, any [[Open Set]] [[Set]] containing $(0,0)$ also contains $(\frac{1}{n\pi},\sin(n \pi))$ for sufficiently large $n$. So, $A$ is empty or $A\cap B\ne\emptyset$, proving that $X$ is [[Connected]].
>
Any [[Neighborhood]] of $(0,0)$ has some [[Disjoint]] squiggles. So, $X$ is not [[Locally Connected]].

