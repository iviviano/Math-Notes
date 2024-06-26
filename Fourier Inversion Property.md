>[!thm]
Let $f\in\mathcal{S}(\mathbb{R};\mathbb{C})$. Then for all $t\in \mathbb{R}$, we have $$f(t)=\int_{-\infty}^{\infty}\widehat f(\nu)~e^{2\pi i \nu t}d \nu$$In particular, the [[Fourier Map]] $\mathcal{F}:\mathcal{S}\rightarrow \mathcal{S}$ is [[Bijective]].

>[!proof] Physics "Proof":
$$\begin{align*}
\int_{-\infty}^{\infty}\hat f(\nu)e^{2\pi i  \nu t}\ d \nu &= \int_{-\infty}^{\infty} \left(\int_{-\infty}^{\infty}f(s)e^{-2\pi i  \nu s}\ ds\right)e^{2\pi i \nu t}\ d \nu\\
&= \int_{-\infty}^{\infty}\underbrace{\left(\int_{-\infty}^{\infty}e^{2\pi  i  \nu (t-s)}\ d \nu\right)}_{:=\delta(t-s)}f(s)\ d s\quad(\text{change integration order})\\
&= \int_{-\infty}^{\infty}f(s)\delta(t-s)\ ds
\end{align*}$$
where we can change the integration order by [[Fubini's Theorem on R2]]

Since $\delta(t-s)$ is "infinitely concentrated" at $t=s$, we recover $f$: $$\int_{-\infty}^{\infty}f(s)\delta(t-s)\ ds=(f\star \delta)(t)=f(t)$$
 Problem: we don't have the necessary [[Script-L1 Norm]] hypothesis: $$|f(s)e^{2\pi i \nu (t-s)}|= |f(s)|\notin\mathcal{L}^{1}(dsd \nu)$$we can't integrate this against $\nu$, since it has no $\nu$-dependence.


>[!proof] Correct Proof

Let $g_{\epsilon}$ be the approximate $\delta$ function from the [[Gaussian]]. This is a [[Approximate Identity on R]], since $g$ is normalized ([[4-17]]) and approximate delta functions form an $\mathbb{R}AI$ ([[set_9.pdf]]):
$$g_{\epsilon}(x)= \frac{1}{\epsilon}g\left(\frac{x}{\epsilon}\right)$$
By the [[Approximate Identities on R Theorem]], 
$$\begin{align*}
f(t)&= \lim_{\epsilon \rightarrow 0^{+}}[f\star g_{\epsilon}](t)\\
&= \lim_{\epsilon \rightarrow 0^{+}}\int_{-\infty}^{\infty}f(s)\underbrace{g_{\epsilon}(t-s)}_{\epsilon^{-1}\widehat{g_{\epsilon^{-1}}}(t-s)}\ ds\\
&= \lim_{\epsilon\rightarrow 0^{+}}\int_{-\infty}^{\infty}f(s) \left(\int_{-\infty}^{\infty}e^{-\epsilon x^{2}}e^{-2\pi i(t-s)x}\ dx\right)\ ds\\
&\overbrace{=}^{\text{Fubini}} \lim_{\epsilon\rightarrow 0^{+}}\int_{-\infty}^{\infty}\underbrace{\left(\int_{-\infty}^{\infty}f(s)e^{-2\pi i s(-x)}\ ds\right)}_{\widehat{f}(-x)}e^{-\epsilon x^{2}}e^{-2\pi i tx}\ dx\\
&= \lim_{\epsilon\rightarrow 0^{+}}\int_{\infty}^{-\infty}\widehat f(\nu)e^{-\epsilon \nu^{2}}e^{2\pi i \nu t}\ (-d \nu) \quad(\text{change variables }\nu=-x)\\
&= \lim_{\epsilon\rightarrow 0^{+}}\int_{-\infty}^{\infty}\widehat f(\nu)e^{2\pi i \nu t}\cdot e^{-\epsilon \nu^{2}}\ d \nu\\
&= \int_{-\infty}^{\infty}\widehat f(\nu)e^{2\pi i \nu t}\underbrace{(\lim_{\epsilon \rightarrow 0^{+}}e^{-\epsilon \nu^{2}})}_{=1}\ d \nu\\
&= \int_{-\infty}^{\infty}\widehat f(\nu)e^{2\pi i \nu t}\ d \nu
\end{align*}$$
where we use the [[Uncertainty Principle]] for the [[Gaussian]] and [[Gaussian Invariance]] to go from $g_{\epsilon}$ to its [[Fourier Transform]] ([[4-17]]).

Now, we can actually use [[Fubini's Theorem on R2]], since $$|f(s)e^{-\epsilon x^{2}}e^{-2\pi i (t-s)x}|= |f(s)|\cdot|e^{-\epsilon x^{2}}|$$
since this is a product of a [[Schwartz Function]] function in $s$ and a [[Schwartz Function]] function in $x$, it is $\mathcal{L}^{1}(dxds)$. 

We were able to move the limit inside the integral since $$e^{-\epsilon \nu^{2}}\rightarrow 1$$uniformly in $\nu$ on all [[Compactness]] [[Subset]]s of $\mathbb{R}$ (it does not converge uniformly on $\mathbb{R}$)