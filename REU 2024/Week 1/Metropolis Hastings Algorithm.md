This is a [[Markov Chain Monte Carlo]] algorithm for sampling from a probability distribution $P(x)$ given a function $f(x)$ with $$f\propto P$$
Let $g(x~|~y)$ be the [[Gaussian]] centered at $y$. This is our proposal function which generates possible transitions in the chain.

Algorithm:
1. Choose an arbitrary point $x_{t}$ to be the initial observation
2. For each iteration $t$:
	1. Propose a candidate $x'$ for the next sample by sampling $g(x'~|~x_{t})$
	2. Calculate the acceptance ratio $$\alpha= \frac{f(x')}{f(x_{t})}$$
	3. Generate a uniform random variable $u\in[0,1]$. If $\alpha<u$, accept by setting $x_{t+1}=x'$. Otherwise, reject by setting $x_{t+1}=x_{t}$

>[!note]
>This version of the algorithm requires the proposal function to be symmetric: 
>$$g(x~|~y)=g(y~|~x)$$

>[!note]
>For a multivariate distribution, the Gibbs sampler may perform better do to lower rejection rates.