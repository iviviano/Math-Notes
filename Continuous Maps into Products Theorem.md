---
tag: topology
mathLink: continuous maps into products theorem
---
> [!thm]
> Let $f:A\rightarrow\prod X_\alpha$ be given by the [[Rule of Assignment]]
> $$f(a) = (f_\alpha(a))_{\alpha\in J}$$
> where $f_\alpha:A\rightarrow X_\alpha$ for each $\alpha$. Let $\prod X_\alpha$ have the [[Product Topology]]. Then, the [[Function]] $f$ is [[Continuous]] [[iff]] each function $f_\alpha$ is [[Continuous]].

>[!prop] Lemma
Let $\pi_{\alpha}:X \rightarrow X_\alpha$ where $X=\prod X_\alpha$ be given by the [[Rule of Assignment]]: $$\pi_{\alpha}(x)=x_{\alpha}$$ Then, $\pi_\alpha$ is [[Continuous]] for each $\alpha$.
>>[!proof]
Let $V$ be [[Open Set]] in $X_{\alpha'}$. Then $U=\pi_{\alpha'}^{-1}$ is [[Open Set]] in $X$ by the [[Comparison of the Box and Product Topologies Theorem]], as $U_{\alpha}=X_{\alpha}$ for all $\alpha$ but possible $\alpha'$. [[therefore]] $\pi_\alpha$ is [[Continuous]] for all $\alpha$.

>[!proof]
Suppose $f$ is [[Continuous]]. For each $\alpha$, $f_{\alpha}(a)=\pi_\alpha\circ f(a)$. As [[Composition]]s of [[Continuous]] [[Function]]s are [[Continuous]] ([[Constructing Continuous Functions Theorem]]), $f_{\alpha}$ is [[Continuous]] for all $\alpha$.
>
Suppose $f_{\alpha}$ is [[Continuous]] for all $\alpha$. Let $\mathcal{B}$ be the [[Basis]] for the [[Product Topology]] given by the [[Comparison of the Box and Product Topologies Theorem]]. Let $B\in \mathcal{B}$. Let $U_{\alpha}=f_{\alpha}^{-1}(B_{\alpha})$. Then, $U_{\alpha}$ is [[Open Set]] in $A$ as each $f_{\alpha}$ is [[Continuous]]. As $$f^{-1}(B)=\bigcup_{\alpha\in J}U_{\alpha}$$
if $U=f^{-1}(B)$, then $U$ is a [[Union]] of [[Open Set]] [[Set]]s, so $U$ is [[Open Set]]. [[therefore]] $f$ is [[Continuous]] by the [[Basis and Subbasis Formulation of Continuity]]. 
