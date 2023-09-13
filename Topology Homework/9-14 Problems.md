From 1.3: 1, 8, 9

>[!note] 1
>
>>[!prop] Lemma
Let $(X,d_X),(Y,d_Y)$ be [[Metric Space]]s. Let $f:X \rightarrow Y$ be [[Continuous]]. Let $x_{0}\in X,y_{0}\in Y$ with $y_0\ne f(x_{0})$. Define a new [[Function]]: $f':X \rightarrow Y$ with the [[Rule of Assignment]]: $$f'(x)=\left\{\begin{align}f(x)&\text{ for }x≠x_0\\y_{0}&\text{ for }x=x_{0}\end{align}\right.$$Then, $f'$ is not [[Continuity at a Point]] $x_{0}$.
>>>[!proof]
>>Pick $\epsilon>0$ such that $$B_{d_{Y}}(f(x_{0}),\epsilon)\cap B_{d_{Y}}(y_{0},\epsilon)=\emptyset$$ which may be done as [[Metric Spaces are Hausdorff]]. Pick $\delta>0$ such that $$\forall x\in X:d_{X}(x,x_{0})<\delta\implies d_{Y}(f(x_{0}),f(x))<\epsilon$$ Then, there is no $\delta_{0}>0$ such that $$\forall x\in X:d_{X}(x,x_{0})<\delta_0\implies d_{Y}(y_{0},f(x))<\epsilon$$ [[therefore]] $f'$ is not [[Continuous]] at $x_{0}$ by the [[Ep-de Formulation of Continuity]].
>
Now prove that $\sin^{-1}:[0,1]\rightarrow \mathbb{R}$ is [[Continuous]]. Let $\epsilon>0, x_{0}\in[0,1]$ be given. Let $\delta=\sin\left(\epsilon+\sin^{-1}(x_{0})\right)$. If $|x-x_{0}|<\delta$, $$|f(x)-f(x_{0})|=|\sin^{-1}(x)-\sin^{-1}(x_{0})|≤\sin^{-1}(x)-\sin^{-1}(x_{0})<\epsilon$$ [[therefore]] $\sin^{-1}:[0,1]\rightarrow \mathbb{R}$ is [[Continuous]] by the [[Ep-de Formulation of Continuity]]. By the lemma, $f$ is not [[Continuous]].

>[!note] 8
>>[!proof] General Proof
Let $\mathcal{B}$ be the [[Basis]] for the [[Product Topology]] on $X=X_{1}\times X_{2}$ given by the [[Comparison of the Box and Product Topologies Theorem]]. If $B\in \mathcal{B}$, $B=U_{1}\times U_{2}$ where $U_{1}$ is [[Open Set]] in $X_{1}$ and $U_{2}$ is [[Open Set]] in $X_{2}$. As $\pi_{1}^{-1}(B)=U_{1}$ which is [[Open Set]] in $X_{1}$, $\pi_{1}$ is [[Continuous]] by the [[Basis and Subbasis Formulation of Continuity]].
>
>
>>[!proof] Proof Using Metric
The [[Metric]] on $X=X_{1}\times X_{2}$ is $d((x_{1},x_{2}),(y_{1},y_{2}))=d_{1}(x_{1},y+1 )+d_{2}(x_{2},y_{2})$. Suppose $V$ is [[Open Set]] in $X$. Then, for each $x\in X$, pick $\epsilon_{x}>0$ such that $B_{d}(x,\epsilon_{x})\subseteq V$. Then, $$V=\bigcup_{x\in X}B_{d}(x,\epsilon_{x})$$By the [[Union Under Inverse Image]], $$\pi_{1}^{-1}(V)=\pi_{1}^{-1}\left(\bigcup_{x\in X}B_{d}(x,\epsilon_{x})\right)=\bigcup_{x\in X}\pi_{1}^{-1}(B_{d}(x,\epsilon_{x}))$$Now examine the [[Preimage]] of a [[Ball]] under the [[Projection]] map$$\pi_{1}^{-1}(B_{d}((x_{1},x_{2}),\epsilon_{(x_{1},x_2)}))=B_{d_{1}}(x_{1},\epsilon_{(x_{1},x_{2})})$$as for all $y\in X_{1}$, $d((x_{1},x_{2}), (y,x_{2}))=d_{1}(x_{1},y)$. So, $\pi^{-1}(V)$ is a [[Union]] of [[Open Set]] [[Ball]]s. [[therefore]] $\pi^{-1}$ is [[Continuous]].

>[!note] 9
By (8), $\pi_{1}$ and $\pi_{2}$ are [[Continuous]]. Let $f(x)=(f_{1}(x),f_{2}(x))$. Suppose $f$ is [[Continuous]]. Then, for each $k$, $\pi_{k}\circ f$ is [[Continuous]] as [[Composition]]s of [[Continuous]] [[Function]]s are [[Continuous]] ([[Constructing Continuous Functions Theorem]]).
>
Suppose that $\pi_{k}\circ f$ is [[Continuous]] for each $k$. Let $x_0\in X, \epsilon>0$ be given. Pick $\delta_{1}>0$ such that if $d(x,x_{0})<\delta, \rho_{1}(\pi_{1}\circ f(x),\pi_{1}\circ f(x_{0}))<\frac{\epsilon}{2}$. Pick $\delta_{2}>0$ such that if $d(x,x_{0})<\delta, \rho_{1}(\pi_{2}\circ f(x),\pi_{2}\circ f(x_{0}))<\frac{\epsilon}{2}$. Let $\delta=\min\{\delta_{1},\delta_{2}\}$. Then, if $d(x,x_{0})<\delta$, $$\rho(f(x),f(x_{0}))=\rho_{1}(\pi_{1}\circ f(x),\pi_{1}\circ f(x_{0}))+\rho_{2}(\pi_{2}\circ f(x),\pi_{2}\circ f(x_{0}))<\frac{\epsilon}{2} + \frac{\epsilon}{2}$$so the $f:X \rightarrow Z_{1}\times Z_{2}$ is [[Continuity at a Point]] $x_{0}$. As $x_{0}$ was arbitrary $f$ is [[Continuous]] on $X$.
>
>>[!note]
>This is just a special case of the [[Continuous Maps into Products Theorem]].
