---
tag: set theory
mathLink: intersection under inverse image lemma
---
```ad-prop
The [[Set Theory/Intersection|Intersection]] behaves nicely under the [[Set Theory/Preimage|Preimage]]:
$$f^{-1}\left(\bigcap_{\lambda\in\Lambda}U_\lambda\right)=\bigcap_{\lambda\in\Lambda}f^{-1}(U_\lambda)$$
```

```ad-proof
Let $x\in f^{-1}(\bigcup_{\lambda\in\Lambda}U_\lambda)$ be given.
Then, pick $\lambda\in\Lambda$ with $f(x)\in U_\lambda$. $x\in f^{-1}(U_\lambda)$, so $x\in \bigcup_{\lambda\in\Lambda}f^{-1}(U_\lambda)$. 
[[therefore]] $f^{-1}(\bigcup_{\lambda\in\Lambda}U_\lambda)$ [[Notation/subset|subset]] $\bigcup_{\lambda\in\Lambda}f^{-1}(U_\lambda)$
Let $x\in\bigcup_{\lambda\in\Lambda}f^{-1}(U_\lambda)$ be given.
Then, pick $\lambda\in\Lambda$ with $x\in f^{-1}(U_\lambda)$ . $f(x)\in\bigcup_{\lambda\in\Lambda}U_\lambda$, so $x\in f^{-1}\left(\bigcup_{\lambda\in\Lambda}U_\lambda\right)$.
[[therefore]] $\bigcup_{\lambda\in\Lambda}f^{-1}(U_\lambda)$ [[Notation/subset|subset]] $f^{-1}\left(\bigcup_{\lambda\in\Lambda}U_\lambda\right)$.
```
