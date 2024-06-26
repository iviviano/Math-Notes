---
tag: topology
mathLink: closure of connected sets proposition
---
>[!prop]
>Let $X$ be a [[Topological Space]]. Let $C\subseteq X$ be [[Connected]] and $C\subseteq Y\subseteq \text{cl }C\subseteq X$, then $Y$ is [[Connected]].

>[!proof]
Let $A\subseteq Y$ that is nonempty, relatively [[Open Set]] and relatively [[Closed Set]]. Then there is a [[Neighborhood]] $U$ in $X$ such that $A=U\cap Y$. Let $x_{0}\in A$. Then, $x_{0}\in \text{cl }C$ and $x_{0}\in U$. So $U\cap C= A\cap C$ is nonempty. So, $A\cap C$ is a nonempty relatively [[Open Set]] [[Subset]] of $C$. Similarly, $A$ is relatively [[Closed Set]] in $Y$. Hence $A\cap C$ is relatively [[Closed Set]] in $C$. Since $C$ is [[Connected]], $C=A\cap C\subseteq A$. So, $C\subseteq Y\subseteq \text{cl }C$. Thus, $A$ is [[Closed Set]] in $Y$ and [[Dense]] in $Y$, so $A=Y$.