The triangle function:

![[Screenshot 2024-06-11 at 10.55.33 AM.png | 400]] 

For the Dirichlet Boundary Condition, we take the 2-periodic odd extension. The sine [[Fourier Coefficient]]s are given by
$$A_{n}= \frac{4}{\pi^{2}n^{2}}\left(\sin\left(\pi \frac{n}{2}\right)-\sin\left(3\pi \frac{n}{2}\right)\right)$$
giving the time-dependent solution:
$$u(x,t)=\sum_{n=1}^{\infty}A_{n}e^{^{- n^{2}\pi^{2}Dt}\sin(n \pi x)}$$


For the Neumann Boundary Condition, we take the 2-periodic even extension. The cosine [[Fourier Coefficient]]s are given by $$B_{n}=\begin{cases}
\frac{1}{2} & n=0 \\
- \frac{4}{n^{2}\pi^{2}}\left(1+(-1)^{n}-2\cos\left(n \frac{\pi}{2}\right)\right) & n>0 \\
\end{cases}$$
giving the time-dependent solution: $$u(x,t)=\sum_{n=0}^{\infty}B_{n}e^{\pi^{2}n^{2}Dt}\cos(n \pi x)$$

For the Periodic Boundary Condition, we take the 1-periodic extension (which happens to be an even function). Its cosine [[Fourier Coefficient]]s are given by $$
B_{n}=\begin{cases}
\frac{1}{2} & n=0 \\
\frac{2}{\pi^{2}n^{2}}((-1)^{n}-1) & n>0
\end{cases}$$
giving the time-dependent solution: $$u(x,t)=\sum_{n=0}^{\infty}B_{n}e^{4\pi^{2}n^{2}Dt}\cos(2\pi nx)$$

