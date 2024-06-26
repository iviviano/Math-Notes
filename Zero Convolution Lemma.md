---
mathLink: zero convolution lemma
---
>[!prop] Lemma
>Given $g\in\mathcal{C}_1$, suppose $$g\star f=0,\forall f\in\mathcal{C}_1$$then, $g$ is identically 0

>[!note]
>How many functions $f\in \mathcal{C}_1$ do we need? Using [[Fourier Coefficient]]s, we need $$g\star e_{n}=0$$for all $n\in \mathbb{Z}$.

>[!proof]
Let $$\phi_{n}=\begin{cases}n- \frac{t}{n} & \text{if }t\in[0, \frac{1}{n}] \\
n+\frac{1}{n} & \text{if }t\in[\frac{-1}{n},0] \\
0 & \text{if }t\notin[\frac{-1}{n}, \frac{1}{n}]\end{cases}$$ Note that it is trivial to show that $\phi_{n}$ is a [[Periodic Approximate Identity]]. And, $\phi_{n}\in\mathcal{C}_{1}$ for all $n$, so $$g\star \phi_{n}=0$$for all $n$ and $$0=g\star \phi_{n}\rightarrow g$$uniformly. Therefore, $g\equiv 0$. 
