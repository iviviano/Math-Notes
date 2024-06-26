Given a [[Ordinary Differential Equation]]: $$y'=f(y)$$and initial condition $y(0)=y_{0}$. We can approximate the solution to the IVP $y(t)$.

The following algorithm generates an approximate solution $u$
1. Choose a step $\Delta t$ and set $t_{n}=n \Delta t,n=0,1,2,\ldots$
2. Let $u_{0}=y_{0}$
3. $u_{n+1}=u_{n}+\Delta t f(t_{n})$

This is justified by the [[Mean Value Theorem]]: $$\frac{u_{n+1}+u_{n}}{\Delta t}=f(u_{n})$$
j