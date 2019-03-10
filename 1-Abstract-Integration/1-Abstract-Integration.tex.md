# Abstract Integration

## **Topological Space**

Let $\mathcal{T}_X \subset \mathcal{P}(X)$.  Then $(X,\mathcal{T}_X)$ is a *topological space* $\iff$

1. $\emptyset , X \in \mathcal{T}_X$
2. $\forall I_n \in \mathcal{F}\big(\N \to \mathcal{T}_X\big)\quad\bigcap_{n=0}^\infty I_n \in \mathcal{T}_X$
3. $\forall U \in \mathcal{P}(\mathcal{T}_X)\quad \bigcup_{u \in U} u \in  \mathcal{T}_X$

$\mathcal{T}_X$ is a *topology* and $\mathscr{T}_X$ is the *family of topologies* on $X$.

For $(X,\mathcal{T}_X)$ and $(Y,\mathcal{T}_Y)$, we say a function $f : X \to Y$ is *continuous* when $\bigcup_{V \in \mathcal{T}_Y}\{f^{-1}(V)\} \subseteq \mathcal{T}_X$.  Equivalently we write $f \in \mathcal{C}(X \to Y)$

Locally, we can say $g : X \to Y$ is *continuous at the point* $x_0$ provided every neighborhood of $g(x_0)$ contains the image of a neighborhood of $x_0$.  It can be proven that a function is continous if and only if it is continuous at all points.

## **Measurable Space**

### *Rudin's Minimal Definition*

Let $𝔐_X \subset \mathcal{P}(X)$.  Then $(X,𝔐_X)$ is a *measurable space* $\iff$

1. $X \in 𝔐_X$
2. $\forall A_n \in \mathcal{F}\big(\Z^+ \to 𝔐_X\big)\quad \bigcup_{n=0}^\infty A_n \in 𝔐$
3. $\forall C \in 𝔐_X \quad C^c \in  𝔐_X$

### *Working Maximal Definition*

Let $𝔐_X \subset \mathcal{P}(X)$.  Then $(X,𝔐_X)$ is a *measurable space* $\iff$

1. $\emptyset , X \in 𝔐_X$
2. $\forall A_n \in \mathcal{F}\big(\N \to 𝔐_X\big)\quad\bigcap_{n=0}^\infty A_n,\bigcup_{n=0}^\infty A_n \in 𝔐$
3. $\forall A,B \in 𝔐_X \quad A-B \in  𝔐_X$

$𝔐_X$ a $\bm{\sigma}$**-algebra** and $\Omega_X$ is the *family of all $\sigma$-algebras* on $X$

For $(X,𝔐_X)$ and $(Y,\mathcal{T}_Y)$, we say a function $f : X \to Y$ is *measurable* when $\bigcup_{V \in \mathcal{T}_Y}\{f^{-1}(V)\} \subseteq 𝔐_X$

$\underline{Proof}$ (of equivalence)

for each enumerated property of $\sigma$-algebras we show its equivalence,

1. $\emptyset = X^c \in 𝔐$
2. $\bigcap_{n=0}^\infty A_n = \big(\bigcup_{n=0}^\infty A_n^c \big)^c \in 𝔐$
3. $A-B=B^c \cap A \in 𝔐$

## *Continuous function composition preserves measurability*

$\underline{Proof}$

Let $f : X \to Y$ be a measurable function and $g : Y \to Z$ be a continuous function 

$$\bigcup_{V \in \mathcal{T}_Z}\{g \circ f^{-1}(V))\} = \bigcup_{V \in \mathcal{T}_Z}\{f^{-1}(g^{-1}(V))\} = \underbrace{\bigcup_{U \in \bigcup_{V \in \mathcal{T}_Z}\{g^{-1}(V)\}}}_{\text{continuity}}\{f^{-1}(U)\} \subseteq \overbrace{\bigcup_{U \in \mathcal{T}_Y}\{f^{-1}(U)\} \subseteq 𝔐_X}^{\text{measurability}}$$

Thus $g \circ f$ is measurable $\ \blacksquare$

## **Metric Space**

Let $d : X \times X \to \R^+ \cup \{0\}$.  Then $(X,d) \text{is a metric space} \iff \forall x,y,z \in X$

1. $d(x,y)=0 \iff x=y$
2. $d(x.y)=d(y,x)$
3. $d(x,z) \leq d(x,y)+d(y,z)$

## The Cartesian Product (on $\R$) preserves measurability

For $(X,𝔐_X)$ and $(Y,\mathcal{T}_Y)$, $u,v: X \to \mathbb{R}$ and $\Phi \in \mathcal{C}(\mathbb{R}^2 \to Y)$

$x \mapsto \Phi(u(x),v(x))$ defines a measurable function on X

>The key to this proof is that an open set in $\R^2$ is a cartesian product of subsets of $\R^1$ that are themselves open.  I should come back here and try to work out if $\R$ is really neccesary or if replacing $\R$ with any topological space and product space would work.

### Correlaries

1. A complex function is measurable if and only if its real and imaginary parts are measurable
2. if $f$ and $g$ are complex measureable functions then $|f|$, $f+g$, and $f g$ are measurable
3. If $f$ is a complex measureable function on $X$ there is a complex measurable function $\alpha$ on $X$ such that $|\alpha|=1$ and $f=\alpha|f|$
4. The Characteristic function is measurable on measurable sets

## **Borel Set**

The *Borel sets* of  $(X,\mathcal{T}_X)$ are given $ℬ_{\mathcal{T}_X}:=\bigcap \big\{𝔐 \in  \Omega_X  \ : \ \mathcal{T}_X \subset \mathcal{T}_X \cap 𝔐  \big\}$

A mapping is *Borel measurable* if it is a measurable on its Borel set.

## Properties of Borel Sets

1. $ℬ_{\mathcal{T}_X}$ is a $\sigma$-algebra on $X$
2. $ℬ_{\mathcal{T}_X}$ contains $\mathcal{T}_X$
3. All other $\sigma$-algebras that contain $\mathcal{T}_X$ contain $ℬ_{\mathcal{T}_X}$
4. Continuous mappings are Borel measurable

To prove these properties we prove the following more general statement (above follows for $ℱ:=\mathcal{T}_X$)

### Borel Properties Lemma

Let $ℱ \subset \mathcal{P}(X)$  Then there is some $\sigma$-algebra $𝔐^*$ such that

$$ℱ \subset 𝔐^* \subset 𝔐$$

for all possible $𝔐$ $\sigma$-algebras in $X$ containing ℱ

$\underline{Proof}$

Since $\mathcal{P}(X)\in \big\{𝔐 \in  \Omega_X  \ : \  ℱ \subset \mathcal{X} \cap 𝔐 \big\}$ we know $ℱ \in 𝔐^* := \bigcap \big\{𝔐 \in  \Omega_X  \ : \ ℱ \subset ℱ \cap 𝔐  \big\}$.  By its definition $𝔐^*$  contains all possible $\sigma$-algebras in $X$ containing ℱ.  Hence we need only prove it is itself a $\sigma$-algebra.  Notice any collection of sets that form a subset of $𝔐^*$ must be contained in all $\sigma$-algebras on $X$ containing $ℱ$ and hence any $\sigma$-algebra operation you could do on that collection would be contained in all $\sigma$-algebras on $X$ containing $ℱ$, and hence would be contained in the their intersection (i.e. $𝔐^*$).  

## More Properties relating a topology and a $\sigma$-algebra 

For $(X,𝔐_X)$, $(Y,\mathcal{T}_Y)$, and $f : X \to Y$

1. $\Big\{ E \in \mathcal{P}(Y) \ : \ f^{-1}(E) \in 𝔐_X \Big\}$ is a $\sigma$-algebra in $X$
2. if $f$ is measurable then $\bigcup_{E \in ℬ_{\mathcal{T}_Y}}$ $f^{-1}(E)$ $\subset 𝔐_X$
3. For Y=$[-\infty,\infty]$, if $\{f^{-1}((\alpha,\infty)) \subset X \ : \ \alpha \in \R \}$ $\subset 𝔐_X$ then $f$ is measurable
4. Borel mapping composition preserves measurability

$\textit{Proof}$

Need

## **Upper and Lower Limits**



1. A function is $\mu$ is **countably additive** if $\forall A \in \mathcal{F}(\N \to X)$ such that $A(\N)$ are disjoint $\mu(\bigcup_{i=1}^\infty A_i)=\sum_{i=1}^\infty A_i$
2. A **positive measure** is a function $\mu: 𝔐_X \to [0,\R]$ such that it is *countably additive*
3. A **complex measure** is a complex-valued countably additive function defined on a $\sigma$-algebra

### **Lebesgue's Monotone Convergence Theorem**

A sequence of dominating functions that converges pointwise to some $f$

1. Is measurable
2. the limit of the integral values of the sequence converge to the integral of $f$

### Lebesgue integrable functions

Let $\mu$ be a positive measure on an arbirary measurable space $X$

$L^1(\mu):=\Big\{ f \in \mathcal{F}(X \to \mathbb{C}) \ : \ \bigcup_{V \in \mathcal{T}_\mathbb{C}}\{f^{-1}(V)\} \subseteq 𝔐_X \ \land \ \int_X|f|d\mu < \infty \Big\}$

### Lebesgue's Dominated Convergence Theorem

suppose $f_n$ is a sequence of complex measureable function on $X$ that converges pointwise to $f$ if there is some $g \in L^1(\mu)
