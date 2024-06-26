Let $u_{j}^{n}$ be a discretization of a differential equation where $j$ represents the spatial index and $n$ represents the temporal index: $$\begin{align*}
x&= jh,\quad j=0,1,\ldots\\
t&= nt,\quad n=0,1,\ldots\\
\end{align*}$$
Define $$\|u^{n}\|:=\max_{j}|u_{j}^{n}|$$
>[!def]
>The difference scheme is *stable* if $$\|u^{n}\|_{\infty}≤\|u^{0}\|_{\infty}$$for all $n≥1$ and all $u^{0}$.

