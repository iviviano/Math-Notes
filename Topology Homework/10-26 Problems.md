From 2.3: 5, 6

>[!note] 5
Let $X=X_{1}\times X_{2}$. 
>
Let $U\times V$ be a [[Basis of a Topology]] element of $X$ under the [[Product Topology]]. Then, for all $x_{1}\in U,x_{2}\in V$ there exists $\epsilon>0$ such that $$B_{d_{1}}(x_{1},\epsilon)\subseteq U \text{  and  }B_{d_{2}}(x_{2},\epsilon)\subseteq V$$as $U$ is [[Open Set]] in the [[Metric Space]] $X_{1}$ and $V$ is [[Open Set]] in the [[Metric Space]] $X_{2}$. Then, $$(x_{1},x_{2})\in B_{d}((x_{1},x_{2}),\epsilon) \subseteq B_{d_{1}}(x_{1},\epsilon)\times B_{d_{2}}(x_{2},\epsilon)\subseteq U\times V$$so the [[Metric Topology]] on $X$ is [[Finer]] than the [[Product Topology]] on $X$ by the [[Finer Bases Lemma]].
>
Let $(x_{1},x_{2})\in X,\epsilon>0$ be given. Then, $$(x_{1},x_{2})\in B_{d_{1}}\left(x_{1},\frac{\epsilon}{2}\right)\times B_{d_{2}}\left(x_{2},\frac{\epsilon}{2}\right)\subseteq B_{d}((x_{1},x_{2}),\epsilon)$$Clearly, $B_{d_{1}}\left(x_{1},\frac{\epsilon}{2}\right)$ is [[Open Set]] in the [[Metric Space]] $X_{1}$ and $B_{d_{2}}\left(x_{2},\frac{\epsilon}{2}\right)$ is [[Open Set]] in the [[Metric Space]] $X_{2}$, so $B_{d_{1}}\left(x_{1},\frac{\epsilon}{2}\right)\times B_{d_{2}}\left(x_{2},\frac{\epsilon}{2}\right)$ is a [[Basis of a Topology]] element of the [[Product Topology]] on $X$. [[therefore]] the [[Product Topology]] on $X$ is [[Finer]] than the [[Metric Topology]] on $X$ by the [[Finer Bases Lemma]].


>[!note] 6
Let $x\in X,\epsilon>0$ be given. Pick a [[Neighborhood]] $U$ of $x$ such that for all $a\in U$, $$|f(x)-f(a)|<\frac{\epsilon}{2\max\{|\sup(f(U))|,|\inf(f(U))|\}}$$Pick a [[Neighborhood]] $V$ of $x$ such that for all $a\in V$, $$|g(x)-g(a)|<\frac{\epsilon}{|2g(x)|}$$Then, if $a\in U\cap V$,$$\begin{split}|f(x)g(x)-f(a)g(a)|&=|f(x)g(x)-f(a)g(x)+f(a)g(x)-f(a)g(a)|\\
&\le|f(x)g(x)-f(a)g(x)|+|f(a)g(x)-f(a)g(a)|\\
&=|g(x)||f(x)-f(a)|+|f(a)||g(x)-g(a)|\\
&\le|g(x)||f(x)-f(a)|+|\max\{\sup(f(U\cap V),\inf(f(U\cap V)\}||g(x)-g(a)|\\
&<|g(x)| \frac{\epsilon}{|2g(x)|}+\max\{|\sup(f(U)|,|\inf(f(U)|\}|g(x)-g(a)|\\
&<\frac{\epsilon}{2} +\frac{\epsilon}{2}=\epsilon\end{split}$$
>
This shows that the [[Preimage]] of any [[Basis of a Topology]] element of $R$ is [[Open Set]] under $fg$. Therefore, $fg$ is continuous on $X$ by the [[Basis and Subbasis Formulation of Continuity]]. 

