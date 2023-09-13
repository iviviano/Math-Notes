---
mathLink: components are clopen in locally connected spaces
tag: topology
---
>[!prop]
>If $X$ is [[Locally Connected]], then every [[Component]] is both [[Closed Set]] and [[Open Set]].

>[!proof]
In general, components are closed. Suppose $X$ is [[Locally Connected]]. Let $C$ be a [[Component]] of $X$. Let $x\in C$. Let $U$ be a [[Connected]] [[Neighborhood]] of $X$. Then, $U\cup C$ is [[Connected]] as [[Unions of Overlapping Connected Sets are Connected]] and $x\in U\cap C$. As $U\subseteq U\cup C$ and $U\not\subset U\cup C$ ($U$ is a [[Maximal]] [[Connected]] [[Set]]), $U\subseteq C$. So there is an [[Open Set]] [[Set]] containing $x$ contained in $C$, so $C$ is [[Open Set]].
