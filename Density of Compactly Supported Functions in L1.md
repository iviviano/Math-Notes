

>[!prop]
Let $f$ be an [[L1 Function]], then for each $\epsilon>0$, there exists $g\in\mathcal{C}_{c}^{\infty}(\mathbb{R};\mathbb{C})$ such that $$\|f-g\|_{\mathcal{L}^{1}}<\epsilon$$

>[!prop] Corollary
If $f\in\mathcal{L}^{1}$, then $\widehat f$ is [[Continuous]].

>[!proof]
Note that $\widehat f$ is [[Continuous]] if $f\in\mathcal{C}_{c}^{\infty}$. Since this is a [[Subset]] of the [[Schwartz Function]] [[Function]]s and the [[The Fourier Map is a Linear Operator on the Class of Schwartz Functions]], $\widehat f\in\mathcal{S}(\mathbb{R})$. Since [[Schwartz Function]] functions are continuous, $\widehat f$ is continuous.
>
Extend to any [[L1 Function]] $f\in\mathcal{L}^{1}$:
Let $g\in\mathcal{C}^{\infty}_{c}(\mathbb{R};\mathbb{C})$ such that $$\|f-g\|_{\mathcal{L}^{1}}<\epsilon$$
Fix a [[Frequency]] $\nu_{0}$.
>$$\begin{align*}
|\hat f(\nu)-\hat f(\nu_{0})|&\le |\hat f(\nu)-\hat f(\nu)|+|\hat g(\nu)-\hat g(\nu_{0})|+|\hat g(\nu)-\hat f(\nu_{0})|\\
&= |\widehat{f-g}(\nu)|+|\hat g(\nu)-\hat g(\nu_{0})|+|\widehat{g-f}(\nu_{0})|\\
&\le 3\epsilon
\end{align*}$$
where the first and third term are small by the [[Fourier Transform Bound]] and the smallness of the the distance between $f,g$ in $\mathcal{L}^{1}$. The second term is small since $\hat g$ is [[Continuous]].

>[!prop] Corollary
If $f\in\mathcal{L}^{1}$, then $$\lim_{\nu \rightarrow \pm \infty}\widehat f(\nu)=0$$In other words, this is the [[Riemann-Lebesgue Lemma for the Fourier Transform]]. 

>[!proof]
For $\epsilon>0$, take $g$ as before. 
>$$\begin{align*}
|\hat f(\nu)|&\le |\hat f(\nu)-\hat g(\nu)|+|\hat g(\nu)|\\
&= |\widehat{f-g}(\nu)|+|\widehat g(\nu)|
\end{align*}$$
The first term is bounded by the $\mathcal{L}^{1}$ norm and $\hat g$ is a [[Schwartz Function]] [[Function]].
