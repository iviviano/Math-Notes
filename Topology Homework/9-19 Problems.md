From 1.3: 12, 13

>[!note] 12
Let $(X,d_{X}),(Y,d_{Y}),(Z,d_{Z})$ be [[Metric Space]]s. Let $f:X \rightarrow Y,g:Y \rightarrow Z$ be [[Uniform Continuity]] [[Function]]s. Let $\epsilon>0$ be given. Pick $\delta_{1}>0$ such that for all $y_{0}\in Y$, $$y\in B_{d_{Y}}(y,\delta_{1})\implies g(y)\in B_{d_{Z}}(g(y_{0}),g(y))$$Now pick $\delta_{0}$ such that for all $x_{0}\in X$,$$x\in B_{d_{X}}(x_{0},\delta_{0})\implies f(x)\in B_{d_{X}}(f(x_{0},f(x)))$$Then, for all $x_{0}\in X$, $$x\in B_{d_{X}}(x_{0},\delta_{0})\implies g\circ f(x)\in B_{d_{Z}}(g\circ f(x_{0}),\epsilon)$$so, $g\circ f:X \rightarrow Z$ is [[Uniform Continuity]].

>[!note] 13


[[Urysohn's Lemma]]


Need to find an infinite set of functions such that no element can be written as a linear combination of the others. Infinite set of functions comes from [[Urysohn's Lemma]].
Suppose $X$ is infinite. Then for each $x,y\in X$, 


Maybe the [[Function]]s given by [[Urysohn's Lemma]] are a basis for the [[Vector Space]]? If so, then just show there are only finitely many such functions? 
Suppose $X$ is finite. 
