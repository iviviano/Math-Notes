---
tag: differential topology
mathLink: derivative
---
>[!def]
Let $f$ be a [[Smooth]] [[Function]] mapping an [[Open Set]] [[Subset]] of $\mathbb{R}^n$ to $\mathbb{R}^m$. Let $x$ be a point in the [[Domain]] of $f$. Then for a [[Vector]] $h\in \mathbb{R}^n$, the derivative of $f$ in the direction $h$ is given by the [[Limit of a Function]] of the [[Difference Quotient]]:
$$df_{x}(h)=\lim_{t \rightarrow 0}\frac{f(x+th)-f(x)}{t}$$
With $x$ fixed, we define a mapping $df_{x}:\mathbb{R}^{n}\rightarrow \mathbb{R}^{m}$ by assigning to each [[Vector]] $h\in \mathbb{R}^n$ the directional derivative: $df_{x}(h)\in \mathbb{R}^m$. This map is called the *derivative* of $f$.

>[!def] Definition for Mappings Between Arbitrary Manifolds
Let $X,Y$ be [[Manifold]], let $f:X \rightarrow Y$ be a [[Smooth]] [[Function]], and let $x\in X, y=f(x)$. Suppose $\phi:U \rightarrow X$ is a [[Parameterization]] of $X$ about $x$ and $\psi:V \rightarrow Y$ is a [[Parameterization]] of $Y$ about $y$ where $U\subseteq \mathbb{R}^{n},V\subseteq \mathbb{R}^{m}$ are [[Open Set]], and $\phi(0)=x,\psi(0)=y$. Then the *derivative* of $f$:
$$df_{x}=d \psi_{0}\circ dh_{0}\circ d \phi_{0}^{-1}$$
This definition creates a [[Linear Transformation]] $f:T_{x}(X)\rightarrow T_{y}(Y)$.
