---
mathLink: uniqueness theorem of Fourier series
---
>[!thm]
>For all [[Continuous]] [[Function]]s, the [[Sequence]] of [[Fourier Coefficient]]s uniquely determines the [[Function]]. For all $f,g\in\mathcal{C}_{1}(\mathbb{R};\mathbb{C})$: $$\hat{f}=\hat{g}\implies f=g$$

>[!proof]

Claim: The [[Fejer Kernel]] $F_n$ is a $\mathcal{C}^{\infty}$-[[Periodic Approximate Identity]].
$$F_{n}=\sum_{|k|\le n}\left(1- \frac{\left|k\right|}{n}\right)e_{k}$$
Show [[PAI-1]]: $$\begin{align*}
\int_{0}^{1}F_{n}(t)\ dt&= \sum_{|k|\le n} \left(1- \frac{\left|k\right|}{n}\right)\int_{0}^{1}e^{2\pi ikt}\ dt\\
&= \sum_{|k|\le n}\left(1- \frac{|k|}{n}\right)\delta_{k,0}\\
&= 1\cdot 1\\
&= 1
\end{align*}$$
Show 

The Cesaro means: 
$$C_{n}[f]= \frac{1}{n}\sum_{k=0}^{n-1} S_{k}[f]$$
and $$F_{n}\star f=C_{n}[f]$$

$$\begin{align*}
S_{n}[f](t)&= \sum_{|k|\le n}\hat{f_{k}}e_{k}(t)\\
&= \sum \int_{0}^{1}f(s)\overline{e_{k}(t)}\ ds\cdot e_{k}(t)\\
&= \int_{0}^{1}\sum f(s)\overline{e_{k}(s)}\ ds\cdot e_{k}(t)\\
&= \int_{0}^{1}\sum e^{2\pi ik(t-s)} f(s)ds\\
&= D_{n}\star f
\end{align*}$$
where $D_{n}$ is the [[Dirichlet Kernel]]

So, $$\begin{align*}F_{n}\star f&=  \frac{1}{n}\sum_{k=0}^{n-1} D_{k}\star f\\
&= \left[\frac{1}{n}\sum_{k=0}^{n-1} D_{k}\right]\star f\end{align*}$$
So, $$F_{n}= \frac{1}{n}\sum_{k=0}^{n-1}D_{k}$$
Because $$
(g-h)\star f=0\implies g-h=0\implies g=h$$which is given by the following lemma

---

>[!prop] Lemma
>Given $g\in\mathcal{C}_1$, suppose $$g\star f=0,\forall f\in\mathcal{C}_1$$then, $g$ is identically 0

>[!proof]
Let $$\phi_{n}=\begin{cases}n- \frac{t}{n} & \text{if }t\in[0, \frac{1}{n}] \\
n+\frac{1}{n} & \text{if }t\in[\frac{-1}{n},0] \\
0 & \text{if }t\notin[\frac{-1}{n}, \frac{1}{n}]\end{cases}$$ Note that it is trivial to show that $\phi_{n}$ is a [[Periodic Approximate Identity]]. And, $\phi_{n}\in\mathcal{C}_{1}$ for all $n$, so $$g\star \phi_{n}=0$$for all $n$ and $$0=g\star \phi_{n}\rightarrow g$$uniformly. Therefore, $g\equiv 0$. 

---
$$\begin{align*}
D_{n}&= \sum_{k=-n}^{n}e^{2\pi ikt}\\
&= e^{-2\pi int}\sum_{k=0}^{2n}e^{2\pi ikt}\\
&= \frac{e^{-2\pi int}e^{2\pi int}\sin((2n+1)\pi t)}{\sin \pi t}\\
&= \frac{\sin((2n+1)\pi t)}{\sin \pi t}
\end{align*}$$
by [[set_1.pdf]] for $t\ne0$, and 
$$\lim_{t \rightarrow 0} \frac{\sin((2n+1)\pi t)}{\sin \pi t}=2n+1=D_{n}(0)$$by [[L'Hopital's Rule]].  

$$\begin{align*}
F_{n}&= \frac{1}{n}\sum_{k=}^{n-1}D_{k}\\
&=  \frac{1}{n}\sum_{k=0}^{n-1} \frac{\sin((2k+1)\pi t)}{\sin \pi t}\\
&= \frac{1}{n\sin \pi t}\Im \text{m}\left(\sum e^{\pi i(2k+1)t}\right)\\
&= \frac{1}{n\sin \pi t}\Im \text{m}\left(\sum e^{\pi it}\cdot e^{2\pi ikt}\right)\\
&= \frac{1}{n \sin \pi t}\Im \text{m}(e^{\pi it}\sum_{0}^{n-1} e^{2\pi ikt})\\
&= \frac{1}{n \sin \pi t}\Im \text{m}\left(e^{\pi it}\cdot \frac{e^{i \frac{n-1}{2}t}\sin( \frac{n}{2}t)}{(\sin (\frac{t}{2}))}\right)\quad \text{not quite right, subbed wrong}\\
&= \frac{1}{n \sin \pi t}\Im \text{m}\left(\frac{e^{i \pi(n-1)t}\sin( \frac{n}{2}t)}{(\sin (\frac{t}{2}))}\right)\\
&= \\
&= \frac{1}{n}\left[\frac{\sin(\pi nt)}{\sin(\pi t)}\right]^{2}\ge 0\text{ and even}
\end{align*}$$

[[PAI-2]] is redundant, since 

Show [[PAI-3]]: 
>[!note]
>for $0\le y\le \frac{\pi}{2}$, $$\frac{2y}{\pi}\le \sin y\le y$$

So, for $|t|>0$

$$\begin{align*}
|F_{n}(t)|&\le \frac{1}{n}\cdot \frac{1}{(2t)^{2}}\\
&= \frac{1}{4nt^{2}}
\end{align*}$$
Thus, $$\sup_{\delta\le t\le \frac{1}{2}} |F_{n}(t)|\le \frac{1}{4n \delta^{2}}\rightarrow 0$$as $n\rightarrow \infty$. Then, $$\int_{(\delta, \frac{1}{2}]} |F_{n}(t)|\ dt\le \frac{1}{4n \delta^{2}} \left(\frac{1}{2}-\delta\right)$$and thus $$\lim_{n\rightarrow \infty}\int_{\left[\frac{-1}{2}, \frac{1}{2}\right]-(-\delta,\delta)}\left|F_{n}(t)\right|\ dt=0$$
