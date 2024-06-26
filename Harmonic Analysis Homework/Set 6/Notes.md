>[!1]

(b)
$$
g^{(\pm)}_{\epsilon;t_{0}}(s):=\begin{cases} \frac{f(t_{0}-s)-f(t_{0})}{\sin(\pi s)}e^{\pm \pi is} & ,\text{ if }\epsilon\le|s|\le \frac{1}{2} \\
0 & ,\text{ if }s\in(-\epsilon,\epsilon)\end{cases}
$$

>[!prop] Lemma
>Let $\epsilon>0$ be given. Then, for each $t\in A$, there exists $N_{t}\in \mathbb{N}$ and $\delta_{t}>0$ so that for all $s\in \mathbb{R}$ with $|s-t|<\delta_{t}$, one has $$\left|\widehat{[g_{\epsilon;s}^{(\pm)}]_{m}}\right|<\epsilon,\text{ for all }|m|\ge N_{t}$$


Let $\epsilon\le |s|\le \frac{1}{2}$ and let $\eta>0$ be given. By the uniform continuity of $f$, pick $\delta$ such that if $|s_{0}-s_{1}|<\delta$, $|f(s_{0})-f(s_{1})| <\frac{\eta}{3}$. For such $s_{0},s_{2}$ and an arbitrary $\epsilon\le |s|\le\frac{1}{2}$,
$$\begin{align*}
\left|g_{\epsilon;s_{0}}^{(\pm)}(s)-g^{(\pm)}_{\epsilon;s_{1}}(s)\right|&= \left|\frac{f(s_{0}-s)-f(s_{0})}{\sin(\pi s)}e^{\pm \pi is}-\frac{f(s_{1}-s)-f(s_{1})}{\sin(\pi s)}e^{\pm \pi is}\right|\\
&= \left|\frac{(f(s_{0}-s)-f(s_{1}-s))+(f(s_{1})-f(s_{0}))}{\sin(\pi s)}e^{\pm \pi is}\right|\\
&\le (\underbrace{|f(s_{0}-s)-f(s_{1}-s)|}_{< \frac{\eta}{3}}+\underbrace{|f(s_{1})-f(s_{0})|}_{< \frac{\eta}{3}})\cdot \underbrace{\frac{\|e^{\pm \pi is}\|_{\infty}}{\|\sin(\pi s)\|_{\infty}}}_{=1}\\
&< \frac{2\eta}{3}
\end{align*}$$
Since this bound is independent of $s$, we get$$
\left\|g_{\epsilon;s_{0}}^{(\pm)}(s)-g^{(\pm)}_{\epsilon;s_{1}}(s)\right\|_{\infty}\le \frac{2\eta}{3}<\eta%\label{sup_bound}
$$
Let $t_{0}\in A$. By the [[Riemann-Lebesgue Lemma]], there exists $N_{t_{0}}\in \mathbb{N}$ such that for all $n\ge N_{t_{0}}$,  
$$\begin{align*}
\left|\widehat{[g_{\epsilon;t_{0}}^{(\pm)}]}_{n}\right|< \frac{\epsilon}{2}
\end{align*}
$$
Take $\eta=\frac{\epsilon}{2}$ in \ref{sup_bound} and choose $\delta_{t_{0}}$ by uniform continuity as above. If $|s_{0}-t_{0}|< \delta_{t_{0}}$, then
$$\begin{align*}
\left|\widehat{[g^{(\pm)}_{\epsilon;s_{0}}]}_{n}\right|&= \left|\widehat{[g^{(\pm)}_{\epsilon;s_{0}}]}_{n}-\widehat{[g^{(\pm)}_{\epsilon;t_{0}}]}_{n}+\widehat{[g^{(\pm)}_{\epsilon;t_{0}}]}_{n}\right|\\
&\le \left|\widehat{[g^{(\pm)}_{\epsilon;s_{0}}]}_{n}-\widehat{[g^{(\pm)}_{\epsilon;t_{0}}]}_{n}\right|+\left|\widehat{[g^{(\pm)}_{\epsilon;t_{0}}]}_{n}\right|\\
&= \left|\widehat{[g^{(\pm)}_{\epsilon;s_{0}}-g^{(\pm)}_{\epsilon;t_{0}}]}_{n}\right|+\left|\widehat{[g^{(\pm)}_{\epsilon;t_{0}}]}_{n}\right|\\
&< \left\|g_{\epsilon;s_{0}}^{(\pm)}(s)-g^{(\pm)}_{\epsilon;s_{1}}(s)\right\|_{\infty}+ \frac{\epsilon}{2} %\label{apply_apriori}\\
&< \frac{\epsilon}{2}+\frac{\epsilon}{2}\\
&= \epsilon
\end{align*}$$
where for (\ref{apply_apriori}), we use the infinity-norm bound for Fourier coefficients from Set 2, Problem 5, part (a). 


>[!2]


(a) 

($\impliedby$) Suppose $\alpha\in \mathbb{Q}$. Let $\alpha= \frac{p}{q}$ with $p,q\in \mathbb{N}$ and $\gcd(p,q)=1$. For each $x\in[0,1)$, $$\begin{align*}
R^{q}_{\alpha}(x)&= x+ q\cdot \alpha\mod1\\
&= x+p\mod1\\
&= x
\end{align*}$$So, $R_{\alpha}^{q}=\text{id}$. Thus, $R_{\alpha}$ is periodic.

($\implies$) Suppose $R_{\alpha}^{q}=\text{id}$ for some $q\in \mathbb{N}$.  Then for all $x\in[0,1)$, $$\begin{align*}
x&= R_{\alpha}^{q}(x)= x+ q\cdot \alpha\mod1
\end{align*}$$Therefore, $q\cdot \alpha\equiv 0\mod1$, which implies $q \alpha=p\in\mathbb{Z}$. Since $q$ is nonzero, we may divide to get $$\alpha= \frac{p}{q}\in\mathbb{Q}$$

(b) 

We argue by contrapositive. Suppose $R^{n}_{\alpha}(x)=R^{m}_{\alpha}(x)$ for some $x\in [0,1)$ and $n<m\in \mathbb{N}$. We have $$x+ n \alpha\equiv x+m \alpha\mod1$$So, $$(m-n)\alpha\equiv0\mod1$$Since $0\ne m-n\in \mathbb{N}$, we have $\alpha\in\mathbb{Q}$ as before. 



>[!3]

Let $N\in \mathbb{N}$ such that $\frac{1}{N}<\epsilon$ by the Archimedean property of $\mathbb{R}$. Divide the half open unit interval into $N$ half open intervals: $$I_{i}=\left[\frac{i}{N},\frac{i+1}{N}\right),0\le i< N$$Note that $$\bigcup_{i=0}^{N-1}I_{i}=[0,1)$$so any collection of $N+1$ points in $[0,1)$ must have at least two elements in $I_{i}$ for some $0\le i<N$ by the Pigeonhole Principle. One such collection is the finite orbit: $$\mathcal{O}_{\alpha}(0,N)=\{R_{\alpha}^{k}(0):0\le k\le N\}$$So, we may pick $n_{1}< n_{2}\le N$ and $i< N$ with $$R_{\alpha}^{n_{1}}(0),R_{\alpha}^{n_{2}}(0)\in I_{i}$$Note that $$0\le|R_{\alpha}^{n_{1}}(0)-R_{\alpha}^{n_{2}}(0)|< \frac{i+1}{N}- \frac{i}{N}= \frac{1}{N}< \epsilon$$We may also write $$\begin{align*}
R_{\alpha}^{n_{1}}(0)-R_{\alpha}^{n_{2}}(0)&= n_{1}\alpha-n_{2}\alpha\mod1
\end{align*}$$Pick $k_{0}\in\mathbb{Z}$ such that $$n_{1}\alpha-n_{2}\alpha-k_{0}=n_{1}\alpha-n_{2}\alpha\mod1$$Then,
$$\begin{align*}
d_{c}(n_{1}\alpha,n_{2}\alpha)&= \min\{|\alpha(n_{1}-n_{2})-k|,k\in \mathbb{Z}\}\\
&\le |\alpha n_{1}-\alpha n_{2}-k_{0}|\\
&= |R_{\alpha}^{n_{1}}(0)-R_{\alpha}^{n_{2}}(0)|\\
&< \frac{1}{N}\\
&< \epsilon
\end{align*}$$

(b)

Suppose not: Let $I=(a,b)$ and let $k_{0}\in \mathbb{N}$ be the first $k$ such that $$R^{k_{0}M}_{\alpha}(x)\le a$$and $$R^{(k_{0}-1)M}_{\alpha}(x)\ge b$$
Note that $$R_{\alpha}^{m}(x)=x+n \alpha\mod1=x+R^{m}_{\alpha}(0)\mod1$$
So, $$\begin{equation}
k_{0}(n_{2}-n_{1})\alpha+x\mod1\le a
\end{equation}$$and $$\begin{equation}
(k_{0}-1)(n_{2}-n_{1})\alpha+x\mod1\ge b
\end{equation}$$Subtracting \ref{lower} from \ref{upper} gives $$(n_{1}-n_{2})\alpha\mod1\ge b-a=\epsilon$$
which contradicts \ref{}.

(c) Let $M\in \mathbb{N}$ and $x\in[0,1]$ be given. Divide $I$ into $M$ subintervals: $$I_{i}=\left(a+\frac{i \epsilon}{M},a+ \frac{(i+1)\epsilon}{M}\right),\text{ for }0\le i< M-1$$and $$I_{M}=\left(b- \frac{\epsilon}{M},b\right)$$By [[Kronecker's Theorem]], there exists $n_{i}\in \mathbb{N}$ such that $$R^{n_{i}}_{\alpha}(x)\in I_{i}\subseteq I$$Note that $n_{i}\ne n_{j}$ for all $i\ne j$, since $I_{i}\cap I_{j}=\emptyset$. We have shown that $$\#(\mathcal{O}_{\alpha}(x)\cap I)\ge M$$Since $M$ was arbitrary, $R^{n}_{\alpha}(x)\in I$ for infinitely many $n$.  



>[!4]


Prove:

>[!prop]
>Let $a,b,c\in \mathbb{N}$ with $b,c≠1$. Suppose there exists a prime $p$ which only contributes to the [[Prime Factorization]] of precisely one of $a$ or $b$ or $c$. Then, $\log_{a}(b)$ and $\log_{a}(c)$ are independent over $\mathbb{Q}$: there are no $n_{1},n_{2},n_{3}\in\mathbb{Z}$ such that $$n_{1}\log_{a}(b)+n_{2}\log_{a}(c)=n_{3}$$besides $n_{1}=n_{2}=n_{3}=0$


Suppose there exist $n_{1},n_{2},n_{3}$ nonzero satisfying $$n_{1}\log_{a}b+n_{2}\log_{a}c=n_{3}$$Using $\log$ properties, we write $$a^{n_{3}}=b^{n_{1}}c^{n_{2}}$$We see that $$\{q:q\text{ is a prime factor of }a\}=\{q:q\text{ is a prime factor of }c\}\cup\{q:q\text{ is a prime factor of }b\}\}$$so there is no prime $p$ contributing to the prime factorization of precisely one of $a$, $b$, or $c$.
 


