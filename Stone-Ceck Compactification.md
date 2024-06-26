---
tag: topology
mathLink: Stone-Ceck compactification
---
>[!thm]
If $X$ is a [[Completely Regular]] [[Topological Space]], then there is a [[Compactness]] space $\beta X$ and a [[Homeomorphism]] $\tau$ from $X$ to a [[Dense]] [[Subset]] of $\beta X$ such that for every [[Bounded Function into R]] [[Continuous]] [[Function]] $f:X \rightarrow \mathbb{R}$ there is a [[Function]] $f^{\beta}:\beta X \rightarrow \mathbb{R}$ with $f^{\beta}\circ \tau=f$. Moreover, $\beta X$ is unique in a the sense that if $Z$ is a [[Compactness]] space with a [[Homeomorphism]] $\sigma$ of $X$ onto a [[Dense]] [[Subset]] of $Z$ such that for each [[Bounded Function into R]] [[Continuous]] [[Function]] $f:X \rightarrow \mathbb{R}$ there is a [[Continuous]] $f^{Z}:Z \rightarrow \mathbb{R}$ with $f^{Z}\circ \sigma=f$, then $Z$ is [[Homeomorphic]] to $\beta X$. 

>[!proof] Proof. (*Existence*)
Let $\mathcal{F}$ denote all the [[Continuous]] [[Function]]s from $X$ into $[0,1]$, and for each $f\in \mathcal{F}$ let $X_{f}=[0,1]$, a copy of the [[Closed Set]] unit interval. Let $$\Omega=\prod\{X_{f}:f\in \mathcal{F}\}$$and define $$\tau:X \rightarrow \Omega, \tau(x)=\{f(x):f\in \mathcal{F}\}$$that is, the coordinate of $\tau(x)$ corresponding to each $f\in \mathcal{F}$ is given by $\tau(x)_{f}=f(x)$. Let $\beta X=\text{cl }\tau(X)$. $\beta X$ is [[Compactness]] by the [[Characterizations of Compactness]], since it is a [[Closed Set]] [[Subset]] of a [[Compactness]] space ($\Omega$ is [[Compactness]] by [[Tikhonov's Theorem]]).
>
Note that $\tau(X)$ is [[Dense]] in $\beta X$ by definition.
>
***Claim***: $\tau:X \rightarrow \tau(X)$ is a [[Homeomorphism]].
Clearly, $\tau$ is [[Continuous]], as the [[Coordinate Functions]]s of $\tau$ are each [[Continuous]] by $\tau$'s definition. So, the [[Maps into Products Theorem]] implies that $\tau$ is [[Continuous]].
>
Show that $\tau^{-1}$ is [[Continuous]]. Let $V$ be [[Open Set]] in $\tau(X)$. As each $f\in \mathcal{F}$ is [[Continuous]], $f^{-1}(V_{f})$ is [[Open Set]] in $X$. So, $$\tau^{-1}(V)=\bigcup_{f\in \mathcal{F}}f^{-1}(V_{f})$$is [[Open Set]] in $X$ as it is a [[Union]] of [[Open Set]] [[Set]]s. 
>
Show that $\tau$ is [[Injective]]. If $x,y\in X$ with $x\ne y$, then there is a [[Continuous]] [[Function]] $f:X \rightarrow [0,1]$ such that $f(x)=0$ and $f(y)=1$ ([[Urysohn's Lemma]]). So, $\tau(x)≠\tau(y)$ since $\tau_{f}(x)=0≠1=\tau_{f}(y)$.
>
$\tau$ is [[Surjective]] by definition, as its [[Range]] is its [[Image Set]].
>
***Claim***: If $f\in$ [[Vector Space of Continuous Bounded Functions]]$(X)$, then there is an $f^{\beta}\in C(\beta X)$ such that $f^{\beta}\circ\tau=f$.
>
Note: if $f\in \mathcal{F}$ and we define $f^\beta$ to be the [[Restriction]] of the [[Projection]] map $\pi_{f}$ to $\beta X$, then $f^\beta$ has the desired property. 
>
Now if $f\in C_{b}(X)$ and $a<f(x)<b$ for all $x\in X$, then $$g=(b-a)^{-1}(f-a)\in \mathcal{F}$$as $g$ is [[Bounded Function into R]] by $0,1$ and is [[Continuous]] by the [[Constructing Continuous Functions Theorem]]. [[therefore]] $g^{\beta}\in C(\beta X)$ with $g=g^{\beta}\circ \tau$. Let $f^{\beta}=(b-a)g^{\beta}+a$. As $$f^{\beta}\circ \tau=[(b-a)g^{\beta}+a]\circ \tau=(b-a)g^{\beta}\circ\tau+a=(b-a)g+a=(f-a)+a=f$$

>[!proof] (*Uniqueness*)

Let $Z,\sigma$ be as in the statement in the theorem and let $\Omega$ be the [[Product Space]] in the proof of existence. Define $\omega:Z \rightarrow \Omega$ by $$\omega(z)=\{f^{Z}(z):f\in \mathcal{F}\}$$Note: for each $x\in X,f\in \mathcal{F}$, $\omega(\sigma(x))_{f}=f(x)=\tau(x)_{f}$. 



Examples:
1. $\beta(0,1]≠[0,1]$, since there is no continuous extension of the [[Topologist's Sine Curve]]
2. $\beta \mathbb{N}$ is one of the major problems in modern point set [[Topology]]
	1. [[Cardinality]] $2^{c}$ where $c=\text{card}(\mathbb{R})$
	2. zero dimensional
	3. no nontrivial [[Converges (Sequence)]]nt [[Sequence]]s
	4. every infinite [[Closed Set]] [[Subset]] of $\beta \mathbb{N}$ contains a copy of $\beta \mathbb{N}$
3. 