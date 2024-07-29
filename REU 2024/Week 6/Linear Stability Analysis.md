>[!note]
Could compute $\alpha_{m}^{n}$ from numerical method to see if amplitudes are actually decreasing


Heat equation

Since $u_{j}^{n}$ approximates the 1-periodic function $u$, it may be interpreted as samples of a 1-periodic signal. This justifies writing $$u_{j}^{n}=\sum_{m\in[N]^{d}}\alpha_{m}^{n}~\e^{2\pi\i \frac{m\cdot j}{N}}$$where $$\alpha_{m}^{n}=\sum_{j\in[N]^{d}}u_{j}^{n}~\e^{-2\pi\i \frac{m\cdot j}{N}}$$is the discrete fourier transform (DFT) of the sequence $u_{j}^{n}$. For the $d$-dimensional DFT, the wavenumbers are vectors $m\in [N]^{d}$ where $$\begin{equation}
[N]=\{0,\ldots,N-1\}
\end{equation}$$
Using properties of the exponential function, we can understand how the discrete laplacian operator acts on Fourier space: 
$$\begin{align*}
		\Delta^{h}u_{j}^{n}&=\frac{1}{h^2}\sum_{i=1}^{d} \sum_{m\in[N]^{d}}\alpha_{m}^{n}~\left(\e^{2\pi \i \frac{m\cdot(j + e_{i})}{N}}-2\e^{2\pi\i\frac{m\cdot j}{N}}+\e^{2\pi\i\frac{m\cdot(j-e_{i})}{N}}\right)\\
		&=\sum_{m\in[N]^{d}}\sum_{i=1}^{d}\alpha_m^n\frac{1}{h^2}\left( \e^{2\pi\i\frac{m}{N}}+\e^{-2\pi\i\frac{m}{N}}-2 \right)~\e^{2\pi\i\frac{m\cdot j}{N}}\\
		&= \sum_{m\in[N]^{d}}\alpha_{m}^{n}~\e^{2\pi\i \frac{m\cdot j}{N}}\underbrace{\sum_{i=1}^{d}\e^{2\pi\i \frac{m}{N}}+\e^{-2\pi\i \frac{m}{N}}-2}_{:=\lambda_{m}} \\
		&=\sum_{m\in[N]^{d}}\lambda_m\alpha_m^n~\e^{2\pi\i\frac{m\cdot j}{N}}\\
\end{align*}$$
Thus, differentiation in the spatial domain corresponds to multiplication in the Fourier domain. For second-order differentiation, we have the amplification factor
$$\lambda_{m}= \frac{1}{h^{2}}\sum_{i=1}^{d}\left(2\cos\left(2\pi \frac{m_{i}}{N}\right)-2\right)=- \frac{4}{h^{2}}\sum_{i=1}^{d}\sin^{2}\left(\pi \frac{m_{i}}{N}\right)$$
The stability of the difference equation is based on the DFT representation of $u_{j}^{n}$. We say the algorithm is stable if 
$$\begin{equation} %\label{eq_stab_cond}
|\alpha_{m}^{n+1}|\le \alpha_{m}^{n}\quad \text{for all }m
\end{equation}$$

For the heat equation forward difference scheme (\ref{ds_HE_FD}), we have the following equation in Fourier space: 
$$\alpha_{m}^{n+1}=\alpha_{m}^{n}+k \lambda_{m}\alpha_{m}^{n}=(1+k \lambda_{m})\alpha_{m}^{n}$$
The stability condition (\ref{eq_stab_cond}) becomes $$|1+k \lambda_{m}|\le1\quad \text{for all }m$$
Since $\lambda_{m}\le 0$, this is equivalent to $$1+k \lambda_{m}\ge-1$$
We need the minimum value of $k \lambda_{m}$ greater than or equal to 2. Over all $N$ and all $m_{i}\in[N]$, the maximum of $\sin^{2} \left(\pi \frac{m}{N}\right)$ is 1. Therefore, a necessary and sufficient condition for stability is that $$k\le \min\left\{\frac{2}{\frac{4}{h^{2}}\sum_{i=1}^{d}\sin^{2}\left(\pi \frac{m_{i}}{N}\right)}:N\in \mathbb{N},m\in[N]^{d}\right\}= \frac{h^{2}}{2\sum_{i=1}^{d}1}$$
The maximum $k$ value for which the scheme is stable is written $$\begin{equation} %\label{eq_}
k_\text{crit}= \frac{h^{2}}{2d}
\end{equation}$$


For the implicit scheme (\ref{eq_HE_CN}), we have the following equivalent equation in Fourier space: 
$$\alpha_{m}^{n+1}=\alpha_{m}^{n}+ \frac{k}{2}(\lambda_{m}\alpha_{m}^{n+1}+\lambda_{m}\alpha_{m}^{n})$$
We can write:
$$(1- \frac{k}{2}\lambda_{m})\alpha_{m}^{n+1}=(1+ \frac{k}{2}\lambda_{m})\alpha_{m}^{n}\implies \frac{\alpha_{m}^{n+1}}{\alpha_{m}^{n}}= \frac{1+\frac{k}{2}\lambda_{m}}{1- \frac{k}{2}\lambda_{m}}$$
Since $\lambda_{m}<0$, this gives unconditional stability for $k>0$: $$-1\le \frac{\alpha_{m}^{n+1}}{\alpha_{m}^{n}}\le1\implies |\alpha_{m}^{n+1}|\le|\alpha_{m}^{n}|$$



Allen-Cahn Equation

$$\frac{\partial v}{\partial t }=\gamma\nabla ^{2}v-\phi(v)$$
The linearized equation about the unstable equilibrium $v=0$ is $$\begin{equation} %\label{eq_unstable_lin_AC}
\frac{\partial v}{\partial t}=\gamma\nabla ^{2}+v
\end{equation}$$
For periodic boundary condition, (\ref{eq_unstable_lin_AC}) has solution $$v(x,t)=\sum_{n\in\mathbb{Z}^{d}}\widehat{[v_{0}]}_{n}~\e^{(1-4\pi^{2}\gamma|n|^{2})t}~\e^{2\pi\i n\cdot x}$$
where the Fourier coefficients of the 1-periodic initial condition are given by 
$$\begin{equation} %\label{eq_FC}
\widehat{[v_{0}]}_{n}:=\int_{\Omega}v_{0}(x)~\e^{2\pi \i n\cdot x}~\ud x
\end{equation}$$
The Fourier mode $n$ will decay in time if $4\pi^{2}\gamma|n|^{2}>1$. This causes a low frequency instability. The constant mode will always be unstable. Whether additional modes are unstable depends on the value of $\gamma$. That a smaller value of $\gamma$ introduces higher frequency oscillations is consistent with its role in determining the width of phase boundaries (ELABORATE?). 



The linearized Allen-Cahn equation about the stable equilibrium $v=1$ is $$\begin{equation} %\label{eq_lin_AC}
\frac{\partial v}{\partial t}=\gamma\nabla ^{2}v+2-2v
\end{equation}$$
For periodic boundary conditions, (\ref{eq_lin_AC}) has solution $$v(x,t)=\sum_{n\in\mathbb{Z}^{d}}C_{n}~\e^{2\pi\i nx}$$
where the constants $C_{n}$: 
$$C_{n}:=\begin{cases}
(\widehat{[v_{0}]}_{0}-1)\e^{-2t}+1 & n=0\\
\widehat{[v_{0}]}_{n}~\e^{-[4\pi^{2}\gamma|n|^{2}+2]t} & n\ne0
\end{cases}$$
are related to the Fourier coefficients defined in (\ref{eq_FC})

For the linear solution, the amplitudes of all non-constant Fourier modes decay exponentially in time. The constant mode approaches the steady state solution 1. Similarly, the linearization about the other stable equilibrium exhibits exponential decay of non-constant Fourier modes. However, the constant coefficient tends to -1.



We can linearize the difference scheme (\ref{ds_AC_FD}) about the stable equilibrium $v=1$, giving $$\begin{equation} %\label{ds_lin_AC_FD}
\frac{v_{j}^{n+1}-v_{j}^{n}}{k}=\Delta^{h}v_{j}^{n}+2-2v_{j}^{n} \tag{lin-\ref{ds_AC_FD}}
\end{equation}$$
Write the solution $v_{j}^{n}$ as $$v_{j}^{n}=\sum_{m\in [N]^{d}}\alpha_{m}^{n}~\e^{2\pi\i \frac{m\cdot j}{N}}$$using the DFT. In conjugate space, (\ref{ds_lin_AC_FD}) becomes 
$$\begin{cases}
\alpha_{m}^{n+1}&= \left(1- 2k\right)\alpha_{m}^{n}+ 2k & m=0\\
\alpha_{m}^{n+1}&= \left(\underbrace{1- 2k+k \gamma \lambda_{m}}_{A_{m,k}}\right)\alpha_{m}^{n} & m\ne0
\end{cases}$$
To satisfy the stability condition (\ref{}), we need the amplitudes of every Fourier mode to decay in time. However, this is not actually possible when $m=0$ and $-1<\widehat{[v_{0}]}_{0}<1$. In this case, $\alpha_{m}^{n}\to 1$ as $n \to \infty$. This is a consequence of the Allen-Cahn equation failing to preserve mass in general (IS THIS TRUE?). Thus, we must use the modified stability condition: $$|\alpha_{m}^{n+1}|\le|\alpha_{m}^{n}|\quad \text{for all }m\ne0$$From (\ref{}), this becomes $|A_{m,k}|\le1$ for all $m\ne0$. Since $A_{m,k}\le1$, we need $$1- 2k-4 \frac{k \gamma}{h^{2}}\sum_{i=1}^{d}\sin^{2}\left(\pi \frac{m_{i}}{J}\right)\ge-1$$
Using the a-priori bound $|\sin(x)|\le1$, we have stability if $$\begin{equation} %\labek{eq_k_crit_AC}
k\le k_\text{crit}:=\frac{h^{2}}{h^{2}+2d\gamma}
\end{equation}$$
Again, the analysis for the linearization of (\ref{ds_AC_FD}) about $v=-1$ reveals the same stability condition on $k$. Since $v=\pm1$ are stable equilibria of the Allen-Cahn equation and solutions are bounded between them, we expect the stability of the linearized scheme at least reflect an upper bound on the critical $k$ of the nonlinear scheme. Numerical experiments support this conclusion. Figure \ref{fg_nonlinear_stability} shows a test which suggests the critical $k$ value for (\ref{ds_AC_FD}) is close to (\ref{eq_k_crit_AC}).

Figure: 
stability and instability of nonlinear scheme based on linear scheme estimate
use $$h=.005,k=.12\text{ vs }.11,N=10000,\gamma=.0001,seed=2$$
This also shows a case where implicit is stable but explicit is unstable





We can also perform this stability analysis on the linearization of the semi-implicit scheme (\ref{ds_AC_CN}): 
$$\begin{align}
\frac{v_{j}^{n+1}-v_{j}^{n}}{k}&=\gamma \Delta^{h}v_{j}^{n+1}+2-2v_{j}^{n}\tag{lin-\ref{ds_AC_CN}}\\
\end{align}$$
In Fourier space, we have $$
\begin{cases}
\alpha_{m}^{n+1}&=\alpha_{m}^{n}+2k-2k \alpha_{m}^{n} & m=0 \\
\alpha_{m}^{n+1}&= \alpha_{m}^{n}+k \gamma \lambda_{m}\alpha_{m}^{n+1}-2k\alpha_{m}^{n} & m\ne0
\end{cases}
$$
For $m\ne0$, we have $$(1-k \gamma \lambda_{m})\alpha_{m}^{n+1}=(1-2k)\alpha_{m}^{n}$$
So, amplitudes are decreasing in time if $$-1\le\frac{1-2k}{1-k \gamma \lambda_{m}}\le1$$Since $\lambda_{m}\le0$, this holds whenever $1-2k>-1$. Thus, the stability condition for the semi-implicit linearized scheme (\ref{ds_lin_AC_CN}) is $$k\le k_\text{crit}= 1$$
% DO WE EXPECT THIS TO REFLECT STABILITY OF NONLINEAR SCEME?

Figure:
maybe show that stability of nonlinear scheme is independent of $h$?




Cahn-Hilliard Equation
$$\frac{\partial c}{\partial t}=M\nabla ^{2}[\phi(c)-\gamma \nabla ^{2}c]$$
Linearizing the Cahn-Hilliard Equation about any constant equilibrium $c=c_{0}$, we have $$\begin{equation} %\label{eq_lin_CH}
\frac{\partial c}{\partial t}=M[\phi'(c_{0})\nabla ^{2}c-\gamma \nabla ^{2}(\nabla ^{2}c)]
\end{equation}$$
For periodic boundary conditions (\ref{eq_lin_CH}) has solution $$c(x,t)=\sum_{n\in\mathbb{Z}^{d}}\widehat{[c_{0}]}_{n}~\e^{-4 \pi^{2}M|n|^{2}[\phi'(c_{0})+4\pi^{2}\gamma|n|^{2}]t}~\e^{2\pi\i n\cdot x}$$
When $\phi'(c_{0})>=0$, every non-constant Fourier mode except $m=0$ decays in time, causing solutions to the linear equation to converge to their constant average. 
When $\phi'(c_{0})<0$, $c_{0}$ is in the unstable region. 
Just as with the linearization of the Allen-Cahn equation about its unstable constant equilibrium, there is a low frequency instability. 
Again, the number of modes which grow in time depends on the parameter $\gamma$. 
Here, the fastest growing mode may not be the constant mode, as shown in Figure \ref{fg_unstable_lin_CH}. 




The metastable region is 




Note that the mass-conservation of the Cahn-Hilliard difference schemes allows us to use the standard stability condition (\ref{eq_stab_cond}).
We can linearize the difference scheme (\ref{ds_CH_FD}) about a stable constant equilibrium $c=c_{0}$, $|c_{0}|\ge \frac{1}{\sqrt{3}}$, giving $$\begin{equation} %\label{ds_lin_CH_FD}
\frac{c_{j}^{n+1}-c_{j}^{n}}{k}=\phi'(c_{0})\Delta^{h}c_{j}^{n}-\gamma \Delta^{h}(\Delta^{h}c_{j}^{n})
\end{equation}$$
Using the standard DFT representation of $c_{j}^{n}$, this gives the equation $$\alpha_{m}^{n+1}=\alpha_{m}^{n}+k\phi'(c_{0})\lambda_{m}\alpha_{m}^{n}-k\gamma \lambda_{m}^{2}\alpha_{m}^{n}=(1+k \phi'(c_{0})\lambda_{m}-k \gamma\lambda_{m}^{2})\alpha_{m}^{n}$$
in conjugate space. Since we are considering a stable equilibrium $c_{0}$, $\phi'(c_{0})\ge0$. Therefore stability condition (\ref{eq_}) become $$|1+\underbrace{k \phi'(c_{0})\lambda_{m}-k \gamma \lambda_{m}^{2}}_{\le0}|\le1\iff1+k \phi'(c_{0}\lambda_{m}-k \gamma \lambda_{m}^{2})\ge-1$$
This holds generally if $$k\le k_\text{crit}= \frac{h^{4}}{8d\gamma+2d^{2}h^{2}\phi'(c_{0})}$$

For the extreme equilibria $c=1$ and $c=-1$, we have a minimal value of $k_\text{crit}$ at $$k'_\text{crit}= \frac{h^{4}}{8d\gamma+4d^{2}h^{2}}$$
Figure: comparing... use $$h=.02,\gamma=.001,k=.000016\text{ vs }.000017,c_{0}(x)=\sin(2\pi x)$$






Linearize the semi-implicit difference scheme (\ref{ds_CH_CN}) about a stable constant equilibrium $c=c_{0}$: $$\begin{equation} %\label{ds_lin_CH_CN}
\frac{c_{j}^{n+1}-c_{j}^{n}}{k}=\phi'(c_{0})\Delta^{h}u_{j}^{n}-\gamma \Delta^{h}(\Delta^{h}u_{j}^{n+1})
\end{equation}$$
In Fourier space, we have the equation $$\alpha_{m}^{n+1}=\alpha_{m}^{n}+k \phi'(c_{0})\lambda_{m}\alpha_{m}^{n}- k \gamma \lambda_{m}^{2}\alpha_{m}^{n}$$
giving $$\left| \frac{\alpha_{m}^{n+1}}{\alpha_{m}^{n}}\right|=\left| \frac{1+k \phi'(c_{0})\lambda_{m}}{1+k \gamma \lambda_{m}^{2}}\right|\le|1+k \phi'(c_{0})\lambda_{m}|$$
which is a good approximation for small $\gamma$. Since $c_{0}$ is a stable equilibrium, we have $\phi'(c_{0})\lambda_{m}\le0$, which gives the stability condition $$k\le - \frac{2}{\phi'(c_{0})\lambda_{m}}\le \frac{h^{2}}{2d\phi'(c_{0})}$$
At the extreme equilibria $c_{0}=\pm1$, we have $$k_\text{crit}= \frac{h^{2}}{4d}$$
It is not surprising that this semi-implicit scheme has stability $O(h^{2})$ while the other (semi)-implicit linear schemes (\ref{ds_HE_CN}) and (\ref{ds_lin_AC_CN) are $O(1)$ in $h$ since we handled the derivative of the approximation of the nonlinear term explicitly. This should align with the nonlinear difference scheme where explicit treatment of the nonlinear term is essential to avoid solving a nonlinear system at each step. 
