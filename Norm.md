---
tag: set theory
mathLink: norm
---
> [!def]
> Given $\boldsymbol{x}\in \mathbb{R}^n$, we define the *norm* of $\boldsymbol{x}$:
> $||\boldsymbol{x}||=(x_1^2 + \cdots + x_n^2)^{\frac{1}{2}}$

>[!def]
Given a $\mathbb{C}$-valued [[Vector Space]] $V$, a *norm* on $V$ is a map $$\|.\|:V \rightarrow [0,\infty)$$which assigns to each vector $v\in V$, a non=negative number $\|v\|$ such that the following three properties hold: 
>1. [[N1]] Positive Definiteness: For $v\in V$, one has $$\|v\|=0\iff v=0$$
>2. [[N2]] Positive Homogeneity: For all $v\in V$ and $\lambda\in \mathbb{C}$, one has $$\|\lambda v\|=|\lambda|\ \|v||$$
>3. [[N3]] [[Triangle Inequality]]: For all $v,w\in V$, one has $$\|v+w\|\le\|v\|+\|w\|$$

