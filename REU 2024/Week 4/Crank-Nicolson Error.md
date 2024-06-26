Consider the following initial value problem for the one-dimensional heat equation $$\begin{split} %\label{eq_heat_de}
\frac{\partial u}{\partial t}(x,t)&=D\frac{\partial ^{2}u}{\partial x^{2}}(x,t),\quad x\in[0,1]\\
u(x,0)&=u_{0}(x)\\
u(0,t)&=u(1,t)=0
\end{split}$$
The Crank-Nicolson method provides an implicit finite difference scheme for this problem. We discretize the spatial domain into $J$ uniform intervals of size $h= \frac{1}{J}$ and consider the first $N$ timesteps of size $k$. Denote the discrete sequence approximating $u$ as $\{u_{j}^{n}\}$ with $$\begin{align*}
u(jh,nt)&\approx u_{j}^{n},\quad j=0,\ldots,J,\quad n=0,\ldots,N
\end{align*}$$
The partial derivatives of (\ref{eq_heat_de}) are approximated as follows: $$\begin{align*}
\frac{\partial u}{\partial t}(jh,nt)&\approx \frac{u_{j}^{n+1}-u_{j}^{n}}{k}\\
\frac{\partial ^{2}u}{\partial x^{2}}(jh,nt)&\approx \frac{1}{2}\left(\frac{u^{n+1}_{j+1}-2u_{j}^{n+1}+u_{j-1}^{n+1}}{h^{2}}+ \frac{u_{j+1}^{n}-2u_{j}^{n}+u_{j-1}^{n}}{h^{2}}\right)
\end{align*}$$
We have the difference equation $$\begin{equation} %\label{eq_heat_CN}
\frac{u_{j}^{n+1}-u_{j}^{n}}{k}= \frac{1}{2}\left(\frac{u^{n+1}_{j+1}-2u_{j}^{n+1}+u_{j-1}^{n+1}}{h^{2}}+ \frac{u_{j+1}^{n}-2u_{j}^{n}+u_{j-1}^{n}}{h^{2}}\right)
\end{equation}$$
taking the diffusion constant $D=1$. 

If $v$ is a true solution to (\ref{eq_heat_de}), we can analyze the local truncation error, $\{\tau_{j}^{n}\}$, of the difference equation (\ref{eq_heat_CN}): 
$$\begin{equation} %\label{eq_heat_CN}
\underbrace{\frac{v_{j}^{n+1}-v_{j}^{n}}{k}}_{:=L}= \frac{1}{2}\left(\underbrace{\frac{v^{n+1}_{j+1}-2v_{j}^{n+1}+v_{j-1}^{n+1}}{h^{2}}}_{:=R_{1}}+ \underbrace{\frac{v_{j+1}^{n}-2v_{j}^{n}+v_{j-1}^{n}}{h^{2}}}_{:=R_{0}}\right)+\tau_{j}^{n}
\end{equation}$$
Fix $j,n$. Let $$v_{ixmt}= \frac{\partial^{i+m} v}{\partial ^{i}x \partial ^{m}t}(jh,nk)$$
We write: $$\begin{align*}
v_{j}^{n+1}&= v_{j}^{n}+kv_{t}+ \frac{k^{2}}{2}v_{tt}+ \frac{k^{3}}{6}v_{ttt}+ \frac{k^{4}}{24}v_{4t}+O(k^{5})\\
v_{j+1}^{n}&= v_{j}^{n}+hv_{x}+ \frac{h^{2}}{2}v_{xx}+ \frac{h^{3}}{6}v_{xxx}+ \frac{h^{4}}{24}v_{4x}+ \frac{h^{5}}{120}v_{5x}+O(h^{6})\\
v_{j-1}^{n}&= v_{j}^{n}-hv_{x}+ \frac{h^{2}}{2}v_{xx}- \frac{h^{3}}{6}v_{xxx}+ \frac{h^{4}}{24}v_{4x}- \frac{h^{5}}{120}v_{5x}+O(h^{6})\\
v_{j+1}^{n+1}&= v_{j}^{n}+kv_{t}+hv_{x}+ \frac{k^{2}}{2}v_{tt}+hkv_{tx}+ \frac{h^{2}}{2}v_{xx}+ \frac{k^{3}}{6}v_{ttt}+ \frac{k^{2}h}{2}v_{ttx}+ \frac{kh^{2}}{2}v_{txx}+ \frac{h^{3}}{6}v_{xxx}\\
&+ \frac{k^{4}}{24}k^{4}v_{4t}+ \frac{k^{3}h}{6}v_{tttx}+ \frac{k^{2}h^{2}}{4}v_{ttxx}+ \frac{kh^{3}}{6}v_{txxx}+ \frac{h^{4}}{24}v_{4x}+O(k^{5}+h^{5})\\
v_{j-1}^{n+1}&= v_{j}^{n}+kv_{t}-hv_{x}+ \frac{k^{2}}{2}v_{tt}-hkv_{tx}+ \frac{h^{2}}{2}v_{xx}+ \frac{k^{3}}{6}v_{ttt}- \frac{k^{2}h}{2}v_{ttx}+ \frac{kh^{2}}{2}v_{txx}- \frac{h^{3}}{6}v_{xxx}\\
&+ \frac{k^{4}}{24}k^{4}v_{4t}- \frac{k^{3}h}{6}v_{tttx}+ \frac{k^{2}h^{2}}{4}v_{ttxx}- \frac{kh^{3}}{6}v_{txxx}+ \frac{h^{4}}{24}v_{4x}+O(k^{5}+h^{5})\\
\end{align*}$$
Now, compute $$\begin{align*}
L&= \frac{1}{k}\left(v_{j}^{n}+kv_{t}+ \frac{k^{2}}{2}v_{tt}+ \frac{k^{3}}{6}v_{ttt}+ \frac{k^{4}}{24}v_{4t}+O(k^{5})-v_{j}^{n}\right)\\
&= v_{t}+ \frac{k}{2}v_{tt}+ \frac{k^{2}}{6}v_{ttt}+ \frac{k^{3}}{24}v_{4t}+O(k^{4})
\end{align*}$$
$$\begin{align*}
R_{0}&= \frac{1}{h^{2}}(v_{j}^{n}+hv_{x}+ \frac{h^{2}}{2}v_{xx}+ \frac{h^{3}}{6}v_{xxx}+ \frac{h^{4}}{24}v_{4x}+ \frac{h^{5}}{120}v_{5x}+O(h^{6})-2v_{j}^{n}\\&+v_{j}^{n}-hv_{x}+ \frac{h^{2}}{2}v_{xx}- \frac{h^{3}}{6}v_{xxx}+ \frac{h^{4}}{24}v_{4x}- \frac{h^{5}}{120}v_{5x}+O(h^{6}))\\
&= 2\left(\frac{1}{2}v_{xx}+ \frac{h^{2}}{24}v_{4x}+O(h^{4})\right)
\end{align*}$$
$$\begin{align*}
R_{1}&= \frac{1}{h^{2}}(
v_{j}^{n}+kv_{t}+hv_{x}+ \frac{k^{2}}{2}v_{tt}+hkv_{tx}+ \frac{h^{2}}{2}v_{xx}+ \frac{k^{3}}{6}v_{ttt}+ \frac{k^{2}h}{2}v_{ttx}+ \frac{kh^{2}}{2}v_{txx}+ \frac{h^{3}}{6}v_{xxx}\\
&+ \frac{k^{4}}{24}k^{4}v_{4t}+ \frac{k^{3}h}{6}v_{tttx}+ \frac{k^{2}h^{2}}{4}v_{ttxx}+ \frac{kh^{3}}{6}v_{txxx}+ \frac{h^{4}}{24}v_{4x}+O(k^{5}+h^{5})\\
&-2(v_{j}^{n}+kv_{t}+ \frac{k^{2}}{2}v_{tt}+ \frac{k^{3}}{6}v_{ttt}+ \frac{k^{4}}{24}v_{4t}+O(k^{5}))\\
&+v_{j}^{n}+kv_{t}-hv_{x}+ \frac{k^{2}}{2}v_{tt}-hkv_{tx}+ \frac{h^{2}}{2}v_{xx}+ \frac{k^{3}}{6}v_{ttt}- \frac{k^{2}h}{2}v_{ttx}+ \frac{kh^{2}}{2}v_{txx}- \frac{h^{3}}{6}v_{xxx}\\
&+ \frac{k^{4}}{24}k^{4}v_{4t}- \frac{k^{3}h}{6}v_{tttx}+ \frac{k^{2}h^{2}}{4}v_{ttxx}- \frac{kh^{3}}{6}v_{txxx}+ \frac{h^{4}}{24}v_{4x}+O(k^{5}+h^{5})\\
&= \frac{2}{h^{2}}\left(\frac{h^{2}}{2}v_{xx}+ \frac{kh^{2}}{2}v_{txx}+ \frac{k^{2}h^{2}}{4}v_{ttxx}+ \frac{h^{4}}{24}v_{4x}+O(k^{5}+h^{5})\right)\\
&= 2\left(\frac{1}{2}v_{xx}+ \frac{k}{2}v_{txx}+ \frac{k^{2}}{4}v_{ttxx}+ \frac{h^{2}}{24}v_{4x}+O(k^{5}+h^{3})\right)
\end{align*}$$

Note that $v$ a solution to (\ref{eq_heat_de}) implies $v_{xx}=v_{t}$. Additionally, $$v_{xxt}=v_{tt}\implies v_{tt}=v_{txx}=(v_{t})_{xx}=v_{xxxx}$$
So, $$\begin{align*}
R_{0}&= 2\left(\frac{1}{2}v_{t}+ \frac{h^{2}}{24}v_{tt}+O(h^{4})\right)\\
R_{1}&= 2\left(\frac{1}{2}v_{t}+ \frac{k}{2}v_{tt}+ \frac{k^{2}}{4}v_{ttt}+ \frac{h^{2}}{24}v_{tt}+O(k^{5}+h^{3})\right)
\end{align*}$$
And, $$\begin{align*}
\tau_{j}^{n}&= L- \frac{1}{2}(R_{0}+R_{1})\\
&= v_{t}+ \frac{k}{2}v_{tt}+ \frac{k^{2}}{6}v_{ttt}+ \frac{k^{3}}{24}v_{4t}+O(k^{4})-\left(\frac{1}{2}v_{t}+ \frac{h^{2}}{24}v_{tt}+O(h^{4})\right)\\
&- \left(\frac{1}{2}v_{t}+ \frac{k}{2}v_{tt}+ \frac{k^{2}}{4}v_{ttt}+ \frac{h^{2}}{24}v_{tt}+O(k^{5}+h^{3})\right)\\
&= \frac{k^{2}}{6}v_{ttt}-\frac{h^{2}}{12}v_{tt}+O(h^{3}+k^{3})
\end{align*}$$
