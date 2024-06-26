---
tag: topology
mathLink: equivalent
---
>[!def]
Let $X$ be a [[Set]] and let $d,\rho$ be [[Metric]]s on $X$. Then, $d$ and $\rho$ are said to be *equivalent* if they define the same [[Converges (Sequence)]]nt [[Sequence]]s. Equivalently, $d$ and $\rho$ are equivalent if the identity [[Function]]:
$$i:(X,d)\rightarrow(X,\rho)$$ is a [[Homeomorphism]].

>[!note]
>Two equivalent metrics do not necessarily have the same [[Cauchy Sequence]] sequences.

>[!prop]
For any [[Metric Space]] $(X,d)$,
$$\rho=\frac{d(x,y)}{1+d(x,y)}$$
defines an equivalent metric.

>[!proof]
Claim: $\rho$ is a [[Metric]].
>1. $\rho(x,y)=0\iff x=y$ follows from $d$ being a [[Metric]]
>2. $\rho(x,y)=\rho(y,x)$ follows from $d$ being a [[Metric]]
>3. Prove the [[Triangle Inequality]] holds:
Define: $f(t)=\frac{t}{1+t}$ on $(-1,\infty)$. Note: $f'(t)=(1+t)^{-2}>0$ and $f''(t)=-2(1+t)^{-3}<0$. Thus, if $s,t>0$ and $g(t)=f(s)+f(t)-f(s+t),$ then, $g'(t)=f'(t)-f'(s+t)>0$. So, $g(t)>0=0$. Then, $f(s+t)≤f(sf(t)$. Since $f$ is increasing, for all $x,y,z\in X$, $$\rho(x,y)=\frac{d(x,y)}{1+d(x,y)}≤\frac{d(x,z)+d(z,y)}{1+d(x,z)+d(z,y)}=f(d(x,z)+d(z,y)≤f(d(x,z))+f(d(z,y))=\rho(x,z)+\rho(x,y)$$so, $\rho$ is a [[Metric]].
>
If $d(x_{n},x)\rightarrow 0$, then $\rho(x_{n},x)=\frac{d(x_{n},x)}{1+d(x_{n},x)}\rightarrow 0$
>
If $\rho(x_{n},x)\rightarrow 0$, then ...
>
So, $i$ is a [[Homeomorphism]] by the [[Net-Sequential Characterization of Homeomorphism]].
