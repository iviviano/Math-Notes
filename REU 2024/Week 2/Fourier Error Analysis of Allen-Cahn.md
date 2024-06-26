Method described for heat equation here: [[https://en.wikipedia.org/wiki/Von_Neumann_stability_analysis]]

The 1D [[Allen-Cahn Equation]]: 
$$\frac{\partial v}{\partial t}=\gamma\frac{\partial^{2}v}{\partial x^{2}}+v-v^{3}$$
may be discretized with a finite difference scheme: 

We approximate $v$ with the sequence $v_{j}^{n}$: $$v(x,t)\approx v_{j}^{n}$$
where $x=jh$ for $0≤j≤J$ and $t=nk$ for $0≤n≤N$. 

Using a forward difference for $v_{t}$ and a central difference for $v_{xx}$, we have
$$\begin{align*}
v_{t}(jh,nk)&\approx \frac{v(jh,(n+1)k)-v(jh,nk)}{(n+1)k-nk}\approx \frac{v_{j}^{n+1}-v_{j}^{n}}{k}\\
v_{x}(jh,nk)&\approx \frac{v((j+1)h,nk)-v(jh,nk)}{(j+1)h-jh}\approx \frac{v_{j+1}^{n}-v_{j}^{n}}{h}\\
v_{xx}(jh,nk)&\approx \frac{v_{x}(jh,nk)-v_{x}((j-1)h,nk)}{jh-(j-1)h}\approx \frac{v_{j+1}^{n}-2v_{j}^{n}+v_{j}^{n-1}}{h^{2}}
\end{align*}$$
The discretized equation: $$\frac{v_{j}^{n+1}-v_{j}^{n}}{k}=\gamma \frac{v_{j+1}^{n}-2v_{j}^{n}+v_{j}^{n-1}}{h^{2}}+v_{j}^{n}-(v_{j}^{n})^{3}$$
We look at the linearization about $v=0$: $$\frac{v_{j}^{n+1}-v_{j}^{n}}{k}=\gamma \frac{v_{j+1}^{n}-2v_{j}^{n}+v_{j}^{n-1}}{h^{2}}+v_{j}^{n}$$
solving for $v_{j}^{n+1}$: 
$$v_{j}^{n+1}=v_{j}^{n}+r(v_{j+1}^{n}-2v_{j}^{n}+v_{j}^{n-1})+kv_{j}^{n}$$
where $r:= \gamma \frac{k}{h^{2}}$

The associated error equation: $$e_{j}^{n+1}=e_{j}^{n}+r(e_{j+1}^{n}-2e_{j}^{n}+e_{j}^{n-1})+ke_{j}^{n}$$
>[!question]
Why do we only need to consider the round-off error?


We write the error as a [[Fourier Polynomial]]: $$e(x,t)=\sum_{m=-M}^{M}E_{m}(t)e^{2\pi imx}$$
>[!question]
Why is a finite Fourier series sufficient?

is it just that we have $2M+1$ degrees of freedom, so we choose a trig poly with $2M+1$ terms


for each term of the error polynomial: $$e_{m}(x,t)=E_{m}e^{2\pi imx}$$
At $(x,t)=(jh,nk)$, $$\begin{align*}
e_{j}^{n}&= E_{m}(nk)e^{2\pi imjh}\\
e_{j}^{n+1}&= E_{m}(nk+k)e^{2\pi imjh}\\
e_{j+1}^{n}&= E_{m}(nk)e^{2\pi im(jh+h)}\\
e_{j-1}^{n}&= E_{m}(nk)e^{2\pi im(jh-h)}
\end{align*}$$
Plugging these expressions into the error difference equation: $$e_{j}^{n+1}=e_{j}^{n}+r(e_{j+1}^{n}-2e_{j}^{n}+e_{j}^{n-1})+ke_{j}^{n}$$
we have $$\begin{align*}
E_{m}(nk+k)e^{2\pi imjh}&= E_{m}(nk)e^{2\pi imjh}+r(E_{m}(nk)e^{2\pi im(jh+h)}-2E_{m}(nk)e^{2\pi imjh}\\&+E_{m}(nk)e^{2\pi im(jh-h)})+kE_{m}(nk)e^{2\pi imjh}\\
&= E_{m}(nk)e^{2\pi imjh}[1+r(e^{2\pi imh}-2+e^{-2\pi imh})+k]\\
&= E_{m}(nk)e^{2\pi imjh}[1+k-4r\sin^{2}(\pi mh)]\\
\end{align*}$$
So, the ratio of errors: $$\frac{E_{m}(nk+k)}{E_{m}(nk)}=1+k-4r\sin^{2}(\pi mh)$$
satisfies the stability condition if and only if $$|1+k-4r\sin^{2}(\pi mh)|\le1$$
since $4r\sin^{2}(\pi mh)\ge0$, $$4r\sin^{2}(\pi mh)\ge k$$and $$4r\sin^{2}(\pi mh)\le2+k$$
Using the bound $$\sin^{2}(\pi mh)\le1$$we have have $$4r\le 2+k$$
