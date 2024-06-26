>[!1]

Fix $0<\delta< \frac{1}{2}$ and let $f\in\mathcal{C}_{1}(\mathbb{R};\mathbb{C})$ be $\alpha$-Hölder continuous. Pick $C>0$ such that for all $x,y\in \mathbb{R}$, $$|f(x)-f(y)|\le C|x-y|^{\alpha}$$
For any $t\in \mathbb{R}$,
$$\begin{align*}
|(F_{n}\star f)(t)-f(t)|=& \left|\int_{- \frac{1}{2}}^{\frac{1}{2}} F_{n}(s)f(t-s)\ ds-f(t)\underbrace{\int_{- \frac{1}{2}}^{\frac{1}{2}}F_{n}(s)\ ds}_{=1 \text{, }F_{n} \text{ is a PAI}} \right|\\
=& \left|\int_{- \frac{1}{2}}^{\frac{1}{2}} F_{n}(s)[f(t-s)-f(t)]\ ds\right|\\
\le& \left|\int_{(-\delta,\delta)}F_{n}(s)[f(t-s)-f(t)]\ ds\right|\\
&\quad\quad\quad+\left|\int_{[- \frac{1}{2}, \frac{1}{2}]-(-\delta,\delta)}F_{n}(s)[f(t-s)-f(t)\ ds\right|\\
:=& I_{1}+I_{2} 
\end{align*}$$
We use the $\alpha$-Hölder condition to estimate $I_{1}$. For all $s\in(- \delta, \delta)$, $|t-s-t|=|s|<\delta$, so $|s|^{\alpha}<\delta^\alpha$ by the monotonicity of $\log$:
$$\begin{align*}
|s|&< \delta\\
\iff\log|s|&< \log \delta\\
\iff \alpha\log|s|&< \alpha\log \delta\\
\iff\log|s|^{\alpha}&< \log \delta^{\alpha}\\
\iff |s|^{\alpha}&< \delta^{\alpha}
\end{align*}$$
Therefore, $$\begin{align*}
I_{1}&\le \int_{- \delta}^{\delta}\left|F_{n}(s)\right|\cdot \underbrace{\left|f(t-s)-f(s)\right|}_{\le C\cdot \delta^\alpha}\ ds\\
&\le C\cdot \delta^{\alpha}\int_{-\delta}^{\delta}|F_{n}(s)|\ ds\\
&\le C\delta^{\alpha}\int_{- \frac{1}{2}}^{\frac{1}{2}}\underbrace{|F_{n}(s)|}_{=F_{n}(s)}\ ds\\
&= C\delta^{\alpha}
\end{align*}$$
For NUMBER, we use that $F_{n}$ is positive and real. For NUMBER, we use that $F_{n}$ is a periodic approximate identity (PAI-1).
For $I_{2}$, $$\begin{align*}
I_{2}&\le \int_{[-\frac{1}{2},\frac{1}{2}]-(-\delta,\delta)}|F_{n}(s)|\cdot|[f(t-s)-f(t)]|\ ds\\
&\le \int_{[-\frac{1}{2},\frac{1}{2}]-(-\delta,\delta)}|F_{n}(s)|\cdot(|f(t-s)|+|f(t)|)\ ds\quad(\triangle \text{ inequality})\\
&\le 2\|f\|_{\infty}\int_{[-\frac{1}{2},\frac{1}{2}]-(-\delta,\delta)}|F_{n}(s)|\ ds\\
&= 2\|f\|_{\infty}\int_{[-\frac{1}{2},\frac{1}{2}]-(-\delta,\delta)} \frac{1}{n} \left(\underbrace{\sin(\pi n s)}_{\le1}\right)^{2}\left(\frac{1}{\underbrace{\sin(\pi s)}_{\ge 2s}}\right)^{2}\ ds\\
&\le 2\|f\|_{\infty}\int_{[- \frac{1}{2}, \frac{1}{2}]-(-\delta,\delta)} \underbrace{\frac{1}{4ns^{2}}}_\text{even}\ ds\\
&\le \frac{\|f\|_{\infty}}{n}\int_{(\delta,\frac{1}{2}]} \frac{1}{s^{2}}\ ds\\
&\le \frac{\|f\|_{\infty}}{n\delta^{2}}\cdot\left(\frac{1}{2}-\delta\right)\quad(\text{ML estimate})\\
&< \frac{\|f\|_{\infty}}{2n\delta^{2}}
\end{align*}$$Since this bound on $I_{1}+I_{2}$ has no dependence on $t$, we have shown the intended bound: $$\|F_{n}\star f-f\|_{\infty}\le C\delta^{\alpha}+ \frac{\|f\|_{\infty}}{2n\delta^{2}}$$


(b) 

For all $n\in \mathbb{N}$, we have the bound $$\|F_{n}\star f-f\|_{\infty}\le C_{f}\cdot n^{-\gamma}$$for constants $C_{f}>0$ and $\gamma(\alpha)>0$ whose optimal values are given by $$\begin{align*}
C_{f}:&= C+2\|f\|_{\infty}\\
\gamma:&= \frac{\alpha}{2+\alpha}
\end{align*}$$

Let $\delta= \frac{1}{2}n^{- \frac{1}{2+\alpha}}$. Then, $$\begin{align*}
\|F_{n}\star f-f\|_{\infty}&\le C\delta^{\alpha}+ \frac{\|f\|_{\infty}}{2n\delta^{2}}\\
&= \frac{C}{\underbrace{2^{\alpha}}_{\ge1}n^{ \frac{\alpha}{2+\alpha}}}+ \frac{\|f\|_{\infty}}{2n\left(\frac{1}{2} n^{- \frac{1}{2+\alpha}}\right)^{2}}\\
&\le \frac{C}{n^{\frac{\alpha}{2+\alpha}}}+ \frac{2\|f\|_{\infty}}{n^{1-\frac{2}{2+\alpha}}}\\
&\le \frac{C}{n^{\frac{\alpha}{2+\alpha}}}+ \frac{2\|f\|_{\infty}}{n^{\frac{\alpha}{2+\alpha}}}\\
&= \frac{C+2\|f\|_{\infty}}{n^{\frac{\alpha}{2+\alpha}}}\\
:&= \frac{C_{f}}{n^{\gamma}}
\end{align*}$$


>[!Problem 2]

(a)

Let $f\in\mathcal{C}_{1}^{1}(\mathbb{R};\mathbb{C})$ satisfy $$\hat f_{0}=\int_{0}^{1}f(t)\ dt=0$$
Note that the Fourier differentiation mantra states: $$\hat f_{n}= \frac{\hat f'_{n}}{2\pi in},\text{ for all }|n|\in \mathbb{N}$$Using Plancherel's Identity for $f$ and $f'$, we see $$\begin{align*}
\int_{0}^{1}|f(t)|^{2}\ dt&= \|f\|_{2}^{2}\\
&= \sum_{n=-\infty}^{\infty}\left|\hat f_{n}\right|^{2}\\
&= \sum_{n=1}^{\infty}\left|\hat f_{-n}\right|^{2}+\hat f_{0}+\sum_{n=1}^{\infty}\left|\hat f_{n}\right|\\
&= \sum_{n=1}^{\infty}\left|\frac{\hat f'_{-n}}{2\pi i}\right|^{2}+0+\sum_{n=1}^{\infty}\left|\frac{\hat f'_{n}}{2\pi i}^{2}\right|\\
&\le \frac{1}{4\pi^{2}}\sum_{n=1}^{\infty}\left|\hat f'_{-n}\right|^{2}+ \frac{1}{4\pi^{2}}\left|\hat f'_{0}\right|^{2}+ \frac{1}{4\pi^{2}}\sum_{n=1}^{\infty}\left|\hat f'_{n}\right|^{2}\\
&= \frac{1}{4\pi^{2}}\sum_{n=-\infty}^{\infty}\left|\hat f'_{n}\right|^{2}\\
&= \frac{1}{4\pi^{2}}\|f'\|_{2}^{2}\\
&= \frac{1}{4\pi^{2}}\int_{0}^{1}|f'(t)|\ dt
\end{align*}$$
but this is missing the factor on $n$...

$$\begin{align*}
\int_{0}^{1}|f(t)|^{2}\ dt&= \|f\|_{2}^{2}\\
&= \sum_{n=-\infty}^{\infty}\left|\hat f_{n}\right|^{2}\\
&= \sum_{n=1}^{\infty}\left|\hat f_{-n}\right|^{2}+\hat f_{0}+\sum_{n=1}^{\infty}\left|\hat f_{n}\right|\\
&= \sum_{n=1}^{\infty}\left|\frac{\hat f'_{-n}}{2\pi in}\right|^{2}+0+\sum_{n=1}^{\infty}\left|\frac{\hat f'_{n}}{2\pi in}^{2}\right|\\
&\le \frac{1}{4\pi^{2}}\sum_{n=1}^{\infty}\frac{\left|\hat f'_{-n}\right|^{2}}{n}+ \frac{1}{4\pi^{2}}\left|\hat f'_{0}\right|^{2}+ \frac{1}{4\pi^{2}}\sum_{n=1}^{\infty}\frac{\left|\hat f'_{n}\right|^{2}}{n}\\
&\le \frac{1}{4\pi^{2}}\sum_{n=1}^{\infty}\left|\hat f'_{-n}\right|^{2}+ \frac{1}{4\pi^{2}}\left|\hat f'_{0}\right|^{2}+ \frac{1}{4\pi^{2}}\sum_{n=1}^{\infty}\left|\hat f'_{n}\right|^{2}\quad(\text{comparison test})\\
&= \frac{1}{4\pi^{2}}\sum_{n=-\infty}^{\infty}\left|\hat f'_{n}\right|^{2}\\
&= \frac{1}{4\pi^{2}}\|f'\|_{2}^{2}\\
&= \frac{1}{4\pi^{2}}\int_{0}^{1}|f'(t)|\ dt
\end{align*}$$


(b)

$$\begin{align*}
|\alpha \beta|&= |\alpha|\cdot|\beta|\\
&= \sqrt{|\alpha|^{2}\cdot|\beta|^{2}}\\
\end{align*}$$So, the claim of Prop NUMBER reduces to showing that in general, the geometric mean of two non-negative real numbers is bound by their arithmetic mean:
$$\begin{equation}\sqrt{ab}\le \frac{a+b}{2}\end{equation}$$
$$\begin{align*}
0&\le  \left(\frac{a}{2}- \frac{b}{2}\right)^{2}=\frac{a^{2}}{4} - \frac{ab}{2}+ \frac{b^{2}}{4}\\
\iff ab&\le \frac{a^{2}}{4}+ \frac{ab}{2}+ \frac{b^{2}}{4}=\left(\frac{1}{2}(a+b)\right)^{2}
\end{align*}$$showing Eq NUMBER for all non-negative real numbers. 


(c)
$$\begin{align}
A(\gamma)&= \frac{1}{2}\int_{0}^{1}x(t)y'(t)-x'(t)y(t)\ dt\\
&\le \frac{1}{2}\int_{0}^{1}|x(t)y'(t)|+|x'(t)y(t)|\ dt\\
&\le \frac{1}{2}\int_{0}^{1} \frac{1}{2}(|x(t)|^{2}+|y'(t)|^{2})+ \frac{1}{2}(|x'(t)|^{2}+|y(t)|^{2})\ dt\\
&= \frac{1}{4}\int_{0}^{1}|x(t)|^{2}\ dt+ \frac{1}{4}\int_{0}^{1}|y'(t)|^{2}+|x'(t)|^{2}\ dt+ \frac{1}{4}\int_{0}^{1}|y(t)|^{2}\ dt\\
&\le \frac{1}{16\pi^{2}}\int_{0}^{1}|x'(t)|^{2}\ dt+ \frac{1}{4}\int_{0}^{1}|y'(t)|^{2}+|x'(t)|^{2}\ dt+ \frac{1}{16\pi^{2}}\int_{0}^{1}|y'(t)|^{2}\ dt\\
&= \frac{1}{16\pi^{2}}\int_{0}^{1}|x'(t)|^{2}+|y'(t)|^{2}\ dt+ \frac{\pi^{2}}{4\pi^{2}}\int_{0}^{1}|y'(t)|^{2}+|x'(t)|^{2}\ dt\\
&= \left(\frac{1+4\pi^{2}}{16\pi^{2}}\right)\int_{0}^{1}|x'(t)|^{2}+|y'(t)|^{2}\ dt
\end{align}$$


$$\begin{align}
A(\gamma)&= \frac{1}{2}\int_{0}^{1}x(t)y'(t)-x'(t)y(t)\ dt\\
&\le \frac{1}{2}\int_{0}^{1}|x(t)y'(t)|+|x'(t)y(t)|\ dt\\
&= \frac{1}{2}\int_{0}^{1}|\sqrt{2\pi} x(t)\cdot \frac{1}{\sqrt{2\pi}}y'(t)|+|\sqrt{2\pi} x'(t)\cdot \frac{1}{\sqrt{2\pi}}y(t)|\ dt\\
&\le \frac{1}{2}\int_{0}^{1} \frac{1}{2}\left(|\sqrt{2\pi} x(t)|^{2}+ \left| \frac{1}{\sqrt{2\pi}}y'(t)\right|^{2}\right)+ \frac{1}{2}\left(|\sqrt{2\pi} y(t)|+ \left| \frac{1}{\sqrt{2\pi}} x'(t)\right|\right)\ dt\\
&= \frac{1}{4}\cdot 2\pi\int_{0}^{1}|x(t)|^{2}\ dt+ \frac{1}{4}\cdot \frac{1}{2\pi}\int_{0}^{1}|y'(t)|^{2}+|x'(t)|^{2}\ dt+ \frac{1}{4}\cdot 2\pi\int_{0}^{1}|y(t)|^{2}\ dt\\
&\le \frac{\pi}{2}\cdot \frac{1}{4\pi^{2}}\int_{0}^{1}|x'(t)|^{2}\ dt+ \frac{1}{4}\cdot \frac{1}{2\pi}\int_{0}^{1}|x'(t)|^{2}+|y'(t)|^{2}\ dt+ \frac{\pi}{2}\cdot \frac{1}{4\pi^{2}}\int_{0}^{1}|y'(t)|^{2}\ dt\\
&= \frac{1}{4\pi}\int_{0}^{1}|x'(t)|^{2}+|y'(t)|^{2}\ dt\\
&= \frac{1}{4\pi}
\end{align}$$




>[!Problem 3]

(a) Let $0<T'<T$ be another period of $f$ and let $n\in\mathbb{Z}$ such that $n\frac{T'}{T}\notin\mathbb{Z}$. Note that $e^{2\pi ik}=1$ precisely when $k\in\mathbb{Z}$. So, $e^{2\pi in \frac{T'}{T}}\ne1$. We have $$\begin{align*}
\hat f_{n}&= \frac{1}{T}\int_{0}^{T}f(t)\ e^{-2\pi in \frac{t}{T}}\ dt\\
&= \frac{1}{T}\int_{T'}^{T+T'}f(s-T')\ e^{-2\pi in \frac{s-T'}{T}}\ ds\quad(\text{change variables }t=s-T')\\
&= e^{2\pi in \frac{T'}{T}} \frac{1}{T}\int_{0}^{T}f(s)\ e^{-2\pi in \frac{s}{T}}\ ds\\
&= e^{2\pi in \frac{T'}{T}}\hat f_{n}
\end{align*}$$Thus, we have $$\hat f_{n}(e^{2\pi in \frac{T'}{T}}-1)=0$$Since $e^{2\pi in \frac{T'}{T}}\ne1$, $\hat f_{n}=0$. 


(b) Let $f\in\mathcal{C}_{T}(\mathbb{R};\mathbb{C})$. Suppose $$\hat f_{n}=0\text{, for all }n\in\mathbb{Z}\text{, for which }n \frac{T'}{T}\notin\mathbb{Z}$$for some $T'>0$. 


Let $g:\mathbb{R}\rightarrow \mathbb{C}$ be defined by $$g(t)=f(t+T'),\text{ for all }t\in \mathbb{R}$$Note that $g\in\mathcal{C}_{T}(\mathbb{R};\mathbb{C})$. Compute $$\begin{align*}
\hat g_{n}&= \frac{1}{T}\int_{0}^{T}g(t)\ e^{-2\pi in \frac{t}{T}}\ dt\\
&= \frac{1}{T}\int_{0}^{T}f(t+T')\ e^{-2\pi in \frac{t}{T}}\ dt\\
&= \frac{1}{T}\int_{T'}^{T+T'}f(s)\ e^{-2\pi in \frac{s-T'}{T}}\ ds\quad(\text{change variables }s=t+T')\\
&= e^{2\pi in \frac{T'}{T}} \frac{1}{T}\int_{0}^{T}f(s)\ d^{-2\pi in \frac{s}{T}}\ ds\\
&= e^{2\pi in \frac{T'}{T}}\hat f_{n}
\end{align*}$$
Consider two cases for $n$. If $n \frac{T'}{T}\in\mathbb{Z}$, then $e^{2\pi in \frac{T'}{T}}=1$, so $$\hat g_{n}=\hat f_{n}$$Otherwise, $$g_{n}=e^{2\pi in \frac{T'}{T}}\hat f_{n}=e^{2\pi in \frac{T'}{T}}\cdot0=0=\hat f_{n}$$Since $$\hat f_{n}=\hat g_{n}$$and $f,g\in\mathcal{C}_{T}(\mathbb{R};\mathbb{C})$, the uniqueness property gives $f=g$. In particular, $$f(t)=g(t)=f(t+T'),\text{ for all }t\in \mathbb{R}$$showing that $f$ is $T'$-periodic.



>[!Problem 4]

(a)

Fix an irrational $\alpha\in \mathbb{R}$ and let $f\in\mathcal{C}_{1}(\mathbb{R};\mathbb{C})$ be $\alpha$-rotationally invariant. 

Let $g:\mathbb{R} \rightarrow \mathbb{C}$ be defined by $g(t):=f(t+\alpha)$. By NUMBER, we have $$\hat f_{n}=\hat g_{n},\text{, for all }n\in\mathbb{Z}$$
We have $$\begin{align*}
\hat f_{n}&= \hat g_{n}\\
&= \int_{0}^{1}f(t+\alpha)e^{-2\pi int}\ dt\\
&= \int_{\alpha}^{1+\alpha}f(s)e^{-2\pi in(s-\alpha)}\ ds\quad(\text{change variables }s=t+\alpha)\\
&= e^{2\pi in \alpha}\int_{0}^{1}f(s)e^{-2\pi ins}\ ds\\
&= e^{2\pi in \alpha}\hat f_{n}
\end{align*}$$
So, $$\begin{equation}\hat f_{n}(e^{2\pi in \alpha}-1)=0,\text{ for all }n\in\mathbb{Z}\end{equation}$$The irrationality of $\alpha$ implies that $n \alpha\notin \mathbb{Z}$ if $n\ne 0$. Note that $e^{2\pi ik}=1$ precisely when $k\in\mathbb{Z}$. Therefore, $e^{2\pi in \alpha}\ne0$ for all $n\ne0$. Then, NUMBER implies that $\hat f_{n}=0$ for all $n\in \mathbb{Z}$ with $n\ne0$. We now use the uniqueness property to show $f$ is constant. Let $h:\mathbb{R} \rightarrow \mathbb{C}$ be defined by $h(t)=c\in \mathbb{C}$ for all $t\in \mathbb{R}$. Compute $$\begin{align*}
\hat h_{0}&= \int_{0}^{1} c\ dt=c\\
\hat h_{n}&= \int_{0}^{1}ce^{-2\pi int}\ dt=c \delta_{-n,0}=0,\text{ for all }n\ne0
\end{align*}$$ By choosing $c=\hat f_{0}$, we see that $$\hat f_{n}=\hat h_{n}, \text{ for all }n\in\mathbb{Z}$$Since $f,h\in\mathcal{C}_{1}(\mathbb{R};\mathbb{C})$, $f=h$ is constant.


(b) 

Let $\alpha= \frac{p}{q}$ for $p,q\in \mathbb{N}$ and $p,q\ne0$. Define $f$ to be the 1-periodic extension of $$f(t)=\begin{cases} t- \frac{n}{q} & t\in[ \frac{n}{q}, \frac{n}{q}+ \frac{1}{2q})\text{, for some }n\in\mathbb{Z} \\ 
\frac{n+1}{q}-t & t\in[\frac{n}{q}+ \frac{1}{2q},\frac{n+1}{q}),\text{ for some }n\in\mathbb{Z}\end{cases}$$
For each $t\in[0,1]$, if $t\in[ \frac{n}{q}, \frac{n}{q}+ \frac{1}{2q})$, $$t+\alpha=t+ \frac{p}{q}\in \left[ \frac{n+p}{q}, \frac{n+p}{q}+ \frac{1}{2q}\right)$$so, $$\begin{align*}f(t+\alpha)&= t+ \frac{p}{q}- \frac{n+p}{q}\\
&= t- \frac{n}{q}\\
&= f(t)\end{align*}$$ If $t\in[ \frac{n}{q}+ \frac{1}{2q}, \frac{n+1}{q})$, $$t+\alpha=t+ \frac{p}{q}\in\left[ \frac{n+p}{q}+ \frac{1}{2q}, \frac{n+p+1}{q}\right)$$so, $$\begin{align*}
f(t+\alpha)&= \frac{1}{2q}-t+ \frac{p}{q}- \frac{n+p}{q}\\
&= \frac{1}{2q}-t- \frac{n}{q}\\
&= f(t)
\end{align*}$$This shows that $f$ is $\alpha$-rotationally invariant. 

$f$ is continuous: at $t= \frac{n}{q}$: 
The left limit of $f$ at $t$: $$f(t-)= t- \frac{n}{q}=0$$The right limit and value of $f$ at $t$: 
$$f(t+)= \frac{n-1+1}{q}- t= \frac{n}{q}- \frac{n}{q}=0$$
at $t= \frac{n}{q}+ \frac{1}{2q}$: 
The left limit of $f$ at $t$: 
$$f(t-)=t- \frac{n}{q}= \frac{n}{q}+ \frac{1}{2q}- \frac{n}{q}= \frac{1}{2q}$$The right limit and value of $f$ at $t$: 
$$f(t+)= \frac{n+1}{q}- \frac{n}{q}- \frac{1}{2q}= \frac{1}{2q}$$Therefore, $f$ is continuous. Since $f$ attains values $0$ and $\frac{1}{2q}$, it is not constant.
