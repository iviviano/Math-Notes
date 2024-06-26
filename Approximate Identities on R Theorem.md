---
mathLink: approximate identities on $\mathbb{R}$ theorem
---
>[!thm]
>For $k\in \mathbb{N}_{0}\cup\{\infty\}$, let $\{\phi_{\lambda},\lambda>0\}$ be a $\mathcal{C}^{k}$-[[Approximate Identity on R]]. Then, for every [[Function]] $f\in\mathcal{C}_{\infty}(\mathbb{R};\mathbb{C})$, one has $$f\star \phi_{\lambda} \rightarrow f,\text{ uniformly as }\lambda \rightarrow \infty$$ 

>[!note]
>We use that $f$ [[Vanishes at Infinity]] and is an [[L1 Function]] to show it is [[Uniform Continuity]] and [[Bounded Function into R]]. I think that [[Uniform Continuity]], [[Bounded Function into R]] and an [[L1 Function]] is actually the same space (see second lemma below following proof)

>[!prop] Lemma
[[Continuous]] [[Function]]s that [[Vanishes at Infinity]] are [[Uniform Continuity]]. 

>[!proof] Proof of the Lemma
Let $f\in\mathcal{C}_{\infty}$, and let $\epsilon>0$ be given. Pick $R>0$ such that for all $|x|\ge R$, $$|f(x)|< \frac{\epsilon}{3}$$
Since continuous functions are uniformly continuous on compact sets, pick $\delta>0$ such that for all $x,y\in[-R,R]$, $$|f(x)-f(y)|< \frac{\epsilon}{3}$$
>For all $x,y\in \mathbb{R}$ with $|x-y|<\delta$, we consider three cases without loss of generality. If $x,y\in[-R,R]$, we have $$|f(x)-f(y)|< \frac{\epsilon}{3}<\epsilon$$
If $x\in[-R,R]$ and $y>R$, $$|f(x)-f(y)|\le |f(x)-f(R)|+|f(R)-f(y)|< \frac{\epsilon}{3}+|f(R)|+|f(y)|< \frac{\epsilon}{3}+ \frac{\epsilon}{3}+ \frac{\epsilon}{3}=\epsilon$$
If $x,y\notin[-R,R]$, $$|f(x)-f(y)|\le |f(x)|+|f(y)|< \frac{\epsilon}{3}+ \frac{\epsilon}{3}\le\epsilon$$
Thus, $f$ is uniformly continuous.

Let $f\in \mathcal{C}_{\infty}(\mathbb{R};\mathbb{C})$. Let $\epsilon>0$ be given. Since $f$ vanishes at $\infty$, it is uniformly continuous on $\mathbb{R}$. Pick $\delta>0$ such that for all $x,y\in \mathbb{R}$ with $|x-y|<\delta$, $|f(x)-f(y)|<\epsilon$.

Since $f$ vanishes at $\infty$, pick $R>0$ such that $$\|f\|_{\infty;\mathbb{R}\setminus(-R,R)}\le \epsilon$$
We also have that $f$ is bounded on $[-R,R]$ by (EVT). Thus, $f$ is bounded with $$\|f\|_{\infty}=\max\{\|f\|_{\infty;[-R,R]} ,\underbrace{\|f\|_{\infty;\mathbb{R}\setminus(-R,R)}}_{\le \epsilon}\}<\infty$$
Pick $\Lambda$ such that for all $\lambda>\Lambda$, $$\int_{\mathbb{R}\setminus(-\delta,\delta)}|\phi_{\lambda}(t)|\ dt<\epsilon$$
Let $C$ be the constant given by $\mathbb{R}AI$-2. 

If $\lambda>\Lambda$,
$$\begin{align*}
\left|(\phi_{\lambda}\star f)(t)-f(t)\right|&= \left|\int_{-\infty}^{\infty}\phi_{\lambda}(s)\cdot f(t-s)\ ds-f(t)\right|\\
&= \left|\int_{-\infty}^{\infty}\phi_{\lambda}(s)\cdot f(t-s)\ ds-f(t)\int_{-\infty}^{\infty}\phi_{\lambda}(s)\ ds\right|\\
&= \left|\int_{-\infty}^{\infty}\phi_{\lambda}(s)(f(t-s)-f(t))\ ds \right|\\
&= \left|\int_{\mathbb{R}\setminus(-\delta,\delta)}\phi_{\lambda}(s)(f(t-s)-f(t))\ ds+ \int_{-\delta}^{\delta}\phi_{\lambda}(s)(f(t-s)-f(t))\ ds\right|\\
&\le \int_{\mathbb{R}\setminus(-\delta,\delta)}\left|\phi_{\lambda}(s)(f(t-s)-f(t))\right|\ ds+ \int_{-\delta}^{\delta}\left|\phi_{\lambda}(s)(f(t-s)-f(t))\right|\ ds\\
&\le \int_{\mathbb{R}\setminus(-\delta,\delta)}|\phi_{\lambda}(s)|\cdot\underbrace{|(f(t-s)-f(t))|}_{\le2\|f\|_{\infty}}\ ds+ \int_{-\delta}^{\delta}|\phi_{\lambda}(s)|\cdot\underbrace{|(f(t-s)-f(t))|}_{<\epsilon}\ ds %\label{unif}
\\
&\le 2\|f\|_{\infty}\underbrace{\int_{\mathbb{R}\setminus(-\delta,\delta)}|\phi_{\lambda}(s)|\ ds}_{<\epsilon}+ \epsilon\int_{-\delta}^{\delta}|\phi_{\lambda}(s)|\ ds\\
&< 2\epsilon\|f\|_{\infty}+\epsilon\underbrace{\int_{-\infty}^{\infty}|\phi_{\lambda}|\ ds}_{\le C\text{, by }\mathbb{R}AI-2}\\
&\le 2\epsilon\|f\|_{\infty}+\epsilon C
\end{align*}$$
where the bound on $|f(t-s)-f(t)|$ in (\ref{unif}) comes from the uniform continuity of $f$ and $|s|<\delta$. Since this bound is a constant (independent of $t$) multiple of $\epsilon$, $$f\star \phi_{\lambda}=\phi_{\lambda}\star f\rightarrow 0,\quad \text{uniformly in }t$$for all $f\in\mathcal{C}_{\infty}(\mathbb{R};\mathbb{C})$.


>[!prop] Lemma
This is the other direction of the previous lemma: $f\in\mathcal{L}^{1}$ and $f$ uniformly continuous implies $f\in\mathcal{C}_{0}$.

>[!proof]

Suppose $f\notin\mathcal{C}_{0}$. Pick $\epsilon>0$ such that for all $R>0$, there exists $|x|>R$ such that $$|f(x)|>\epsilon$$
By uniform continuity, we have $\delta>0$ such that for all $x,y\in\mathbb{R}$, $$|f(x)-f(y)|< \frac{\epsilon}{2}$$
Consider $R>0$ such that $$\int_{\mathbb{R}\setminus(-R,R)}|f(x)|\ dx<\delta\epsilon$$
by $f\in\mathcal{L}^{1}$. Pick $x$ with $|x|>R$, $|f(x)|>\epsilon$, and $$f(x)=\max_{t\in[x-\delta,x+\delta]}(f(t))$$
by the [[Extreme Value Theorem]].

Note that for $t\in(x-\delta,x+\delta)$, the second half of the [[Triangle Inequality]] implies that $$|f(x)|-|f(t)|=|\ |f(x)|-|f(t)|\ |\le|f(x)-f(t)|< \frac{\epsilon}{2}$$
Since $|f(x)|<\epsilon$, $$|f(t)|\ge \frac{\epsilon}{2}$$
We have:
$$\begin{align*}
\int_{\mathbb{R}\setminus(-R,R)}|f(x)|\ dx&\ge \int_{x-\delta}^{x+\delta}\underbrace{|f(t)|}_{\ge \frac{\epsilon}{2}}\ dt\\
&\ge 2\delta\cdot \frac{\epsilon}{2}\quad(\text{mL estimate})\\
&= \delta\epsilon\\
&> \int_{\mathbb{R}\setminus(-R,R)}|f(x)|\ dx
\end{align*}$$a contradiction. Thus, $f\in\mathcal{C}_{0}$. 

