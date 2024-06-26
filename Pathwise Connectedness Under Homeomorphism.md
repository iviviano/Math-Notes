---
tags:
  - topology
mathLink: pathwise connectedness under homeomorphism lemma
---
>[!prop] Lemma
Let $f:X \rightarrow Y$ be a [[Homomorphism]]. If $X$ is [[Pathwise Connectedness]] or $Y$ is [[Pathwise Connectedness]], then $X$ and $Y$ are [[Pathwise Connectedness]]. 

>[!proof]
Assume $X$ is [[Pathwise Connectedness]]. Let $p,q\in Y$. Let $p'=f^{-1}(p),q'=f^{-1}(q)$. Since $X$ is [[Pathwise Connectedness]], pick a [[Continuous]] $g:[0,1]\rightarrow X$ such that $g(0)=p'$ and $g(1)=q'$. Then, $f\circ g$ is a [[Function]] from $[0,1]$ to $y$ with $(f\circ g)(0)=p,(f\circ g)(1)=q$. So, $Y$ is [[Pathwise Connectedness]].

>[!thm] 
$\mathbb{R}^{n}$ is not [[Homeomorphic]] to $\mathbb{R}$ if $n>1$. 

>[!proof]
If $f:\mathbb{R}^{n}\rightarrow \mathbb{R}$ is a [[Homeomorphism]], then so is $f|\mathbb{R}^{n}-\{p\}:\mathbb{R}^{n}-\{p\}\rightarrow \mathbb{R}-\{f(p)\}$. But this [[Restriction]] contradicts the lemma. Since $\mathbb{R}^{n}-\{p\}$ is [[Pathwise Connectedness]] and $\mathbb{R}-\{f(p)\}$ is not.
