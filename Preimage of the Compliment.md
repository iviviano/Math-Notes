---
tag: set theory
mathLink: preimage of the compliment proposition
---
>[!prop]
Let $f:X \rightarrow Y$. Let $A\subseteq Y$. Then, $$f^{-1}(Y-A)=X-f^{-1}(A)$$

>[!proof]
Let $x\in f^{-1}(Y-A)$. Then, $f(x)\in Y-A$, so $f(x)\notin Y-A$. As $x\in X$, $$f^{-1}(Y-A)\subseteq X-f^{-1}(A)$$Let $x\in X-f^{-1}(A)$. Then, $$f(x)\in f(X-f^{-1}(A))\subseteq f(X)-f(f^{-1}(A))\subseteq Y-A$$So, $f(x)\in Y-A$, so $x\in f^{-1}(Y-A)$. $$\therefore f^{-1}(X-A)=X-f^{-1}(A)$$


