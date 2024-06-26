>[!1]

(a)
Suppose $f\in\mathcal{L}^{1}$. That is, $$\int_{-\infty}^{\infty}|f(t)|\ dt<\infty$$Since the integral converges, we have both $$\begin{align*}
\int_{0}^{\infty}|f(t)|\ dt&< \infty\\
\int_{-\infty}^{0}|f(t)|\ dt&< \infty
\end{align*}$$
Note that sequence convergence always implies Cauchy sequence. Let $\epsilon>0$ be given and pick $N_{-},N_{+}\in \mathbb{N}$ such that
$$\begin{align*}
\left|\int_{0}^{R}|f(t)|\ dt-\int_{0}^{S}|f(t)|\ dt\right|<\epsilon,\quad \text{for all }R>S\ge N_{+}\\
\left|\int_{-R}^{0}|f(t)|\ dt-\int_{-S}^{0}|f(t)|\ dt\right|<\epsilon,\quad \text{for all }R>S\ge N_{-}\\
\end{align*}$$
For $R>S\ge N_{+}$, we have
$$\begin{align*}
\left|\int_{0}^{R}f(t)\ dt-\int_{0}^{S}f(t)\ dt\right|&= \left|\int_{S}^{R}f(t)\ dt\right|\\
&\le \int_{S}^{R}|f(t)|\ dt\\
&= \underbrace{\int_{0}^{R}|f(t)|\ dt-\int_{0}^{S}|f(t)|\ dt}_{\ge0}\\
&= \left|\int_{0}^{R}|f(t)|\ dt-\int_{0}^{S}|f(t)|\ dt\right|\\
&< \epsilon
\end{align*}$$
and similarly for $R>S\ge N_{-}$, we have 
$$\begin{align*}
\left|\int_{-R}^{0}f(t)\ dt-\int_{-S}^{0}f(t)\ dt\right|&= \left|\int_{-R}^{-S}f(t)\ dt\right|\\
&\le \int_{-R}^{-S}|f(t)|\ dt\\
&= \underbrace{\int_{-R}^{0}|f(t)|\ dt-\int_{-S}^{0}|f(t)|\ dt}_{\ge0}\\
&= \left|\int_{-R}^{0}|f(t)|\ dt-\int_{-S}^{0}|f(t)|\ dt\right|\\
&< \epsilon
\end{align*}$$
This shows that both $\int_{0}^{R}f(t)\ dt$ and $\int_{-R}^{0}f(t)\ dt$ are Cauchy sequences in $\mathbb{R}$. Since $\mathbb{R}$ is complete, Cauchy implies convergence. Thus, the improper Riemann integral of $f$ converges. 

(b)


Let $f\in\mathcal{S}(\mathbb{R};\mathbb{C})$ and let $$C_{m,n}:=\sup_{x\in \mathbb{R}}|x^{m}f^{(n)}(x)|$$
Let $1<R\in \mathbb{R}$ be given. Estimate $$\begin{align*}
\int_{-R}^{R}|f(x)|\ dx&= \underbrace{\int_{-1}^{1}|f(x)|\ dx}_{:=C\in \mathbb{R}}+\int_{[-R,R]\setminus(-1,1)}|f(x)|\ dx\\
&= C+\int_{[-R,R]\setminus(-1,1)} \frac{1}{x^{2}}\underbrace{|x^{2}f(x)|}_{\le C_{2,0}}\ dx\\
&\le C+ C_{2,0}\int_{[-R,R]\setminus(-1,1)} \frac{1}{x^{2}}\ dx\\
&= C+2C_{2,0}\int_{1}^{R} \frac{1}{x^{2}}\ dx\\
&= C+2C_{2,0} \left(\frac{-1}{x}\bigg|_{1}^{R}\right)\\
&= C+ 2C_{2,0}\left(1- \frac{1}{R}\right)
\end{align*}$$
Thus, $$\lim_{R\rightarrow \infty}\int_{-R}^{R}|f(x)|\ dx\le\sup_{R>1}\left(C+2C_{2,0}\left(1- \frac{1}{R}\right)\right)= C+2C_{2,0}<\infty$$
This shows that the Cauchy principal value and thus also the improper Riemann integral of $|f|$ is finite. So, $f\in\mathcal{L}^{1}$.

---

Let $f\in\mathcal{S}(\mathbb{R};\mathbb{C})$ and let $$C_{m,n}:=\sup_{x\in \mathbb{R}}|x^{m}f^{(n)}(x)|$$
Let $1<R\in \mathbb{R}$ be given. Estimate $$\begin{align*}
\int_{0}^{R}|f(x)|\ dx&= \underbrace{\int_{0}^{1}|f(x)|\ dx}_{:=C\in \mathbb{R}}+\int_{0}^{R}|f(x)|\ dx\\
&= C+\int_{1}^{R} \frac{1}{x^{2}}\underbrace{|x^{2}f(x)|}_{\le C_{2,0}}\ dx\\
&\le C+ C_{2,0}\int_{0}^{R} \frac{1}{x^{2}}\ dx\\
&= C+C_{2,0} \left(\frac{-1}{x}\bigg|_{1}^{R}\right)\\
&= C+ C_{2,0}\left(1- \frac{1}{R}\right)
\end{align*}$$
Thus, $$\lim_{R\rightarrow \infty}\int_{0}^{R}|f(x)|\ dx\le\sup_{R>1}\left(C+C_{2,0}\left(1- \frac{1}{R}\right)\right)= C+C_{2,0}<\infty$$
Let $1<R\in \mathbb{R}$ be given. Estimate
$$\begin{align*}
\int_{-R}^{0}|f(x)|\ dx&= \int_{-R}^{-1}|f(x)|\ dx+\underbrace{\int_{-1}^{0}|f(x)\ dx}_{:=C\in \mathbb{R}}\\
&= \int_{-R}^{-1}  \frac{1}{x^{2}}\underbrace{|x^{2}f(x)|}_{\le C_{2,0}}\ dx+C\\
&\le C_{2,0}\int_{-R}^{-1} \frac{1}{x^{2}}\ dx + C\\
&= C_{2,0} \left(-\frac{1}{x}\bigg|_{-R}^{-1}\right)+C\\
&= C_{2,0} \left(1- \frac{1}{R}\right)+C
\end{align*}$$
Thus, 
$$\lim_{R\rightarrow \infty}\int_{-R}^{0}|f(x)|\ dx\le\sup_{R>1} \left(C+C_{2,0}\left(1-\frac{1}{R}\right)\right)= C+C_{2,0}<\infty$$
We have shown that both of the improper Riemann integrals of $|f|$ exist. So, $f\in\mathcal{L}^{1}$. 

>[!2]


(b)



(c)

Let $0<\phi\in\mathcal{L}^{1}\cap\mathcal{C}^{k}(\mathbb{R};\mathbb{C})$ satisfy $$\int_{-\infty}^{\infty}\phi(x)\ dx=1$$
Note that $\phi$ real valued and non-negative implies $|\phi|=\phi$.

$\mathbb{R}AI-1$: $$\begin{align*}
\int_{-\infty}^{\infty}\phi_{\epsilon}(x)\ dx&= \int_{-\infty}^{\infty} \frac{1}{\epsilon}\phi\left( \frac{1}{\epsilon}x\right)\ dx\\
&= \int_{-\infty}^{\infty}\phi(t)\ dt\quad(\text{change variables }t= \frac{x}{\epsilon})\\
&= 1
\end{align*}$$
$\mathbb{R}AI-2$: Since $|\phi|=\phi$, $$\phi_{\epsilon}(x)=\frac{1}{\epsilon}\phi\left( \frac{1}{\epsilon}x\right)=\left| \frac{1}{\epsilon}\phi\left( \frac{1}{\epsilon}x\right)\right|=\left|\phi_{\epsilon}\right|$$Thus, $\mathbb{R}AI-2$ follows from $\mathbb{R}AI-1$ by Remark 9.10 (2) of [CM].

$\mathbb{R}AI-3$: Since $\phi\in\mathcal{L}^{1}$, pick $R>0$ such that $$\int_{\mathbb{R}\setminus(-R,R)}\phi(x)\ dx<\epsilon$$
If $\epsilon<1$, we have 
$$\begin{align*}
\int_{\mathbb{R}\setminus(-R,R)}\phi_{\epsilon}(x)\ dx&= \int_{-\infty}^{-R} \frac{1}{\epsilon}\phi\left( \frac{1}{\epsilon}x\right)dx+\int_{R}^{\infty} \frac{1}{\epsilon}\phi\left( \frac{1}{\epsilon}x\right)\ dx\\
&= \int_{-\infty}^{- \frac{R}{\epsilon}}\phi(t)\ dt+\int_{\frac{R}{\epsilon}}^{\infty}\phi(t)\ dt\quad(\text{change variables }t= \frac{x}{\epsilon})\\
&\le \int_{-\infty}^{R}\phi(t)\ dt+\int_{R}^{\infty}\phi(t)\ dt%\label{c}
\\
&= \int_{\mathbb{R}\setminus(-R,R)}\phi(t)\ dt\\
&< \epsilon
\end{align*}$$
where the monotonicity of the integrals in (\ref{c}) holds for the non-negative real-valued function $\phi$.

(d)
Find $f\in\mathcal{L}^{1}$ with $f^{2}\notin\mathcal{L}^{1}$. 


Define $f:\mathbb{R}\rightarrow \mathbb{R}$:

$$\begin{equation} %\label{f}
f(x):=\begin{cases}
 \sqrt{n} & x\in \left[n,n+ \frac{1}{n^ 2}\right]\text{ for some }n\in \mathbb{N}_{0} \\
0 & \text{otherwise}
\end{cases}
\end{equation}$$
Note that the $n$ in (\ref{f}) is unique for each $x$. We see $$\int_{-\infty}^{0}f(x)\ dx=0$$
For $n\in \mathbb{N}$, we see, $$\int_{0}^{n}f(x)\ dx= \sum_{k=0}^{n-1} \frac{\sqrt{k}}{k^{2}}=\sum_{k=0}^{n-1} \frac{1}{k^{\frac{3}{2}}}$$which converges as $n \rightarrow \infty$, since it is a $p$ series with $p>1$. Thus, $|f|=f$ has convergent improper Riemann integrals and $f\in\mathcal{L}^{1}$

However, for $n\in \mathbb{N}$, $$\int_{0}^{n}(f(x))^{2}\ dx=\sum_{k=0}^{n-1} \frac{k}{k^{2}}=\sum_{k=0}^{n-1} \frac{1}{k}$$which diverges as $n \rightarrow \infty$, since it is the harmonic series. Thus, $f^{2}\notin\mathcal{L}^{1}$. 




>[!3]

OPTIONAL - (a) This is a simple application of the [[Irrationality of Logs]].

(b)

For the mean-tone temperament, $g_{\alpha}= \frac{7}{12}$, so 
$$\begin{align*}
&g_{\alpha}= g-\alpha \epsilon_{s}\\
&\iff \alpha= \frac{g-g_{\alpha}}{\epsilon_{s}}= \frac{g-7/12}{\epsilon_{s}}\\
\end{align*}$$
Compute the first couple continued fraction approximants:
$$\begin{align*}
\alpha&= .09090368\ldots\\
a_{0}&= \lfloor \alpha\rfloor= 0\\
x_{1}&= \frac{1}{\alpha-a_{0}}=11.0006548\ldots\\
a_{1}&= \lfloor x_{1}\rfloor=11\\
\alpha_{1}&= a_{0}+ \frac{1}{a_{1}}= \frac{1}{11}\\
r_{1}&= x_{1}-a_{1}=.00065477\ldots\\
x_{2}&= \frac{1}{r_{1}}=1527.25201\ldots\\
a_{2}&= \lfloor x_{2}\rfloor =1527\\
\alpha_{2}&= a_{0}+ \frac{1}{a_{1}+\frac{1}{a_{2}}}= \frac{1527}{16798} 
\end{align*}$$
The first continued fraction approximant $\frac{1}{11}$ is a very good approximant because of the huge jump in denominators from $11$ to $16798$. Also, a scale of 16798 tones would be impractical.
