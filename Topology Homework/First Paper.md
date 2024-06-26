
<h1 align=center> Introduction </h1>

<h1 align=center> Exterior Algebra </h1>
Definitions:
- [[P-Tensor]]
- [[tensor product]]
- [[alternating tensor]] [[P-Tensor]] and how to [[Make a Tensor Alternating]]
- [[wedge product]]
- [[Pullback]]s and alternating tensors under pullbacks
- might need anticommutativity of wedge products

I will begin by establishing the exterior algebra in full generality, before returning to apply it to integration. First, here are some definitions from linear algebra. Let $V$ be a vector space. For convenience, use $\mathbb{R}$ as its field of scalars. A *functional* on $V$ is a linear map $F:V \rightarrow \mathbb{R}$. The *dual space* of $V$ is the vector space of all linear functionals on $V$. The dual space will be denoted $V^{*}$. Each of these definitions has higher dimensional generalizations that will be essential to the theory of integration. A *$p$-tensor* on $V$ is a multilinear real valued function on $V^{p}$. Multilinear functions are linear in each variable separately. Formally, if $T:V^{p}\rightarrow \mathbb{R}$ is a $p$-tensor, $$T(v_{1},\ldots,u_{i}+av_{i},\ldots,v_{p})=(FORMAT)T(v_{1},\ldots,u_{i},\ldots,v_{p})+aT(v_{1},\ldots,v_{i},\ldots,v_{p})$$for all $v_{1},\ldots,v_{k},u_{i}\in V,a\in \mathbb{R}$. For convenience, define $0$-tensors as constant real numbers.

Multiplication of tensors is defined with the *tensor product*. If $T$ is a $p$-tensor and $S$ is a $k$-tensor, their tensor product is given by $$T\otimes S(v_{1},\ldots,v_{p},v_{p+1},\ldots,v_{p+k})=T(v_{1},\ldots,v_{p})\cdot S(v_{p+1},\ldots,v_{p+k})$$defines a $p+k$ tensor on $S$.

Let $S_{p}$ denote the [[Symmetric Group of Degree n]] $p$. A permutation $\pi\in S_{p}$ is said to be [[Odd Permutation]] (even) if it can be expressed as with an odd (even) number of simple transpositions: $$v_{1},\ldots,v_{i},\ldots,v_{j},\ldots,v_{p}\rightarrow v_{1},\ldots,v_{j},\ldots,v_{i},\ldots,v_{p}(format)$$of the identity permutation. Clearly, $\pi$ must be odd or even. Now, let $(-1)^\pi=1$ if $\pi$ is even and $-1$ if $\pi$ is odd. Given the $p$-tensor $T$ on $V$, define a new $p-$tensor $T^\pi$ by $$\begin{equation}
T^{\pi}(v_{1},\ldots,v_{p})=T(v_{\pi(1)},\ldots,v_{\pi(p)})
\end{equation}$$for $v_{1},\ldots,v_{p}\in V$. A $p$-tensor $T$ on $V$ is said to *alternate* if for every $v_{1},\ldots,v_{p}\in V$ and $\pi\in S_{p}$, $$T^{\pi}(v_{1},\ldots,v_{p})=(-1)^{\pi}T(v_{1},\ldots,v_{p})$$

Not all tensors on a vector space $V$ alternate. Given a $p$-tensor $T$ on $V$, define $$\begin{equation}
\text{Alt }T=\frac{1}{p!}\sum_{\pi\in S_{p}}(-1)^{\pi}T^{\pi}
\end{equation}$$If $T$ is already alternating, then $$\text{Alt }T= \frac{1}{p!}\sum_{\pi\in S_{p}}(-1)^{\pi}T^{\pi}= \frac{1}{p!}\sum(-1)^{\pi}(-1)^{\pi}T=\frac{1}{p!}\sum_{\pi\in S_{p}}T=T$$as the order of $S_{p}$ is $p!$. Generally, $\text{Alt }T$ is alternating for any tensor $T$: if $\sigma\in S_{p}$, $$(\text{Alt }T)^{\sigma}=\left(\frac{1}{p!}\sum_{\pi\in S_{p}}(-1)^{\pi}T^{\pi}\right)^{\sigma}=\frac{1}{p!}\sum_{\pi\in S_{p}}(-1)^{\pi}T^{\sigma\circ\pi}$$as $(T^\pi)^\sigma=T^{\sigma\circ\pi}$. Clearly, $(-1)^{\sigma\circ \pi}=(-1)^{\sigma}(-1)^{\pi}$, so $$(\text{Alt }T)^{\sigma}=\frac{1}{p!}\sum_{\pi\in S_{p}}\frac{(-1)^\sigma(-1)^\pi}{(-1)^{\sigma}}T^{\sigma\circ\pi}=\frac{(-1)^{\sigma}}{p!}\sum_{\pi\in S_{p}}(-1)^{\sigma\circ\pi}T^{\sigma\circ\pi}$$Let $\tau=\sigma\circ\pi$ for each $\pi\in S_{p}$. Since $S_{p}$ is a [[Group]] and $\pi$ ranges through $S_{p}$, so does $\tau$. This allows us to rewrite $$(\text{Alt }T)^{\sigma}=(-1)^{\sigma} \frac{1}{p!}\sum_{\tau\in S_{p}}(-1)^{\tau}T^{\tau}=(-1)^{\sigma}\text{Alt }T$$proving that $\text{Alt }T$ is alternating.

The tensor product of two alternating tensors does not necessarily alternate. Obviously, all $1$-tensors alternate as the only permutation in $S_1$ is the identity. However, not all tensor products of $1$-tensors alternate. This motivates the *wedge product*. For two tensors $T$ and $S$ on $V$, their wedge product is defined as $$T\land S=\text{Alt }(T\otimes S)$$As sums and scalar multiples of alternating tensors still alternate, the collection of all alternating $p$-tensors on $V$ forms a vector space denoted $\Lambda^{p}(V^{*})$. 

>[!thm] Theorem 1
>Let $v_{1},\ldots,v_{k}$ be a [[Basis of a Vector Space]] of $V$ and let $\phi_{1},\ldots,\phi_{k}$ be the induced [[Dual Basis]] of $V^{*}$. Letting $\phi_{I}=\phi_{i_{1}}\land\cdots\land \phi_{i_{p}}$ for some sequence $I$, the [[Collection]] $$\{\phi_{I}:I=i_{1},\ldots,i_{p} \text{ and }i_{1}<\cdots<i_{p}\}$$of $p$-tensors on $V$ forms a [[Basis of a Vector Space]] of $\Lambda^{p}(V^{*})$.

Next, generalize the transpose. Let $A:V \rightarrow W$ be any linear map. $A^{*}:W^{*}\rightarrow V^{*}$ is the induced linear map between the dual spaces. Now, let $T$ be a $p$-tensor on $W$. Then, the *pullback* of $T$ by $A$ is the $p$-tensor on $V$ defined by $$\begin{equation}A^{*}T(v_{1},\ldots,v_{p})=T(Av_{1},\ldots,Av_{p})\end{equation}$$for $v_{1},\ldots,v_{p}\in V$. The pullback of a tensor has the following properties: $$\begin{align}
A^{*}(T+S)&=A^{*}T+A^{*}S\\
A^{*}(T\land S)&=A^{*}T\land A^{*}S\\
Any others?
\end{align}$$
Property NUMBER: $$\begin{align*}A^{*}(T+S)(v_{1},\ldots,v_{p})&=(T+S)(Av_{1},\ldots,Av_{p})\\&=T(Av_{1},\ldots Av_{p})+S(Av_{1},\ldots,Av_{p})\\&=(A^{*}T)(v_{1},\ldots,v_{p})+(A^{*}S)(v_{1},\ldots,v_{p})\end{align*}$$
Property NUMBER: $$\begin{align*}A^{*}(T\land S)(v_{1},\ldots,v_{p},v_{p+1},\ldots,v_{p+k})&=(T\land S)(Av_{1},\ldots,Av_{p},Av_{p+1},\ldots,Av_{p+k})\\
&=\text{Alt }(T\otimes S)()\\
&=\sum_{\pi\in S_{p+k}}(-1)^{\pi}(T\otimes S)(Av_{\pi(1)},\ldots,Av_{\pi(p+k)})\\
&=\sum_{\pi\in S_{p+k}}(-1)^{\pi}(A^{*}T\otimes A^{*}S)(v_{\pi(1)},\ldots,v_{\pi(p+k)})\\
&=\text{Alt }(A^{*}T\otimes A^{*}S)(v_{1},\ldots,v_{p},v_{p+1},\ldots,v_{p+k})\\
&=(A^{*}T\land A^{*}S)(v_{1},\ldots,v_{p},v_{p+1},\ldots,v_{p})\end{align*}$$

>[!thm]
>Let $A:V \rightarrow V$ be a linear isomorphism. Then, $$A^{*}T=(\text{det }A)T$$for all alternating $k$-tensors $T$ where $k=\text{dim }V$.

There is only one strictly increasing sequence $I$ of length $k$ (work on this). So, Thm 1 implies that all $k$-tensors on $V$ are some constant multiple of $\phi_{1}\land\cdots\land\phi_{k}$. Thm NUMBER makes precise how the pullback relates these tensors. For a full proof, see Guilleman and Pollack 159. An important consequence of Thm NUMBER and Eq NUMBER is the following relationship: $$\begin{equation}A^{*}\phi_{1}\land\cdots\land A^{*}\phi_{k}=A^{*}T=(\text{det }A)\ \phi_{1}\land\cdots\land \phi_{k}\end{equation}$$



<h1 align=center> Differential Forms </h1>

Let $X$ be a smooth manifold. A *$p$-form* $\omega$ on $X$ is a function that assigns to each point $x\in X$, an alternating $p$-tensor $\omega(x)$ on $T_{x}(X)$. Sums and scalar multiples of $p$-forms are defined point-wise: $$(a\omega_{1}+\omega_{2})(x)=a\cdot\omega_{1}(x)+\omega_{2}(w)$$Similarly, the wedge product for tensors may be extended to forms point-wise: $$(\omega_{1}\land \omega_{2})(x)=\omega_{1}(x)\land \omega_{2}(x)$$as wedge products of alternating tensors alternate. Clearly, a $0$-form is just a real-valued function on $X$, since each point in $X$ is mapped to a $0$-tensor, and $0$-tensors are just real numbers.

An important example of a $1$-form comes from should be familiar. Let $V\subseteq \mathbb{R}^k$ be open and $f:V \rightarrow \mathbb{R}$ be [[Smooth]]. Define the *differential* of $f$ to be the function $df$ mapping $x\mapsto df_{x}$.  As $T_{y}(\mathbb{R})=\mathbb{R}$ for all $y\in \mathbb{R}$, $df_{x}:T_{x}(V)\rightarrow \mathbb{R}$. Additionally, $df_{x}$ is alternating as it is as $1$-tensor. So, $df$ is a $1$-form on subsets of $\mathbb{R}^{k}$. Now consider the coordinate functions $x_{1},\ldots,x_{k}:\mathbb{R}^{k}\rightarrow \mathbb{R}$ on $\mathbb{R}^k$. Fix $z\in \mathbb{R}^{k}$ and let $a\in \mathbb{R}^{k}$. For each $i≤k$, $$dx_{i}(z)(a)=\lim_{h \rightarrow 0} \frac{x_{i}(z+ha)-x_{i}(z)}{h}=\lim_{h \rightarrow 0} \frac{z_{i}+ha_{i}-z_{i}}{h}=a_{i}$$So, $dx_{1}(z),\ldots,dx_{k}(z)$ are the dual basis for $T_{z}(\mathbb{R}^k)^{*}$. Applying Thm NUMBER, we get an extremely useful (reword) characterization of the forms on Euclidean space.

>[!prop]
>Let $U\subseteq \mathbb{R}^{k}$ be [[Open Set]]. Then any $p$-form $\omega$ on $U$ may be written uniquely as $$\omega=\sum_{I}f_{I}dx_{I}$$for increasing index sequences $I=i_{1}<\cdots<i_{p}$ and real-valued functions $f_{I}$ on $U$.

A form is said to be *smooth* if each coefficient $f_{I}$ of its expansion in Proposition NUMBER is a [[Smooth]] function.

We extend pullbacks of tensors to differential forms as well. If $f:X \rightarrow Y$ is a [[Smooth]] map and $\omega$ is a $p$-form on $Y$, we define a $p$-form on $X$ by $$f^{*}\omega(x)=(df_{x})^{*}\omega[f(x)]$$for all $x\in X$. As $df_{x}:T_{x}(X)\rightarrow T_{f(x)}(Y)$ is a linear map between the tangent spaces, it pulls back a $p$-tensor on the tangent space of $Y$ to a $p$-tensor on the tangent space of $X$. The pullback has the following properties: $$\begin{align}
f^{*}(\omega_{1}+\omega_{2})&=f^{*}\omega_{1}+f^{*}\omega_{2}\\
f^{*}(\omega_{1}\land \omega_{2})&=f^{*}\omega_{1}\land f^{*}\omega_{2}\\
(f\circ h)^{*}\omega&=h^{*}f^{*}\omega(Check if this is needed)\\
\end{align}$$
(NUMVER 1) is obvious from the linearity of the derivative and its pullback: $$f^{*}(\omega_{1}+\omega_{2})(x)=(df_{x})^{*}(\omega_{1}+\omega_{2})[f(x)]=(df_{x})^{*}\omega_{1}[f(x)]+(df_{x})^{*}\omega_{2}[f(x)]=f^{*}\omega_{1}(x)+f^{*}\omega_{2}(x)$$FORMAT. Property (NUMBER ....): $$\begin{align*}
f^{*}(\omega_{1}\land \omega_{2})(x)&=(df_{x})^{*}(\omega_{1}\land \omega_{2})(x)\\
&=(df_{x})^{*}(\omega_{1}(x)\land \omega_{2}(x))\\
&=(df_{x})^{*}\omega_{1}(x)\land (df_{x})^{*}\omega_{2}(x) \text{ JUSTIFY with properties of puulback for tensors}\\
&=f^{*}\omega_{1}(x)\land f^{*}\omega_{2}(x)
\end{align*}$$Prove 3 if used.

Additionally, if $a:U \rightarrow \mathbb{R}$ is a $0$-form, then $$\begin{equation}f^{*}a=a\circ f\end{equation}$$
At each $x$, $a(x)$ is a $0$-tensor. So, Eq NUMBER shows that $(df_{x})^{*}$ is the identity. Therefore, $$\begin{equation}f^{*}a(x)=(df_{x})^{*}a[f(x)]=a[f(x)]=(a\circ f)(a)\end{equation}$$

Let $U\subseteq \mathbb{R}^{k},V\subseteq \mathbb{R}^{l}$. Let $x_{1},\ldots,x_{k}$ be the coordinate functions on $\mathbb{R}^{k}$ and $y_{1},\ldots,y_{l}$ be the coordinate functions on $\mathbb{R}^{l}$. Let $f:V \rightarrow U$ be a smooth function given by $f=(f_{1},\ldots,f_{k})$. Then, $$\begin{equation}f^{*}dx_{i}=\sum_{j=1}^{l}\frac{\partial f_{i}}{\partial y_{j}}\ dy_{j}=df_{i}\end{equation}$$

Fix $y\in V$ and let $a\in V$.
$$f^{*}dx_{i}(y)(a)=(df_{y})^{*}dx_{i}[f(y)](a)$$
At every $x$, $dx_{i}(x)=\begin{bmatrix}0 \cdots 1 \cdots 0\end{bmatrix}$ where the $i$'th column is nonzero. So, $$\begin{align*}(df_{y})^{*}dx_{i}[f(y)](a)&=dx_{i}[f(y)][df_{y}(a)]
=[0\cdots1\cdots0]\begin{bmatrix}\frac{\partial f_{1}}{\partial y_{1}}(y)&\cdots&\frac{\partial f_{1}}{\partial y_{l}}(y)\\\vdots&\ddots&\vdots\\\frac{\partial f_{k}}{\partial y_{1}}(y)&\cdots&\frac{\partial f_{k}}{\partial y_{l}}(y)\end{bmatrix}a\\
&=\begin{bmatrix}\frac{\partial f_{i}}{\partial y_{1}}(y)&\cdots&\frac{\partial f_{i}}{\partial y_{l}}(y)\end{bmatrix}a\end{align*}$$Let $a=(a_{1},\ldots,a_{l})$. Then, $$\begin{bmatrix}\frac{\partial f_{i}}{\partial y_{1}}(y) & \cdots & \frac{\partial f_{i}}{\partial y_{l}}(y)\end{bmatrix}a=\begin{bmatrix}\frac{\partial f_{i}}{\partial y_{1}}(y) & \cdots & \frac{\partial f_{i}}{\partial y_{l}}(y)\end{bmatrix}\begin{bmatrix}a_{1}\\\vdots\\a_{l}\end{bmatrix}=\sum_{j=1}^{l}a_{j}\frac{\partial f_{i}}{\partial y_{j}}(y)$$As $dy_{j}(y)(a)=a_{j}$, this shows the first equality of Eq NUMBER. For the second equality,$$df_{i}(y)(a)=\begin{bmatrix}\frac{\partial f_{i}}{\partial y_{1}}(y) & \cdots  & \frac{\partial f_{i}}{\partial y_{l}}(y)\end{bmatrix}\begin{bmatrix}a_{1}\\\vdots\\a_{l}\end{bmatrix}=\sum_{j=1}^{l}a_{j}\ \frac{\partial f_{i}}{\partial y_{j}}(y)$$

$$\begin{equation}df=\sum_{j=1}^{l}\frac{\partial f}{\partial x_{j}}\ dy_{j}\end{equation}$$Fix $y\in V$. Let $a=(a_{1},\ldots,a_{l})$. Then, $df(y)=df_{y}$, so $$df_{y}(a)=\begin{bmatrix}\frac{\partial f}{\partial y_{1}}(y) & \cdots & \frac{\partial f}{\partial y_{i}}(y)\end{bmatrix}\begin{bmatrix}a_{1}\\\vdots\\a_{l}\end{bmatrix}=\sum_{j=1}^{l}a_{j}\ \frac{\partial f}{\partial y_{j}}(y)$$Since $dy_{j}(y)(a)=a_{j}$, Eq NUMBER holds.


Let $f:V \rightarrow U$ be a diffeomorphism. Then, $df_{y}$ is an isomorphism. Let $\omega$ be a $k$-form on $U\subseteq \mathbb{R}^{k}$. Then, $\omega=a\ dx_{1}\land\cdots\land dx_{k}$ for some function $a:U \rightarrow \mathbb{R}$. So, the pullback of $\omega$ by $f$ evaluated at $y\in V$: $$\begin{align*}f^{*}\omega(y)&=f^{*}(a\ dx_{1}\land\cdots\land dx_{k})(y)\\
&=(f^{*}a\ f^{*}dx_{1}\land\ldots\land f^{*}dx_{k})(y)\\
&=(a\circ f)(y)\cdot(df_{y})^{*}dx_{1}\land\cdots\land(df_{x})^{*}dx_{k}[f(y)]\\
&=(a\circ f)(y)\cdot(\text{det }df_{y})(dx_{1}\land\cdots\land dx_{k})[f(y)]\quad(det thm)\\
&=(a\circ f)(y)\cdot(\text{det }df_{y})(dy_{1}\land\cdots\land dy_{k})(y)\end{align*}$$So, the pullback of a $k$-form form by a diffeomorphism $f$ is $$\begin{equation}f^{*}\omega=(a\circ f)(\text{det }df)\ dy_{1}\land\cdots\land dy_{k}\end{equation}$$


<h1 align=center> Integration of Forms </h1>


For the rigorous technical definition of integration and integrability of functions on $\mathbb{R}^{n}$, see Spivak (PAGES and FORMAT). The following theorem from multivariable calculus allows us to extend integration to manifolds through parameterizations.

>[!thm] 
>Suppose $f:V \rightarrow U$ is a diffeomorphism of open sets in $\mathbb{R}^{k}$ or $H^{k}$ and $a:U \rightarrow \mathbb{R}$ is an integrable function. Then, $$\int_{U}a\ dx_{1}\cdots dx_{k}=\int_{V}(a\circ f)|\text{det }df|dy_{1}\cdots dy_{k}$$where $df$ is the differential of $f$ mapping $x\mapsto df_{x}$.

Let $\omega=a\ dx_{1}\land\cdots\land dx_{k}$ and define $$\int_{U}\omega=\int_{U}a\ dx_{1}\cdots dx_{k}$$Then Eq NUMBER shows that Thm NUMBER may be stated(talk about orientations)$$\int_{U}\omega=\int_{V}f^{*}\omega$$
All $k$-forms on $U$ may be written as $a\ dx_{1}\land\cdots\land dx_{k}$ for some real-valued function $a$ on $U$. So, an intuitive definition of an integrability of forms is whether the function $a$ is integrable (reword).

Let $X$ be a $k$-dimensional manifold. The *support* of a $k$-form $\omega$ on $X$ is the closure of the set of points in $X$ for which $\omega$ is nonzero. Assume that $\omega$ has compact support. 

If the support of $\omega$ is contained in some parametrizable open subset $W$ of $X$, let $\phi:U \rightarrow W$ be an orientation-preserving diffeomorphism for $U\subseteq H^{k}$. Then, $\phi^{*}\omega$ is a compactly supported, smooth $k$-form on $U$. Clearly, $$\begin{equation}\int_{W}\omega=\int_{U}\phi^{*}\omega\end{equation}$$As $\omega$ is $0$ outside of $W$, $$\int_{X}\omega=\int_{W}\omega=\int_{U}\phi^{*}\omega$$integrates $\omega$ over the manifold $X$. (Justify independence of parameterization choice?)

Now abandon the assumption that the compact support of $\omega$ is contained in a single parametrizable subset of $X$. Let $\mathcal{W}$ be the collection of parametrizable subsets of $X$. Let $\theta_{i}$ be a partition of unity subordinate to $\mathcal{W}$. For each $x\in X$, there is a parametrizable neighborhood $W$ of $X$  such that only finitely many $\theta_{i}$ are nonzero on . The collection of such $W$ forms an open cover of the compact set $\text{spt }\omega$. This collection must omit a finite subcover. As only finitely many $\theta_{i}$ are nonzero on each element of this subcover, only finitely many $\theta_{i}$ are nonzero on $\text{spt }\omega$. As each $\theta_{i}$ is nonzero only on a compact (EXPLAIN?) subset of a single parametrizable subset $W_{i}$ of $X$, $$\int_{X}\theta_{i}\omega=\int_{W_{i}}\theta_{i}\omega$$may be found by Eq NUMBER. As $\theta_{i}\omega$ is nonzero for only finitely many $i$, define $$\int_{X}\omega=\sum_{i}\int_{X}\theta_{i}\omega$$For proofs that the given definition of integration does not depend on the choice of parameterization and partition of unity, see ...


Theorems:
- [[Change of Variables in Rn]] (in terms of functions and forms) Theorem 3-13 in Spivak
- use of [[Partition of Unity]] to extend integration to manifolds

>[!note]
>I don't think integrating other forms over submanifolds is important

<h1 align=center> Differentiation of Forms </h1>
Definitions:
- [[Exterior Derivative]]

As the differential of a function is a $1$-form, it makes sense to define a differentiation operation on forms. Let $\omega=\sum f_{I}dx_{I}$ be a $p$-form on an open set $U\subseteq H^{k}$. Then, $$\begin{equation}d \omega=\sum df_{I}\land dx_{I}\end{equation}$$defines a $(p+1)$-form on $U$. The operator $d$ has the following linearity relationship for forms on Euclidean space: $$\begin{equation}d(\omega_{1}+\omega_{2})=d\sum_{I}(f_{I_{1}}+f_{I_{2}})\land dx_{I}=\sum_{I}d(f_{I_{1}}+f_{I_{2}})\land dx_{I}=\sum_{I}(d f_{I_{1}}+d f_{I_{2}})\land dx_{I}=d \omega_{1}+d \omega_{2}\end{equation}$$
>[!prop] Lemma
Suppose that $g\colon V \rightarrow U$ is a diffeomorphism of open sets of $H^{k}$. Then for every form $\omega$ on $U$, $d(g^{*}\omega)=g^{*}(d \omega)$

See... for proof. Analogous to how Theorem NUMBER allows definition of integration on manifolds, Lemma NUMBER gives a local definition of the exterior derivative of forms on manifolds. Let $X$ be a manifold. For any parameterization $\phi:U \rightarrow X$, define $d \omega$ on the image of $\phi$ by $$(\phi^{-1})^{*}d(\phi^{*}\omega)$$Now let $\psi:V \rightarrow X$ be another parameterization with $V\cap U\ne \emptyset$. Let $\xi=\phi^{-1}\circ \psi$. Lemma NUMBER gives: $$
(\psi^{-1})^{*}d(\psi^{*}\omega)=(\psi^{-1})^{*}d(\xi^{*}\phi^{*}\omega)=(\psi^{-1})^{*}\xi^{*}d(\phi^{*}\omega)=(\phi^{-1})^{*}d(\phi^{*}\omega)
$$showing the independence of $d \omega$ on the choice of parameterization. 




The operator $d$ for forms on arbitrary manifolds has the following linearity property: $$\begin{align}d(\omega_{1}+\omega_{2})&=d \omega_{1}+d \omega_{2}\\
\end{align}$$Let $\phi:U \rightarrow X$ be some parameterization. On the image of $U$, $$\begin{align*}d (\omega_{1}+\omega_{2})&=(\phi^{-1})^{*}d(\phi^{*}(\omega_{1}+\omega_{2}))\\
&=(\phi^{-1})^{*}d(\phi^{*}\omega_{1}+\phi^{*}\omega_{2})\\
&=(\phi^{-1})^{*}(d (\phi^{*}\omega_{1})+d(\phi^{*}\omega_{2}))\quad(NUMBER)\\
&=(\phi^{-1})^{*}d (\phi^{*}\omega_{1})+(\phi^{-1})^{*}d(\phi^{*}\omega_{2})\\
&=d \omega_{1}+d \omega_{2}\end{align*}$$

Following are some useful characterizations of forms on Euclidean space.

For any $p$-form $\omega=\sum f_{I}\ dx_{I}$ on $U\subseteq \mathbb{R}^{k}$, $$\begin{align*}
d \omega&=d\sum_{I}f_{I}\ dx_{I}\\
&=\sum_{I}d(f_{I}\ dx_{I})\\
&=\sum_{I}df_{I}\land dx_{I}\quad(\text{Eq NUMBER})\\
&=\sum_{I}\left(\sum_{i=1}^{k}\frac{\partial f_{I}}{\partial x_{i}}\ dx_{i}\right)\land dx_{I}\quad (\text{Eq NUMBER})\\
&=\sum_{I}\sum_{i=1}^{k}\frac{\partial f_{I}}{\partial x_{i}}\ dx_{i}\land dx_{I}
\end{align*}$$

From Thm NUMBER, $dx_{J}=0$ if $J$ has any duplicate indices. So, $dx_{i}\land dx_{I}\ne0$ only if $i\notin I$. Thus, $$\sum_{i=1}^{k}\frac{\partial f_{I}}{\partial x_{i}}\ dx_{i}\land dx_{I}=\sum_{i\notin I}\frac{\partial f_{I}}{\partial x_{i}}\ dx_{i}\land dx_{I}$$So, $$\begin{equation}d \omega=\sum_{I}\sum_{i\notin I}\frac{\partial f_{I}}{\partial x_{i}}\ dx_{i}\land dx_{I}\end{equation}$$In particular, if $\omega$ is a $(k-1)$-form, $$\begin{equation} d \omega=\sum_{I}\sum_{i\notin I}\frac{\partial f_{I}}{\partial x_{i}}\ dx_{i}\land dx_{I}=\sum_{i=1}^{k}(-1)^{i}\frac{\partial f_{i}}{\partial x_{i}}\ dx_{1}\land\cdots\land dx_{k}\end{equation}$$where $f_{I}=f_{i}$ when $i\notin I$. 

Theorems:
- [[Properties of the Exterior Derivative]]
- 

<h1 align=center> Generalized Stokes Theorem </h1>
>[!thm]
>Let $X$ be an oriented compact $k$-dimensional manifold with boundary, and let $\partial X$ denote the $(k-1)$-dimensional boundary of $X$ with the boundary orientation. If $\omega$ is a $(k-1)$-form on $\partial X$, then $$\int_{X}d \omega=\int_{\partial X}\omega$$



Assume the compact support of $\omega$ is contained in a single parametrizable subset $W$ of $X$. Let $\phi:U \rightarrow W$ be a parameterization.

First assume that $U\subseteq \mathbb{R}^{k}$. Then, $\omega$ is uniformly $0$ on the boundary of $X$. So we must show that $\int_{X}d \omega=0$. Write the $(k-1)$-form on $U$ $$\phi^{*}\omega=\sum_{I}f_{I}dx_{I}$$where $I$ are increasing sequences of length $k-1$. Clearly, this is equivalent to $$\phi^{*}\omega=\sum_{i=1}^{k}(-1)^{i-1}f_{i}\ dx_{1}\land\cdots \widehat{dx_{i}}\land\cdots\land dx_{k}$$where $\widehat{dx_{i}}$ indicates $dx_{i}$ is omitted from the wedge product. As, $d(\phi^{*}\omega)=\phi^{*}d \omega$ by Eq NUMBER,
$$\int_{X}d \omega=\int_{U}\phi^{*}d \omega=\int_{U}d(\phi^{*}\omega)$$From Eq NUMBER (verify signs here), $$d(\phi^{*}\omega)=\sum_{i=1}^{k}\frac{\partial f_{i}}{\partial x_{i}}\ dx_{1}\land\cdots\land dx_{k}$$
So, $$\int_{U}d(\phi^{*}\omega)=\int_{U}\sum_{i=1}^{k}\frac{\partial f_{i}}{\partial x_{i}}\ dx_{1}\land\cdots\land dx_{k}=\sum_{i=1}^{k}\int_{U}\frac{\partial f_{i}}{\partial x_{i}}\ dx_{1}\land\cdots\land dx_{k}$$by the linearity of the integral. Using the definition of integration of forms: $$\sum_{i=1}^{k}\int_{U}\frac{\partial f_{i}}{\partial x_{i}}\ dx_{1}\land\cdots\land dx_{k}=\sum_{i=1}^{k}\int_{U}\frac{\partial f_{i}}{\partial x_{i}}dx_{1}\cdots dx_{k}$$

As $U$ contains the support of $\phi^{*}\omega$, for all $x\in \mathbb{R}^{k}-U$, $\forall i: f_{i}=0$. So, $$\int_{U}\frac{\partial f_{i}}{\partial x_{i}}\ dx_{1}\cdots dx_{k}=\int_{\mathbb{R}^{k}}\frac{\partial f_{i}}{\partial x_{i}}\ dx_{1}\cdots dx_{k}$$Now examine the integral $\int_\mathbb{R} \frac{\partial f_{i}}{\partial x_{i}}dx_{i}$ for some $i$. $$\int_\mathbb{R}\frac{\partial f_{i}}{\partial x_{i}}dx_{i}=\lim_{a \rightarrow \infty}\int_{-a}^{a}\frac{\partial f_{i}}{\partial x_{i}}dx_{i}=\lim_{a \rightarrow \infty}(\left.f_{i}(x_{1},\ldots,x_{i},\ldots,x_{k})\right|_{x_{i}=-a}^{x_{i}=a})$$by the fundamental theorem of calculus. As $\text{spt }\omega$ has compact support, so must $\text{spt } f_{i}$. So, outside of some interval $[-a,a]$, $f_{i}$ is uniformly 0. Now integrate $\frac{\partial f_{i}}{\partial x_{i}}$ over all of $\mathbb{R}^{k}$. Fubini's Theorem (cite spivak) gives $$\int_{\mathbb{R}^{k}}\frac{\partial f_{i}}{\partial x_{i}}\ dx_{1}\cdots dx_{k}=\int_{\mathbb{R}^{k-1}}\left(\int_\mathbb{R} \frac{\partial f_{i}}{\partial x_{i}}\ dx_{i}\right)dx_{1}\cdots\widehat{dx_{i}}\cdots dx_{k}=\int_{\mathbb{R}^{k-1}}0\ dx_{1}\cdots\widehat{dx_{i}}\cdots dx_{k}=0$$Therefore, $$\int_{X}d \omega=\sum_{i=1}^{k}\int_{\mathbb{R}^{k}}\frac{\partial f_{i}}{\partial x_{i}} \ dx_{1}\cdots dx_{k}=0$$


Now, assume that $U\not\subseteq \mathbb{R}^{k}$, so $U\subseteq H^{k}$ and $U$ intersects the boundary of $H^{k}$. Again, $$\int_{X}d \omega=\sum_{i=1}^{k}\int_{H^{k}}\frac{\partial f_{i}}{\partial x_{i}}\ dx_{1}\cdots dx_{k}$$For all $i<k$, $$\int_{H^{k}}\frac{\partial f_{i}}{\partial x_{i}}\ dx_{1}\cdots dx_{k}=\int_{H^{k-1}}\left(\int_\mathbb{R} \frac{\partial f_{i}}{\partial x_{i}}dx_{i}\right)dx_{1}\cdots\widehat{dx_{i}}\cdots dx_{k}=0$$for the same reasoning as before. Now, $$\int_{H^{k}}\frac{\partial f_{k}}{\partial x_{k}}\ dx_{1}\cdots dx_{k}=\int_{\mathbb{R}^{k-1}}\left(\int_{H^{1}}\frac{\partial f_{k}}{\partial x_{k}}dx_{k}\right)dx_{1}\cdots dx_{k-1}$$and $$\int_{H^{1}}\frac{\partial f_{k}}{\partial x_{k}}\ dx_{k}=\int_{0}^{\infty}\frac{\partial f_{k}}{\partial x_{k}}\ dx_{k}=\lim_{a \rightarrow \infty}\left.f_{k}(x_{1},\ldots,x_{k-1},x_{k})\right|_{x_{k}=0}^{x_{k}=a}$$by the fundamental theorem of calculus. As the support of $f_{k}$ is compact, it is bounded ([[Heine-Borel Theorem]]). So for sufficiently large $a$, $f_{k}(x_{1},\ldots,x_{k-1},a)=0$. Then, $$\int_{H^{1}}\frac{\partial f_{k}}{\partial x_{k}}\ dx_{k}=0-f_{k}(x_{1},\ldots,x_{k-1},0)=-f_{k}(x_{1},\ldots,x_{k-1},0)$$giving$$\int_{X}d\omega=\int_{\mathbb{R}^{k-1}}-f_{k}(x_{1},\ldots,x_{k-1},0)\ dx_{1}\cdots dx_{k-1}$$







$$\int_{\partial X}\omega=\int_{U\cap \partial H^{k}}\phi^{*}\omega=\int_{\partial H^{k}}\phi^{*}\omega=\int_{\partial H^{k}}\sum_{i=1}^{k}(-1)^{i-1}f_{i}\ dx_{1}\land\cdots\land\widehat{dx_{i}}\land\cdots\land dx_{k}$$
As $x_{k}=0$ on the boundary of $H^{k}$, $dx_{k}=0$ on $\partial H^{k}$ as well. Only the $k$-th term of the sum does not have a $dx_{k}$ term, so $$\int_{\partial H^{k}}\phi^{*}\omega=\int_{\partial H^{k}}(-1)^{k-1}f_{k}\ dx_{1}\land\cdots\land dx_{k-1}$$
Let $e_{1},\ldots,e_{k}$ be the ordered standard basis for $\mathbb{R}^{k}$. Then, $e_{1},\ldots,e_{k-1}$ is the standard basis for $\mathbb{R}^{k-1}$. The outward unit normal vector to $H^{k}$ is $-e_{k}=(0,\ldots,0,-1)$. In the boundary orientation of $\partial H^{k}$, the sign of the ordered basis $e_{1},\ldots,e_{k-1}$ is the sign of the ordered basis $-e_{k},e_{1},\ldots,e_{k-1}$ in $H^{k}$. Let $h$ be the diffeomorphism that takes $(x_{1},\ldots,x_{k-1})$ in $\mathbb{R}^{k-1}$ to $(x_{1},\ldots,x_{k-1},0)$ in $\partial H^{k}$. The alternating property of the determinant shows that $h$ alters orientation by a factor of $(-1)^{k}$. Therefore, $$\int_{\partial H^{k}}\phi^{*}\omega=(-1)^{k}\int_{\mathbb{R}^{k-1}}(-1^{k-1})f_{k}\ dx_{1}\land\cdots\land dx_{k-1}=\int_{\mathbb{R}^{k-1}}-f_{k}\ dx_{1}\cdots dx_{k-1}$$as $(-1)^{k}(-1)^{k-1}=-1$. 


Now, abandon the assumption that the compact support of $\omega$ is contained in a single parametrizable subset of $X$. Choose a partition of unity $\theta_{i}$ subordinate to the collection of parametrizable subsets of $X$. Clearly, the special case above gives $$\int_{\partial X}\theta_{i}\omega=\int_{X}d \theta_{i}\omega$$By the definition of ...
$$\int_{\partial X}\omega=\sum_{i}\int_{\partial X}\theta_{i}\omega=\sum_{i}\int_{X}d \theta_{i}\omega=\int_{X}\sum_{i}d \theta_{i}\omega$$By Eq NUMBER, $$\sum_{i}d \theta_{i}\omega=d\sum \theta_{i}\omega=d \omega$$so, $$\int_{\partial X}\omega=\int_{X}\sum_{i}d \theta_{i} \omega=\int_{X}d \omega$$



<h1 align=center> Examples </h1>
Maybe use the examples of integration of forms in $\mathbb{R}^3$ and derive green's theorem, stokes' theorem, divergence theorem?

Volume SA relation? (is this stokes?)

The 1, 2, and 3-forms in $\mathbb{R}^{3}$ may be concisely characterized. 

All $0$-forms on $\mathbb{R}^{3}$ are functions: $f:\mathbb{R}^{3}\rightarrow \mathbb{R}$. 



The following classical theorems of calculus are immediate low-dimensional corollaries of Thm NUMBER. 

>[!prop] Corollary: Fundamental Theorem of Calculus
Let $a,b\in \mathbb{R}$. Let $f:[a,b]\rightarrow \mathbb{R}$ be a smooth function. Then, $$\int_{a}^{b}f'(x)\ dx=f(b)-f(a)$$

>[!proof]

Of course, this was in proving the generalized Stokes Theorem, so the following is not a valid proof. It serves to illustrate that the fundamental theorem of calculus is just a special case...

The interval $[a,b]$ is a smooth $1$-dimensional manifold with boundary. Its boundary is the $0$-dimensional manifold $\{a,b\}$ with orientation ... . By Eq NUMBER, $$df=\frac{\partial f}{\partial x}\ dx=f'\ dx$$Use the definition of integrating a $0$-dimensional manifold given in (4.5 Problem 1). Then, $$\int_{\partial [a,b]}f=f(b)-f(a)\quad(\text{explain orientation more})$$
and, $$\int_{\partial [a,b]}f=\int_{[a,b]}df$$by Thm NUMBER.


>[!prop] Corollary: Green's Theorem
Let $W\subseteq \mathbb{R}^{2}$ be compact and let $\gamma=\partial W$ be smooth. Then $$\int_{\gamma}f\ dx+g\ dy=\int_{W}\left(\frac{\partial g}{\partial x}-\frac{\partial f}{\partial y}\right)\ dx\ dy$$

>[!proof]
Let $\omega=f\land dx+g\land dy$. Then, $$d \omega=\left((-1)^{1}\frac{\partial f}{\partial y}+\left(-1\right)^{2}\frac{\partial g}{\partial x}\right)\ dx\ dy$$by Eq NUMBER. By Thm NUMBER, $$\int_{\gamma}\omega=\int_{W}d \omega$$So, $$\int_{\gamma}f\ dx+g\ dy=\int_{\gamma}\omega=\int_{W}d \omega=\int_{W}\left(\frac{\partial g}{\partial x}-\frac{\partial f}{\partial y}\right)\ dx\ dy$$


Maybe define integration of a vector field over a surface before stating the theorem

Assume that $S$ is the graph of a function $G:\mathbb{R}^{2}\rightarrow \mathbb{R}$. (MAYBE ELABORATE ON THIS). Then, $\phi:\mathbb{R}^{2}\rightarrow S$ defined by $$\phi(x_{1},x_{2})=(x_{1},x_{2},G(x_{1},x_{2}))$$is a parameterization of $S$ (CLARIFY?).

The normal vector $\vec{n}$ to $S$ is given by $$\vec{n}=\left(-\frac{\partial G}{\partial x_{1}},-\frac{\partial G}{\partial x_{2}},1\right)$$The *area form* $dA$ is a smooth $2$-form on $S$ defined by $$dA=|\vec{n}|\ dx_{1}\land dx_{2}=\sqrt{\left(\frac{\partial G}{\partial x_{1}}\right)^{2}+\left(\frac{\partial G}{\partial x_{2}}\right)^{2}+1}\ dx_{1}\land dx_{2}$$

The *curl* of a vector field $\vec{F}=(f_{1},f_{2},f_{3})$ on $\mathbb{R}^{3}$ is the vector field $$\text{curl }\vec{F}=\left(\frac{\partial f_{3}}{\partial x_{2}}-\frac{\partial f_{2}}{\partial x_{3}},\frac{\partial f_{1}}{\partial x_{3}}-\frac{\partial f_{3}}{\partial x_{1}},\frac{\partial f_{2}}{\partial x_{1}}-\frac{\partial f_{1}}{\partial x_{2}}\right)$$

$$\text{curl }\vec{F}\cdot\vec{n}=\left(\frac{\partial f_{2}}{\partial x_{3}}-\frac{\partial f_{3}}{\partial x_{2}}\right)\cdot\frac{\partial G}{\partial x_{1}}+\left(\frac{\partial f_{3}}{\partial x_{1}}-\frac{\partial f_{1}}{\partial x_{3}}\right)\cdot\frac{\partial G}{\partial x_{2}}+\frac{\partial f_{2}}{\partial x_{1}}-\frac{\partial f_{1}}{\partial x_{2}}$$

>[!prop] Corollary: Classical Stokes' Theorem
Let $S\subseteq \mathbb{R}^{3}$ be a compact oriented $2$-dimensional manifold with boundary. Let $\vec{F}=(f_{1},f_{2},f_{3})$ be a vector field in $\mathbb{R}^{3}$. Then $$\int_{S}(\text{curl }\vec{F}\cdot\vec{n})\ dA=\int_{\partial S}f_{1}dx_{1}+f_{2}dx_{2}+f_{3}dx_{3}$$

>[!proof]


Let $\omega=f_{1}\land dx_{1}+f_{2}\land dx_{2}+f_{3}\land dx_{3}$ be a $1$-form on $S$. Then, $$d \omega=\sum_{i=1}^{3}df_{i}\land dx_{i}=\sum_{i=1}^{3}\left(\sum_{k=1}^{3}\frac{\partial f_{i}}{\partial x_{k}}\ dx_{k}\right)\land dx_{i}$$by Eq NUMBER. For each $i$, $$\begin{align*}\sum_{k=1}^{3}\frac{\partial f_{i}}{\partial x_{k}}\ dx_{k}\land dx_{i}&=\frac{\partial f_{i}}{\partial x_{1}}\ dx_{1}\land dx_{i}+\frac{\partial f_{i}}{\partial x_{2}}\ dx_{2}\land dx_{i}+\frac{\partial f_{i}}{\partial x_{3}}\ dx_{3}\land dx_{i}\end{align*}$$so, $$d \omega=\left(\frac{\partial f_{2}}{\partial x_{1}}-\frac{\partial f_{1}}{\partial x_{2}}\right)\ dx_{1}\land dx_{2}+\left(\frac{\partial f_{3}}{\partial x_{1}}-\frac{\partial f_{1}}{\partial x_{3}}\right)\ dx_{1}\land dx_{3}+\left(\frac{\partial f_{3}}{\partial x_{2}}-\frac{\partial f_{2}}{\partial x_{3}}\right)\ dx_{2}\land dx_{3}$$
By Thm NUMBER, $$\int_{\partial S}\omega=\int_{S}d \omega=\int_{\mathbb{R}^{2}}\phi^{*}d \omega$$

Compute $\phi^{*}d \omega$: Eq NUMBER and Eq NUMBER give$$\begin{align*}
\phi^{*}dx_{1}&=dx_{1}\\
\phi^{*}dx_{2}&=dx_{2}\\
\phi^{*}dx_{3}&=dG=\frac{\partial G}{\partial x_{1}}\ dx_{1}+\frac{\partial G}{\partial x_{2}}\ dx_{2}\quad(\text{Eq NUMBER})\\
\phi^{*}dx_{1}\land dx_{2}&=\phi^{*}dx_{1}\land \phi^{*}dx_{2}=dx_{1}\land dx_{2}\\
\phi^{*}dx_{1}\land dx_{3}&=\phi^{*}dx_{1}\land \phi^{*}dx_{3}=dx_{1}\land\left(\frac{\partial G}{\partial x_{1}}\ dx_{1}+\frac{\partial G}{\partial x_{2}}\ dx_{2}\right)=\frac{\partial G}{\partial x_{2}}dx_{1}\land dx_{2}\\
\phi^{*}dx_{2}\land dx_{3}&=\phi^{*}dx_{2}\land \phi^{*}dx_{3}=dx_{2}\land\left(\frac{\partial G}{\partial x_{1}}\ dx_{1}+\frac{\partial G}{\partial x_{2}}\ dx_{2}\right)=-\frac{\partial G}{\partial x_{1}}\ dx_{1}\land dx_{2}
\end{align*}$$so, $$\begin{align*}\phi^{*}d \omega=\left(\frac{\partial f_{2}}{\partial x_{1}}-\frac{\partial f_{1}}{\partial x_{2}}\right)\circ \phi\ dx_{1}\land dx_{2}&\\
+\left(\frac{\partial f_{3}}{\partial x_{1}}-\frac{\partial f_{1}}{\partial x_{3}}\right)&\circ \phi\cdot\frac{\partial G}{\partial x_{2}}\ dx_{1}\land dx_{2}\\
-&\left(\frac{\partial f_{3}}{\partial x_{2}}-\frac{\partial f_{2}}{\partial x_{3}}\right)\circ \phi\cdot\frac{\partial G}{\partial x_{1}}\ dx_{1}\land dx_{2}\\
\end{align*}$$


