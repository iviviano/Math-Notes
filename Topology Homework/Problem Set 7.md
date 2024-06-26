<p align=center>
Topology <br>
Problem Set 7 <br>
Isaac Viviano
</br>

---

>[!note] 2.3.2
Let $X=[0,1]$ be equipped with the [[Metric Topology]] and $W=\{0,1\}$ have the [[Discrete Topology]] given by the [[Metric]] $\rho$. Let $A=[0,\frac{1}{2}),B=[\frac{1}{2},1]$. Clearly, $X=A\cup B$. Define $g:A \rightarrow W$ and $h:B \rightarrow W$ by $$\begin{align}
\forall x\in A:h(x)=0\\
\forall x\in B:g(x)=1\\
\end{align}$$
and let $f$ be given by the [[Pasting Lemma]]. Pick $\epsilon>0$ with $\epsilon<1$. Then, for all $\delta>0$ there exists $x\in A$ such that $x\in B_{d}(\frac{1}{2},\epsilon)$ in $X$. Then, $\rho(f(\frac{1}{2}),x)=\rho(1,0)=1>\epsilon$, so $f$ is not [[Continuous]] by the [[Ep-de Formulation of Continuity]]

>[!note] 2.3.7
Let $X_{1}=\mathbb{R},X_{2}=\mathbb{R}^{3}$ and let $Z_{1}=Z_{2}=\mathbb{R}^{2}$. Then, $$X=Z=\mathbb{R}^{4}$$so, $X$ is homeomorphic to $Z$. However, $X_{1}$ is not homeomorphic to $Z_{1}$ or $Z_{2}$. Suppose $f:\mathbb{R}\rightarrow \mathbb{R}^{2}$ is a [[Homeomorphism]]. Then, $f^{-1}(\mathbb{R}^{2})=\mathbb{R}$. Let $y=f(0)$. Then, $f^{-1}(\mathbb{R}^{2}-\{y\})=\mathbb{R}-\{0\}$. $\mathbb{R}^{2}-\{y\}$ is [[Connected]], but $\mathbb{R}-\{0\}$ is not [[Connected]]. As the [[Image]] of a [[Connected]] [[Set]] under $f^{-1}$ is not [[Connected]], $f^{-1}$ cannot be [[Continuous]] by the [[Intermediate Value Theorem]]. [[therefore]] $f$ is not a [[Homomorphism]]. As $f$ was arbitrary, $X_{1}$ is not [[Homeomorphic]] to $Z_{1}$ or $Z_{2}$.

>[!note] 2.3.8
Let $X=\{a,b\}$. Let $f:X \rightarrow X$ have the [[Rule of Assignment]] $f(x)=a$. Give $X$ the [[Topology]] $$T=\{\emptyset ,\{a\},X\}$$Then, $f$ is an open map. However, $f(b)=\{a\}$. As $X-\{a\}=\{b\}$ is not open, $f$ is not a closed map.

>[!note] 2.3.5
Let $X=X_{1}\times X_{2}$. 
>
Let $U\times V$ be a [[Basis of a Topology]] element of $X$ under the [[Product Topology]]. Then, for all $x_{1}\in U,x_{2}\in V$ there exists $\epsilon>0$ such that $$B_{d_{1}}(x_{1},\epsilon)\subseteq U \text{  and  }B_{d_{2}}(x_{2},\epsilon)\subseteq V$$as $U$ is [[Open Set]] in the [[Metric Space]] $X_{1}$ and $V$ is [[Open Set]] in the [[Metric Space]] $X_{2}$. Then, $$(x_{1},x_{2})\in B_{d}((x_{1},x_{2}),\epsilon) \subseteq B_{d_{1}}(x_{1},\epsilon)\times B_{d_{2}}(x_{2},\epsilon)\subseteq U\times V$$so the [[Metric Topology]] on $X$ is [[Finer]] than the [[Product Topology]] on $X$ by the [[Finer Bases Lemma]].
>
Let $(x_{1},x_{2})\in X,\epsilon>0$ be given. Then, $$(x_{1},x_{2})\in B_{d_{1}}\left(x_{1},\frac{\epsilon}{2}\right)\times B_{d_{2}}\left(x_{2},\frac{\epsilon}{2}\right)\subseteq B_{d}((x_{1},x_{2}),\epsilon)$$Clearly, $B_{d_{1}}\left(x_{1},\frac{\epsilon}{2}\right)$ is [[Open Set]] in the [[Metric Space]] $X_{1}$ and $B_{d_{2}}\left(x_{2},\frac{\epsilon}{2}\right)$ is [[Open Set]] in the [[Metric Space]] $X_{2}$, so $B_{d_{1}}\left(x_{1},\frac{\epsilon}{2}\right)\times B_{d_{2}}\left(x_{2},\frac{\epsilon}{2}\right)$ is a [[Basis of a Topology]] element of the [[Product Topology]] on $X$. [[therefore]] the [[Product Topology]] on $X$ is [[Finer]] than the [[Metric Topology]] on $X$ by the [[Finer Bases Lemma]].

>[!note] 2.3.6
Let $x\in X,\epsilon>0$ be given. Pick a [[Neighborhood]] $U$ of $x$ such that for all $a\in U$, $$|f(x)-f(a)|<\frac{\epsilon}{2\max\{|\sup(f(U))|,|\inf(f(U))|\}}$$Pick a [[Neighborhood]] $V$ of $x$ such that for all $a\in V$, $$|g(x)-g(a)|<\frac{\epsilon}{|2g(x)|}$$Then, if $a\in U\cap V$,$$\begin{split}|f(x)g(x)-f(a)g(a)|&=|f(x)g(x)-f(a)g(x)+f(a)g(x)-f(a)g(a)|\\
&\le|f(x)g(x)-f(a)g(x)|+|f(a)g(x)-f(a)g(a)|\\
&=|g(x)||f(x)-f(a)|+|f(a)||g(x)-g(a)|\\
&\le|g(x)||f(x)-f(a)|+|\max\{\sup(f(U\cap V),\inf(f(U\cap V)\}||g(x)-g(a)|\\
&<|g(x)| \frac{\epsilon}{|2g(x)|}+\max\{|\sup(f(U)|,|\inf(f(U)|\}|g(x)-g(a)|\\
&<\frac{\epsilon}{2} +\frac{\epsilon}{2}=\epsilon\end{split}$$
>
This shows that the [[Preimage]] of any [[Basis of a Topology]] element of $R$ is [[Open Set]] under $fg$. Therefore, $fg$ is continuous on $X$ by the [[Basis and Subbasis Formulation of Continuity]]. 