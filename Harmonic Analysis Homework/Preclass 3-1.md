>[!Q1]
Let $(V,\|.\|)$ be a [[Banach Space]], and let $v_{n}$ be a [[Norm Summable]]e [[Sequence]]. Let $$\begin{align*}
a_{n}&= \sum_{i=1}^{n}\|v_{i}\|\\
s_{n}& =\sum_{i=1}^{n}v_{n}
\end{align*}$$Let $\epsilon>0$ be given and pick $N$ such that for all $n,m\ge N$, $$|a_{n}-a_{m}|<\epsilon$$For $n>m\ge N$, $$\begin{align*}
\|s_{n}-s_{m}\|&= \left\|\sum_{i=1}^{n}v_{i}-\sum_{i=1}^{m}v_{i}\right\|\\
&= \left\|\sum_{i=m+1}^{n}v_{i}\right\|\\
&\le \sum_{i=m+1}^{n}\|v_{i}\|\\
&= \sum_{i=1}^{n}\|v_{i}\|-\sum_{i=1}^{m}\|v_{i}\|\\
&= a_{n}-a_{m}\\
&\le |a_{n}-a_{m}|\\
&< \epsilon
\end{align*}$$Therefore, the sequence of partial sums $s_n$ is [[Cauchy Sequence]] in $(V,\|.\|)$. Since $(V,\|.\|)$ is [[Complete]], this sequence [[Converges (series)]]s and is [[Summable]]e.


>[!Q2]
Let $v_{n}$ be a [[Cauchy Sequence]] [[Sequence]] in $(V,\|.\|)$. Let $\epsilon>0$ be given. Pick $n_{0}\in N$ such that for all $n>m\ge n_{0}$, $$\|v_{n}-v_{m}\|<\epsilon$$For each $k\in \mathbb{N}$ starting at $k=1$, Pick $n_{k}=n_{k}(\epsilon)>n_{k-1}$ such that for all $n>m\ge n_{k}$, $$\|v_{n}-v_{m}\|< \frac{\epsilon}{2^{k}}$$In particular, for all $k\in \mathbb{N}$, $n_{k+1}>n_{k}\ge n_{k}$, so $$\|v_{n_{k+1}}-v_{n_{k}}\|< \frac{\epsilon}{2^{k}}$$
