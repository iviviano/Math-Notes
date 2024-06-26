
>[!1]

(a)

$$\begin{align*}
K(x)&=  \int_{-1}^{1}(1-|y|)\cdot e^{2\pi ixy}\ dy\\
&= \int_{-1}^{0}(1-|y|)\cdot e^{2\pi ixy}\ dy+ \int_{0}^{1}(1-|y|)\cdot e^{2\pi ixy}\ dy\\
&= \int_{-1}^{0}(1+y)\cdot e^{2\pi ixy}\ dy+ \int_{0}^{1}(1-y)\cdot e^{2\pi ixy}\ dy\\
&\overset{\text{IBP}}{=} (1+y) \frac{e^{2\pi ixy}}{2\pi ix}\bigg|_{y=-1}^{0}-\int_{-1}^{0}\frac{e^{2\pi ixy}}{2\pi ix}\ dx\\
&\quad+ (1-y) \frac{e^{2\pi ixy}}{2\pi ix}\bigg|_{y=0}^{-1}+\int_{0}^{1}\frac{e^{2\pi ixy}}{2\pi ix}\ dx\\\\
&= \frac{1}{2\pi ix}- \frac{e^{2\pi ixy}}{(2\pi ix)^{2}}\bigg|_{y=-1}^{0}- \frac{1}{2\pi ix}+ \frac{e^{2\pi ixy}}{(2\pi ixy)^{2}}\bigg|_{y=0}^{1}\\
&= - \frac{1-e^{-2\pi ix}}{-(2\pi x)^{2}}+ \frac{e^{2\pi ix}-1}{-(2\pi x)^{2}}\\
&= \frac{2-e^{2\pi ix}-e^{-2\pi ix}}{(2\pi x)^{2}}\\
&= \frac{2-\Re \text{e}(e^{2\pi ix})}{(2\pi x)^{2}}\\
&= \frac{2-\cos 2\pi x}{(2\pi x)^{2}}\\
&= \frac{\sin^{2} \pi x}{(2\pi x)^{2}}\\
&= \left(\frac{\sin \pi x}{2\pi x}\right)^{2}
\end{align*}$$

(b) 

Applying a change of variables, we find a more useful expression of $K_{\lambda}$: $$
K_{\lambda}(x)=\lambda K(\lambda x)=\int_{-1}^{1}(1-|y|)e^{2\pi i \lambda xy}\ dy=\int_{-\lambda}^{\lambda}\left(1- \frac{|\nu|}{\lambda}\right)e^{2\pi i \nu x}\ d \nu
$$
Compute:
$$\begin{align*}
f\star K_{\lambda}&= \int_{-\infty}^{\infty}f(s)\cdot K_{\lambda}(t-s)\ ds\\
&= \int_{-\infty}^{\infty}f(s)\int_{-\lambda}^{\lambda} \left(1- \frac{|\nu|}{\lambda}\right)e^{2\pi i \nu (t-s)}\ d \nu\ ds\\
&\overset{\text{Fubini}}{=} \int_{-\lambda}^{\lambda} \left(1- \frac{|\nu|}{\lambda}\right)e^{2\pi i \nu t} \left(\underbrace{\int_{-\infty}^{\infty}f(s)~e^{-2\pi i \nu s}\ ds}_{=\widehat f(\nu)}\right)\ d \nu\\
&= \int_{-\lambda}^{\lambda} \left(1- \frac{|\nu|}{\lambda}\right)\widehat f(\nu)~e^{2\pi i \nu t}\ d \nu
\end{align*}$$
Since $$\left|f(s) \left(1- \frac{|\nu|}{\lambda}\right) e^{2\pi i \nu t-s}\right|=\left|f(s)\right|\cdot \underbrace{\left(1- \frac{|\nu|}{\lambda}\right)}_{\le1}\cdot\underbrace{\left| e^{2\pi i \nu t-s}\right|}_{=1}\le |f(s)|$$
we can apply Fubini because $f$ is a Schwartz function in $s$ and the $\lambda$ domain is compact. 

By problem 2, $K_{\lambda}$ is an approximate $\delta$ function and thus an $\mathbb{R}AI$ by Set 9, Problem 2 (c). Thus, the convolution $$
f\star K_{\lambda}\rightarrow f,\text{ uniformly}
$$
by the Approximate Identities on $\mathbb{R}$ Theorem. 

So, $$\begin{align*}
f(t)&= \lim_{\lambda \rightarrow \infty} f\star K_{\lambda}
\end{align*}$$





For the uniqueness theorem: if $\widehat f=\widehat g$, 
$$\begin{align*}
(f-g)(t)&= \lim_{\lambda \rightarrow \infty}\int_{-\lambda}^{\lambda}\left(1- \frac{|\nu|}{\lambda}\right)\widehat {[f-g]}(\nu)~e^{2\pi i \nu t}\ d \nu\\
&= \lim_{\lambda \rightarrow \infty}\int_{-\lambda}^{\lambda}\left(1- \frac{|\nu|}{\lambda}\right)[\widehat f-\widehat g](\nu)~e^{2\pi i \nu t}\ d \nu\\
&= \lim_{\lambda \rightarrow \infty}\int_{-\lambda}^{\lambda}\left(1- \frac{|\nu|}{\lambda}\right)\cdot 0\cdot~e^{2\pi i \nu t}\ d \nu\\
&= \lim_{\lambda\rightarrow \infty}0\\
&= 0
\end{align*}$$


>[!2]



>[!3]

Suppose (13) and let $f,g\in\mathcal{S}(\mathbb{R};\mathbb{C})$. Note that $f\cdot g,f\star g\in\mathcal{S}(\mathbb{R};\mathbb{C})$. Define:
$$h^{(-)}(x)=h(-x)$$for each $h\in\mathcal{S}(\mathbb{R};\mathbb{C})$. Note that $h^{(-)}\in\mathcal{S}(\mathbb{R};\mathbb{C})$.

$$\begin{align*}
\widehat h(\nu)&= \int_{-\infty}^{\infty}h(t)~e^{-2\pi i \nu t}\ dt\\
&= -\int_{\infty}^{-\infty}h(-t)~e^{2\pi i \nu t}\ dt\\
&= \int_{-\infty}^{\infty}h^{(-)}(t)~e^{2\pi i \nu t}\ dt\\
&= \check{h^{(-)}}(\nu)
\end{align*}$$
Also, note that $$(f\cdot g)^{(-)}=f^{(-)}\cdot g^{(-)}$$
Compute:
$$\begin{align*}
\widehat f\star \widehat g&= \check{f^{(-)}}\star\check{g^{(-)}}\\
&= \mathcal{F}^{-1}(\mathcal{F}(\check{f^{(-)}}\star\check{g^{(-)}}))\\
&= \mathcal{F}^{-1}(f^{(-)}\cdot g^{(-)})\\
&= \mathcal{F}^{-1}((f\cdot g)^{(-)})\\
&= \mathcal{F}(f\cdot g)
\end{align*}$$



Proof of (13):
$$\begin{align*}
\mathcal{F}[f\star g](\nu)&= \int_{-\infty}^{\infty}(f\star g)(t)~e^{-2\pi i \nu t}\ dt\\
&= \int_{-\infty}^{\infty}e^{-2\pi i \nu t} \left[\int_{-\infty}^{\infty}f(s)\cdot g(t-s)\ ds\right]\ dt\\
&\overset{\text{Fubnini}}{=} \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}f(s)\cdot g(t-s)~e^{-2\pi i \nu t}\ dt\ ds%\label{fubini}
\\
&= \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}f(s)\cdot g(u)~e^{-2\pi i \nu(u+s)}\ du\ ds\quad(\text{change variables: }u=t-s)\\
&= \int_{-\infty}^{\infty}f(s)~e^{-2\pi i \nu s}\underbrace{\left[\int_{-\infty}^{\infty}g(u)~e^{-2\pi i \nu u}\ du\right]}_{=\widehat g(\nu)}\ ds\\
&= \widehat g(\nu)\cdot\underbrace{\int_{-\infty}^{\infty}f(s)~e^{-2\pi i \nu s}\ ds}_{=\widehat{f}(\nu)}\\
&= (\widehat f\cdot\widehat g)(\nu)
\end{align*}$$
Note that (\ref{fubini}) we can apply Fubini's theorem for integration on $\mathbb{R}^{2}$, since the integrand satisfies an $\mathcal{L}^{1}$ bound:
$$
\left|e^{-2\pi i \nu t}f(s)\cdot g(t-s)\right|=\left|f(s)|\cdot |g(t-s)\right|
$$
because $f$ is Schwartz in $s$ and $g$ is Schwartz in $t$. 

>[!4]

The first inequality in the proof of the Uncertainty principle applies Cauchy Schwartz: $$
\|t\cdot f(t)\|_{\mathcal{L}^{2}(dt)}\cdot\| \frac{1}{2\pi i}\cdot \frac{df}{dt}(t)\|_{\mathcal{L}^{2}(dt)}\\
\ge \left|\left\langle t\cdot f(t), \frac{1}{2\pi i} \frac{df}{dt}(t)\right\rangle_{\mathcal{L}^{2}}\right|\\
$$
Here, equality holds if and only if the inner product functions are linearly dependent. That is, there exists a $\lambda\in \mathbb{C}$ such that
$$t\cdot f(t)=-\lambda f'(t)$$
By the general solution to the decay equation, we see that $$
f(t)=A\cdot e^{-\int \frac{t}{\lambda}dt}= A\cdot e^{-\frac{t^{2}}{2\lambda}}
$$for some $A\in \mathbb{C}$. 

The second inequality in the Uncertainty principle proof reduced the modulus of a complex number by looking at the modulus of the real part. Equality holds here if and only if the imaginary part is 0:
$$\begin{equation} %\label{im_zero}
\Im \text{m}(\langle t f(t),f'(t)\rangle)=0
\end{equation}
$$
Computing the LHS,
$$\begin{align*}
\Im \text{m}(\langle tf(t),f'(t))&= \frac{1}{2i}(\langle tf(t),f'(t)\rangle-\overline{\langle tf(t),f'(t)\rangle})\\
&= \frac{1}{2i}(\langle tf(t),f'(t)\rangle-\langle f'(t),tf(t)\rangle)\\
&= \frac{1}{2i}(\langle f(t),tf'(t)\rangle+\langle f(t),tf'(t)+f(t)\rangle)\\
&= \frac{1}{2i}(\langle f(t),f(t)+2tf'(t\rangle)\\
&= \frac{1}{2i}(\langle f(t),f(t)\rangle+\langle f(t),2tf'(t)\rangle)\\
&= \frac{1}{2i}\left(\|f\|_{\mathcal{L}^{2}}^{2}+\int_{-\infty}^{\infty}\overline{f(t)}\cdot2tf'(t)\ dt\right)\\
&= \frac{1}{2i}\left(1-\int_{-\infty}^{\infty}\overline{f(t)}\cdot \frac{2t^{2}}{\lambda}f(t)\ dt\right)\\
&= \frac{1}{2i}\left(1-\frac{2}{\lambda}\int_{-\infty}^{\infty} \underbrace{t^{2}|f(t)|^{2}}_{\ge0}\ dt\right)
\end{align*}$$
we see that (\ref{im_zero}) implies $$
\lambda= 2\int_{-\infty}^{\infty}t^{2}|f(t)|^{2}\ dt
$$so, $\lambda\in \mathbb{R}$ with $\lambda>0$. 

Also, note the normalization condition: $$\begin{align*}
1&= \|f\|_{\mathcal{L}^{2}}^{2}\\
&= \int_{-\infty}^{\infty}|f(t)|^{2}\ dt\\
&= |A|^{2}\int_{-\infty}^{\infty} e^{- \frac{t^{2}}{\lambda}}\ dt\\
&= |A|^{2}\sqrt{\pi \lambda}\underbrace{\int_{-\infty}^{\infty} e^{-\pi u^{2}}\ du}_{=1}\quad(\text{change variables: }u= \frac{t}{\sqrt{\pi \lambda}})\\
&= |A|^{2}\sqrt{\pi \lambda}
\end{align*}$$
Where the real change of variables is allowed since we showed $\lambda>0$. So, $|A|^{2}= \frac{1}{\sqrt{\pi \lambda}}$. Since $\lambda>0$ we can write: $$\lambda= \frac{1}{\pi|A|^{4}}$$ 
Therefore, we have that the class of functions which minimize uncertainty is $$\begin{equation} %\label{norm_gaus}
f(t)=Ae^{-\pi|A|^{4} \frac{t^{2}}{2}}
\end{equation}$$
where $A\in \mathbb{C}$ is a parameter. 

Via explicit computation, we can verify that $f$ defined in (\ref{norm_gaus}) minimizes uncertainty. First compute the Fourier Transform with Gaussian invariance: $$
\widehat f(\nu) = \frac{1}{|A|^{2}}e^{\frac{-\pi \nu^{2}}{|A|^{4}}} 
$$
Noting that the standard deviation of a normal random variable with distribution: $$
g(x)= \frac{1}{\sigma \sqrt{2\pi}}e^{- \frac{x^{2}}{2\sigma^{2}}}
$$
is $\sigma$, we see $$\begin{align*}
w_{t}&= \frac{1}{\sqrt{2\pi}|A|^{2}}\\
w_{\nu}&= \frac{|A|^{2}}{\sqrt{2\pi}}
\end{align*}$$for $f$ and thus, $$
w_{t}\cdot w_{\nu}= \frac{1}{4\pi}
$$

(b)

Let $f\in\mathcal{S}(\mathbb{R};\mathbb{C})$ with $\nu_\text{avg}=0$.

Define $g:\mathbb{R}\rightarrow \mathbb{C}$ with $$g(t)=f(t+T_\text{avg})$$
Note that $$\begin{align*}
\left|\widehat g(\nu)\right|&= \left|\int_{-\infty}^{\infty}g(t)~e^{-2\pi i \nu t}\ dt\right|\\
&= \left|\int_{-\infty}^{\infty}f(t+T_\text{avg})~e^{-2\pi i \nu t}\ dt\right|\\
&= \left|\int_{-\infty}^{\infty}f(\tau)~e^{-2\pi i \nu(\tau-T_{\text{avg}})}\ d \tau \right|\quad(\text{change variables: }\tau=t+T_\text{avg})\\
&= \left|e^{2\pi i \nu T_\text{avg}}\underbrace{\int_{-\infty}^{\infty}f(\tau)~e^{-2\pi i \nu \tau}\ d \tau}_{=\widehat f(\nu )} \right|\\
&= \left|e^{2\pi i \nu T_\text{avg}}\right|\cdot \left|\widehat f(\nu)\right|\\
&= \left|\widehat f(\nu)\right|
\end{align*}$$
Thus, the distributions $|\widehat g|^{2}$ and $\left|\widehat f\right|^{2}$ have the same mean and standard deviation. We have the expected value of $t$ for distribution $|g|^{2}$:
$$\begin{align*}
T'_\text{avg}&= \int_{-\infty}^{\infty}t\cdot |g(t)|^{2}\ dt\\
&= \int_{-\infty}^{\infty}t\cdot |f(t+T_\text{avg})|^{2}\ dt\\
&= \int_{-\infty}^{\infty}(\tau-T_\text{avg})|f(\tau)|^{2}\ d \tau\quad(\text{change variables: }\tau=t+T_\text{avg})\\
&= \underbrace{\int_{-\infty}^{\infty}\tau|f(\tau)|^{2}\ d \tau}_{=T_\text{avg}}- T_{\text{avg}}\underbrace{\int_{-\infty}^{\infty}|f(\tau)|^{2}\ d \tau}_{=1}\\
&= T_\text{avg}-T_\text{avg}\\
&= 0
\end{align*}
$$

and the variances:
$$\begin{align*}
\underbrace{w_{t}^{2}}_{\text{for }f}&= \int_{-\infty}^{\infty}|t-T_\text{avg}|^{2} |f(t)|^{2}\ dt\\
&= \int_{-\infty}^{\infty}|\tau|^{2}|f(\tau+T_\text{avg})|^{2}\ d \tau\quad(\text{change variables: }\tau=t-T_\text{avg})\\
&= \int_{-\infty}^{\infty}|\tau|^{2}|g(\tau)|^{2}\ d \tau\\
&= \underbrace{w_{t}^{2}}_{\text{for }g}
\end{align*}$$


Since $g\in\mathcal{S}(\mathbb{R};\mathbb{C})$ with $T'_\text{avg}=0$, it satisfies the Uncertainty Principle. So, for $f$, we have $$
w_{t}\cdot w_{\nu}\ge \frac{1}{4\pi}
$$








Let $f\in\mathcal{S}(\mathbb{R};\mathbb{C})$. By the inversion property, let $h:\mathbb{R}\rightarrow \mathbb{C}$ such that $$
\widehat h(\nu)=\widehat f(\nu+\nu_\text{avg})
$$
By the above computation, $|\widehat h|^{2}$ is centered at 0 with the same standard deviation $w_\nu$ as $|\widehat f|^{2}$. So, by Lemma \ref{uncertainty_lemma}, we have the uncertainty principle for $h$.

Apply the inversion property:
$$\begin{align*}
|h(\nu)|&= \left|\int_{-\infty}^{\infty}\widehat h(\nu)~e^{2\pi i \nu t}\right|\ d \nu\\
&=\left| \int_{-\infty}^{\infty}\widehat f(\nu+\nu_\text{avg})e^{2\pi i \nu t}\ d \nu\right|\\
&=\left| \int_{-\infty}^{\infty}\widehat f(s)e^{2\pi i t (s-\nu_\text{avg})}\ ds\right|\quad(\text{change variables: }s=\nu+\nu_\text{avg})\\
&=\left| e^{-2\pi i t\nu_\text{avg}}\underbrace{\int_{-\infty}^{\infty}\widehat f(s)~e^{2\pi i t s}\ ds}_{=f(t)}\right|\\
&=\left| e^{2\pi i \alpha \nu}~ f(t)\right|\\
&= \left|f(t)\right|
\end{align*}$$
Thus, $h$ has the same intensity as $f$ for all $t\in \mathbb{R}$. So, $|h|^{2}$ and $|f|^{2}$ have the same expected value and standard deviation in the time domain. Since $h$ and $f$ have the same width in both the time and frequency domain, the uncertainty principle extends to $f$: $$w_{t}\cdot w_{\nu}\ge \frac{1}{4\pi}$$
