>[!note] Q1
>$$\begin{align*}
\| v\|-\|w\|&= \|(v-w)+w\|-\|w\|\\
&\le \|v-w\|+\|w\|-\|w\|\\
&= \|v-w\|
\end{align*}$$
Therefore, $$\begin{align*}
\|\ \|v\|-\|w\|\ \|&\le \|\ \|v-w\|\ \|\\
&= \|v-\ w\|
\end{align*}$$

>[!note] 2
>- [[N1]]: For $v\in\mathcal{B}(S,\mathbb{C})$, if $$\|v\|_{\infty}=0$$then, $$\begin{align*}
\sup_{x\in S}|v(x)|=0
\end{align*}$$so, for $x\in S$, $$|v(x)|≤0$$Since $|.|$ is non-negative, we have for all $x\in S$, $$|v(x)|=0\implies v(x)=0$$by the positive definiteness of $|.|$, showing $v=0$. If $v=0,$ $$\begin{align*}
\|v\|_{\infty}&= \sup_{x\in S}|v(x)|\\
&= \sup_{x\in S}|0|\\
&= \sup_{x\in S}0\\
&= 0
\end{align*}$$
>- [[N2]]: Let $\lambda\in \mathbb{C}$ and $v\in\mathcal{B}(S;\mathbb{C})$. $$\begin{align*}
\|\lambda v\|_{\infty}&= \sup_{x\in S}|\lambda v(x)|\\
&= \sup_{x\in S}|\lambda|\cdot|v(x)|\\
&= |\lambda|\sup_{x\in S}|v(x)|\\
&= |\lambda|\cdot\|v(x)\|_{\infty}
\end{align*}$$
>- [[N3]]: Let $v,w\in\mathcal{B}(S;\mathbb{C})$. $$\begin{align*}
\|v+w\|_{\infty}&= \sup_{x\in S}|v(x)+w(x)|\\
&\le \sup_{x\in S}(|v(x)|+|w(x)|)\\
&\le \sup_{x\in S}|v(x)|+\sup_{x\in S}|w(x)|\\
&= \|v\|_{\infty}+\|w\|_{\infty}
\end{align*}$$

>[!Q3]
Since $\Re \text{e}(f_{n})=f_{n}$, I graphed $f_{n}:\mathbb{R}\rightarrow \mathbb{R}$ in $\mathbb{R}^2$: ![[Long image 2024-02-23 10.31.17.jpg]]
