>[!def]

For any non-negative integer $p$, we define $$W^{m,p}:=\{u\in L^{p}(\Omega):\partial ^{\alpha}u\in L^{p}(\Omega)\text{ for all }|\alpha|\le m\}$$
Additionally, define $$W_{0}^{m,p}=\text{cl }(\mathcal{C}^{\infty}_{c})$$
The [[Norm]] on $W^{m,p}$ is defined by $$\|u\|_{W^{m,p}}:=\left\{\sum_{0\le|\alpha|\le m}\|\partial ^{\alpha}u\|^{p}_{L^{p}(\Omega)}\right\}^{\frac{1}{p}}$$
Note that all derivatives are taken as [[Derivative of a Distribution]].

For the case $p=2$, $W^{m,p}$ and $W_{0}^{m,p}$ are [[Hilbert Space]]s. We denote $$\begin{align*}H^{m}&:=W^{m,2}\\
H^{m}_{0}&:=W_{0}^{m,2}
\end{align*}$$
The [[Inner Product]] on $H^{m}$ is $$(u,v)_{H^{m}}:=\sum_{0\le|\alpha|\le m}\langle \partial ^{\alpha}u,\partial ^{\alpha}v\rangle_{L^{2}}$$
This inner product induces the standard Sobolev norm. 