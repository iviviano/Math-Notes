---
tag: algebra
mathLink: pullback
---
>[!def]
Let $X,Y$ be [[Vector Space]]s. If $u:X \mapsto Y$ is a [[Linear Transformation]], then its [[Dual]] is the map $u^{*}:Y^{*}\mapsto X^{*}$, defined by $f \mapsto f\circ u$. The resulting [[Function]] $u^{*}(f)$ is called the *pullback* of $f$ by $u$. 

Transpose: 

>[!def] Generalization to $p$-[[P-Tensor]]s:
>Suppose that $A:V \mapsto W$ is a [[Linear Transformation]]. The, the [[Pullback]] $A^{*}:W^{*}\mapsto V^{*}$ extends to the [[Exterior Algebra]]s, $A^{*}:\Lambda^{p}(W^{*})\mapsto \Lambda^{p}(V^{*})$ for all $p≥0$. If $T\in \Lambda^{p}(W^{*})$, define $A^{*}T\in \Lambda^{p}(V^{*})$ by $$A^{*}T(v_{1},\ldots,,v_{p})=T(Av_{1},\ldots,Av_{p})$$for all $v_{1},\ldots,v_{p}\in V$. Then, $A^*$ is a [[Homomorphism]].

>[!def] Application to $p$-[[P-Form]]s
If $f:X \rightarrow Y$ is a [[Smooth]] map and $\omega$ is a $p$-[[P-Form]] on $Y$, we define a $p$-form $f^{*}\omega$ on $X$ as follows. If $f(x)=y$ then $f$ induces a [[Derivative]] map $df_{x}:T_{x}(X)\rightarrow T_{y}(Y)$. Since $\omega(y)$ is an [[Alternating Tensor]] $p$-tensor on $T_{y}(Y)$, we can pull it back to $T_{x}(X)$ using the transpose $df_{x}^{*}$ as described above. Define $$f^{*}\omega(x)=(df_{x})^{*}\omega[f(x)]$$Then, $f^{*}\omega(x)$ is an [[Alternating Tensor]] $p$-tensor on $T_{x}(X)$, so $f^{*}$ is a $p$-form on $X$ called the *pullback* of $\omega$ by $f$.

>[!note]
>This works because $df_{x}$ is a [[Linear]] map between the [[Tangent Space]]s.