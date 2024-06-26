>[!thm]
If $\{X_{i}:i\in I\}$ are [[Regular]] [[Topological Space]]s, then $$X=\prod_{i\in I}X_{i}$$

>[!proof]
Let $G$ be [[Open Set]] in $X$ and $x\in G$. Then, there are indices $i_{1},\ldots,i_{n}$ and [[Open Set]] [[Set]]s $V_{i_{k}}\subseteq X_{i_{k}}$ such that $$x\in\bigcap_{k=1}^{n}\pi_{i_{k}}^{-1}(V_{i_{k}})\subseteq G$$Since each [[Topological Space]] $X_{i_{k}}$ is [[Regular]], there exists an [[Open Set]] [[Set]] $U_{i_{k}}\subseteq X_{i_{k}}$ with $\pi_{i_{k}}(x)\in U_{i_{k}}$ and $U_{i_{k}}\subseteq \text{cl }U_{i_{k}}\subseteq  V_{i_{k}}$ by the [[Characterizations of Regular Spaces Proposition]]. Thus, $$x\in U=\bigcap_{k=1}^{n}\pi_{i_{k}}^{-1}(V_{i_{k}})\subseteq \text{cl }U\subseteq\bigcap_{k=1}^{n}\pi_{i_{k}}^{-1}(\text{cl }(U_{i_{k}}))\subseteq \bigcap_{k=1}^{n}\pi_{i_{k}}^{-1}(V_{i_{k}}\subseteq G)$$So, $X$ is [[Regular]] by the [[Characterizations of Regular Spaces Proposition]].
