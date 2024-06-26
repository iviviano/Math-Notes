---
mathLink: triangle inequality for complex integrals theorem
---
>[!thm]
>Let $f:[a,b]\rightarrow \mathbb{C}$ be a [[Complex-Valued Function]], [[Riemann Integrable]] [[Function]]. Then, 
>1. $|f|\in\mathcal{R}([a,b];\mathbb{R})$
>2. The [[Triangle Inequality]]: $$\left|\int_{a}^{b}f(t)dt\right|≤\int_{a}^{b}|f(t)|dt$$

>[!note]
>If $f:[a,b]\rightarrow \mathbb{C}$ is [[Continuous]], then $|f|\in\mathcal{C}([a,b];\mathbb{R})$

>[!proof] Proof of special case where $f$ is [[Continuous]] via polarization
Let $$I=\int_{a}^{b}f(t)dt=|I|\cdot e^{i\theta}$$for some fixed $\theta\in[0,2\pi)$. Then, $$\begin{align}|I|&=e^{-i\theta}\cdot I=\Re \text{e}\left(e^{-i\theta}\int_{a}^{b}f(t)dt\right)=\Re \text{e}\left(\int_{a}^{b}(e^{-i\theta}f(t))dt\right)\\
&=\int_{a}^{b}\Re \text{e}(e^{-i\theta}f(t))dt\le\int_{a}^{b}|\Re \text{e}(e^{-i\theta}f(t))|dt\quad(\text{Triangle inequality of }\mathbb{R})\\
&\le \int_{a}^{b}|e^{-i\theta}f(t)|dt=\int_{a}^{b}|e^{-i\theta}||f(t)|dt\\
&=\int_{a}^{b}|f(t)|dt\end{align}$$