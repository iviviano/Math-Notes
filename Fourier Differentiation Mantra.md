---
mathLink: Fourier differentiation mantra
---
>[!thm]
>Let $f\in\mathcal{C}_{1}^{k}(\mathbb{R};\mathbb{C})$, for some $k\in \mathbb{N}$. Then, 
>1. For all $1\le j\le k$, the [[Fourier Coefficient]]s of the $j$-th [[Derivative]] of $f$ satisfy $$\widehat{[f^{(j)}]}_{n}=(2\pi in)^{j}\cdot\hat{f}_{n}$$for each $n\in\mathbb{Z}$
>2. The [[Fourier Coefficient]]s of $f$ decay with the bound $$|\hat{f}_{n}|\le \frac{\|f^{(k)}\|_{1}}{(2\pi)^{k}}|n|^{-k}$$

>[!thm]
Given $k\in \mathbb{N}$, suppose $f\in\mathcal{C}^{k}_{\infty}(\mathbb{R};\mathbb{C})\cap\mathcal{L}^{1}$ satisfies $$f^{(j)}\in\mathcal{L}^{1}\text{ and }\lim_{t \rightarrow \pm\infty}f^{(j)}(t)=0\text{, for all }1\le j\le k$$
Then, 
>1. For all $1\le j\le k$, the [[Fourier Transform]] of the $j$-th derivative of $f$ satisfies $$\widehat{[f^{(j)}]}(\nu)= (2\pi i \nu)^{j}\cdot\widehat f(\nu)$$
>2. The [[Fourier Transform]] decays with the bound $$\left|\widehat f(\nu)\right|\le \frac{\|f^{(k)}\|_{\mathcal{L}^{1}}}{(2\pi)^{k}}\left|\nu\right|^{-k}$$
