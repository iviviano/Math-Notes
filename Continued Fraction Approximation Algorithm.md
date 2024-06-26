>[!def]
>The *continued fraction approximation algorithm* is defined recursively. In the following, $\lfloor a\rfloor$ refers to the [[Integer Part]] of $a$.
Let $\alpha\in \mathbb{R}-\mathbb{Q}$.

>[!todo]
Initial step to restrict to $(0,1)$.
Let $$\alpha_{0}=a_{0}=\lfloor \alpha\rfloor$$
Base step:
Let $$x_{1}:= \frac{1}{\alpha-a_{0}}>1$$This gives: $$\alpha=a_{0}+ \frac{1}{x_{1}}$$Set $$a_{1}:=\lfloor x_{1}\rfloor$$and approximate $\alpha$ by replacing $x_{1}$ with $a_{1}$: $$\alpha_{1}:= a_{0}+ \frac{1}{a_{1}}$$compute the first remainder: $$r_{1}:=x_{1}-a_{1}$$
Recursive step: Let$$x_{n}:= \frac{1}{r_{n}}>1$$This gives: $$\alpha=a_{0}+\frac{1}{a_{1}+\frac{1}{a_{2}+\cdots\frac{1}{a_{n-1}+\frac{1}{a_{n}+\frac{1}{x_{n+1}}}}}}$$Set $$a_{n+1}:=\lfloor x_{n+1}\rfloor$$and obtain the $(n+1)$-st [[Continued Fraction Approximant]] by replacing $x_{n+1}$ by $a_{n+1}$: $$
\alpha_{n+1}:=a_{0}+\frac{1}{a_{1}+\frac{1}{a_{2}+\cdots\frac{1}{a_{n-1}+\frac{1}{a_{n}+\frac{1}{a_{n+1}}}}}}
$$Compute the $(n+1)$-st remainder: $$r_{n+1}:=x_{n+1}-a_{n+1}$$for the next iteration.
