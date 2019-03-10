# Abstract Integration

## **Topological Space**

Let $\mathcal{T}_X \subset \mathcal{P}(X)$.  Then $(X,\mathcal{T}_X)$ is a *topological space* $\iff$

1. $\emptyset , X \in \mathcal{T}_X$
2. $\forall I_n \in \mathcal{F}\big(\N \to \mathcal{T}_X\big)\quad\bigcap_{n=0}^\infty I_n \in \mathcal{T}_X$
3. $\forall U \in \mathcal{P}(\mathcal{T}_X)\quad \bigcup_{u \in U} u \in  \mathcal{T}_X$

$\mathcal{T}_X$ is a *topology* and $\mathscr{T}_X$ is the *family of topologies* on $X$.

For $(X,\mathcal{T}_X)$ and $(Y,\mathcal{T}_Y)$, we say a function $f : X \to Y$ is *continuous* when $\bigcup_{V \in \mathcal{T}_Y}\{f^{-1}(V)\} \subseteq \mathcal{T}_X$.  Equivalently we write $f \in C(X \to Y)$

Locally, we can say $g : X \to Y$ is *continuous at the point* $x_0$ provided every neighborhood of $g(x_0)$ contains the image of a neighborhood of $x_0$.  It can be proven that a function is continous if and only if it is continuous at all points.

## **Measurable Space**

### *Rudin's Minimal Definition*

Let $\mathfrak{M}_X \subset \mathcal{P}(X)$.  Then $(X,\mathfrak{M}_X)$ is a *measurable space* $\iff$

1. $X \in \mathfrak{M}_X$
2. $\forall A_n \in \mathcal{F}\big(\Z^+ \to \mathfrak{M}_X\big)\quad \bigcup_{n=0}^\infty A_n \in \mathfrak{M}$
3. $\forall C \in \mathfrak{M}_X \quad C^c \in  \mathfrak{M}_X$

### *Working Maximal Definition*

Let $\mathfrak{M}_X \subset \mathcal{P}(X)$.  Then $(X,\mathfrak{M}_X)$ is a *measurable space* $\iff$

1. $\emptyset , X \in \mathfrak{M}_X$
2. $\forall A_n \in \mathcal{F}\big(\N \to \mathfrak{M}_X\big)\quad\bigcap_{n=0}^\infty A_n,\bigcup_{n=0}^\infty A_n \in \mathfrak{M}$
3. $\forall A,B \in \mathfrak{M}_X \quad A-B \in  \mathfrak{M}_X$

$\mathfrak{M}_X$ a $\bm{\sigma}$**-algebra** and $\Omega_X$ is the *family of all $\sigma$-algebras* on $X$

For $(X,\mathfrak{M}_X)$ and $(Y,\mathcal{T}_Y)$, we say a function $f : X \to Y$ is *measurable* when $\bigcup_{V \in \mathcal{T}_Y}\{f^{-1}(V)\} \subseteq \mathfrak{M}_X$

$\underline{Proof}$ (of equivalence)

for each enumerated property of $\sigma$-algebras we show its equivalence,

1. $\emptyset = X^c \in \mathfrak{M}$
2. $\bigcap_{n=0}^\infty A_n = \big(\bigcup_{n=0}^\infty A_n^c \big)^c \in \mathfrak{M}$
3. $A-B=B^c \cap A \in \mathfrak{M}$

## Continuous function composition preserves measurability

$\underline{Proof}$

Let $f : X \to Y$ be a measurable function and $g : Y \to Z$ be a continuous function

$$\bigcup_{V \in \mathcal{T}_Z}\{g \circ f^{-1}(V))\} = \bigcup_{V \in \mathcal{T}_Z}\{f^{-1}(g^{-1}(V))\} = \underbrace{\bigcup_{U \in \bigcup_{V \in \mathcal{T}_Z}\{g^{-1}(V)\}}}_{\text{continuity}}\{f^{-1}(U)\} \subseteq \overbrace{\bigcup_{U \in \mathcal{T}_Y}\{f^{-1}(U)\} \subseteq \mathfrak{M}_X}^{\text{measurability}}$$

Thus $g \circ f$ is measurable $\ \blacksquare$

## **Metric Space**

Let $d : X \times X \to \R^+ \cup \{0\}$.  Then $(X,d) \text{is a metric space} \iff \forall x,y,z \in X$

1. $d(x,y)=0 \iff x=y$
2. $d(x.y)=d(y,x)$
3. $d(x,z) \leq d(x,y)+d(y,z)$

## The Cartesian Product (on $\R$) preserves measurability

For $(X,\mathfrak{M}_X)$ and $(Y,\mathcal{T}_Y)$, $u,v: X \to \mathbb{R}$ and $\Phi \in C(\mathbb{R}^2 \to Y)$

$x \mapsto \Phi(u(x),v(x))$ defines a measurable function on $X$

>The key to this proof is that an open set in $\R^2$ is a cartesian product of subsets of $\R^1$ that are themselves open.  I should come back here and try to work out if $\R$ is really neccesary or if replacing $\R$ with any topological space and product space would work.

### Correlaries

1. A complex function is measurable if and only if its real and imaginary parts are measurable
2. if $f$ and $g$ are complex measureable functions then $|f|$, $f+g$, and $f g$ are measurable
3. If $f$ is a complex measureable function on $X$ there is a complex measurable function $\alpha$ on $X$ such that $|\alpha|=1$ and $f=\alpha|f|$
4. The Characteristic function is measurable on measurable sets

## **Borel Set**

The *Borel sets* of  $(X,\mathcal{T}_X)$ are given $\mathscr{B}_{\mathcal{T}_X}:=\bigcap \big\{\mathfrak{M} \in  \Omega_X  \ : \ \mathcal{T}_X \subset \mathcal{T}_X \cap \mathfrak{M}  \big\}$

A mapping is *Borel measurable* if it is a measurable on its Borel set.

## Properties of Borel Sets

1. $\mathscr{B}_{\mathcal{T}_X}$ is a $\sigma$-algebra on $X$
2. $\mathscr{B}_{\mathcal{T}_X}$ contains $\mathcal{T}_X$
3. All other $\sigma$-algebras that contain $\mathcal{T}_X$ contain $\mathscr{B}_{\mathcal{T}_X}$
4. Continuous mappings are Borel measurable

To prove these properties we prove the following more general statement (above follows for $\mathscr{F}:=\mathcal{T}_X$)

### Borel Properties Lemma

Let $\mathscr{F} \subset \mathcal{P}(X)$  Then there is some $\sigma$-algebra $\mathfrak{M}^*$ such that

$$\mathscr{F} \subset \mathfrak{M}^* \subset \mathfrak{M}$$

for all possible $\mathfrak{M}$ $\sigma$-algebras in $X$ containing $\mathscr{F}$

$\underline{Proof}$

Since $\mathcal{P}(X)\in \big\{\mathfrak{M} \in  \Omega_X  \ : \  \mathscr{F} \subset \mathcal{X} \cap \mathfrak{M} \big\}$ we know $\mathscr{F} \in \mathfrak{M}^* := \bigcap \big\{\mathfrak{M} \in  \Omega_X  \ : \ \mathscr{F} \subset \mathscr{F} \cap \mathfrak{M}  \big\}$.  By its definition $\mathfrak{M}^*$  contains all possible $\sigma$-algebras in $X$ containing \mathscr{F}.  Hence we need only prove it is itself a $\sigma$-algebra.  Notice any collection of sets that form a subset of $\mathfrak{M}^*$ must be contained in all $\sigma$-algebras on $X$ containing $\mathscr{F}$ and hence any $\sigma$-algebra operation you could do on that collection would be contained in all $\sigma$-algebras on $X$ containing $\mathscr{F}$, and hence would be contained in the their intersection (i.e. $\mathfrak{M}^*$).  

## Properties of mappings from measurable spaces

For $(X,\mathfrak{M}_X)$, $(Y,\mathcal{T}_Y)$, and $f : X \to Y$

1. $\Big\{ E \in \mathcal{P}(Y) \ : \ f^{-1}(E) \in \mathfrak{M}_X \Big\}$ is a $\sigma$-algebra in $X$
2. if $f$ is measurable then $\bigcup_{E \in \mathscr{B}_{\mathcal{T}_Y}}$ $f^{-1}(E)$ $\subset \mathfrak{M}_X$
3. For Y=$[-\infty,\infty]$, if $\{f^{-1}((\alpha,\infty)) \subset X \ : \ \alpha \in \R \}$ $\subset \mathfrak{M}_X$ then $f$ is measurable
4. Borel mapping composition preserves measurability

$\textit{Proof}$

## **Upper and Lower Limits**

For $a : \N \to [-\infty,\infty]$

$$\beta:=\limsup_{k \to \infty} a_k:= \lim_{n \to \infty} \ \sup \{a(m)  \ : \ m > n \}$$
$$\alpha:=\liminf_{k \to \infty} a_k:= \lim_{n \to \infty} \ \inf \{a(m)  \ : \ m > n \}$$

For $f : \N \to \mathcal{F}(X \to [-\infty,\infty])$

$\sup_{n} f_n$ is the function that maps

$$x \mapsto \sup ( \{f_n(x) \ : \  n \in \N \})$$

$\limsup_{n \to \infty} f_n$ is the function that maps

$$x \mapsto \lim_{m \to \infty} \sup ( \{f_n(x) \ : \  n > m \})$$

## **Pointwise limit**

For $f : \N \to \mathcal{F}(X \to [-\infty,\infty])$ if

$$f(x)=\lim_{n \to \infty} f_n (x)$$

Then $f$ is the pointwise limit of $\{f_n\}$ assuming $f_n(x)$ converges for all $x \in X$

## limsups preserve measurability

$\underline{Proof}$

need

## **Measures and Measure Space**

A function $f : X \to Y$ is **countably additive** if $\forall A \in \mathcal{F}(\N \to X)$

$$f(\bigcup_{i=0}^\infty A_i)=\sum_{i=0}^\infty f(A_i)$$

When all $A(\N)$ are disjoint

A function $f : X \to Y$ is **finitely additive** if $\forall n \in \N$ and $\forall A \in \mathcal{F}(\N \to X)$

$$f(\bigcup_{i=0}^n A_i)=\sum_{i=0}^n f(A_i)$$

When all $A(\N)$ are disjoint

A **positive measure** is a function $\mu: \mathfrak{M}_X \to [0,\infty]$ such that it is *countably additive*

A **complex measure** is a function $\mu: \mathfrak{M}_X \to \mathbb{C}$ such that it is *countably additive*

A **measure space** is a measurable space with a positive measure defined its $\sigma$-algebra

## Elementary Properties of Positive Measure

For measurable space $(X,\mathfrak{M}_X)$ and positive measure $\mu : \mathfrak{M}_X \to [0,\infty]$

1. $\mu (\emptyset)=0$
2. $\mu$ is finitely additive
3. For $A,B \in \mathfrak{M} \quad A \subset B \rightarrow \mu(A) \leq \mu(B)\quad$ (called **monotonicity**)
4. $\lim_{n \to \infty} \mu (\bigcup_{m=0}^n A_m)=\mu(\lim_{n \to \infty} \bigcup_{m=0}^n A_m)$
5. $\lim_{n \to \infty} \mu (\bigcap_{m=0}^n A_m)=\mu(\lim_{n \to \infty} \bigcap_{m=0}^n A_m)$ when $\mu(A_0)$ is finite

$\underline{Proof}$

need

## The Counting Measure and The Unit Mass

$\mu : \mathcal{P}(X) \to [0,\infty]$
defined

$$\mu(E)=\begin{cases} \textrm{card}(E) & \textrm{card}(E)<\aleph_0 \\ \infty & \textrm{card}(E) \geq \aleph_0\end{cases}$$

Gives the **counting measure** on $X$

For some $x_0 \in X$ we say $\mu : \mathcal{P}(X) \to [0,\infty]$
defined

$$\mu(E)=\begin{cases} 1 & x_0 \in E \\ 0 & x_0 \notin E \end{cases}$$

is the **unit mass** *concentrated at $x_0$*

## Arithmetic on $[0, \infty]$

We define

$a + \infty=\infty + a:=\infty$

and

$a\cdot \infty=\infty \cdot a:=\begin{cases} \infty & 0 < a < \infty \\ 0 & a=0 \end{cases}$

Defining Arithmetic on $[0, \infty]$ as such is communtative, associative, and satisfies the distributive laws.

The following modifications to the cancellation laws hold

1. When $a < \infty, \quad a+b=a+c \rightarrow b=c \lor a < \infty$

2. When $0 < a < \infty, \quad ab=ac \rightarrow b=c$

## **Simple Function**

$s : (X,\mathfrak{M}_X) \to \mathbb{C}$ is a simple function provided the cardinality of $s(X)$ is finite.

The set of all such simple functions is given $\mathfrak{S}_{X \to \mathbb{C}}$

## Simple functions can approximate measurable functions

For $(X,\mathfrak{M}_X)$ and measurable $f : X \to [0,\infty]$  There exists $\mathfrak{s} \in \mathcal{F}(\N \to \mathfrak{S}_{X \to [0,\infty]})$ such that  

1. $\forall n \in \N \quad 0 \leq \mathfrak{s}_n \leq \mathfrak{s}_{n+1}$
2. $f$ is the poinwise limit of $\mathfrak{s}_n$

Note that when we write an inequality between two functions, this implies that the inequality holds on the output of the two function whenever the functions are evaluated on a common element of their domain.

$\underline{Proof}$

need

## Integration of Positive Functions

The **Integral** of a measurable simple function $s : X \to [0,\infty]$ is defined

$$\int_E s \ d\mu = \sum_{\alpha \in s(X)} \alpha\cdot \mu(E \cap s^{-1}(\alpha))$$

The **Lebesgue Integral** of a measurable function $f : X \to [0,\infty]$ is defined

$$\int_E f \ d\mu = \sup \{ \int_E s \ d\mu \ : \ s \in \mathfrak{S}_{X \to [0,\infty]} \ \land \ 0 \leq s \leq f \}$$

## Elementary Properties of the Lebesgue Integral

The Following follow immediately from out definitions of the *Lebesgue integral*

1. $0 \leq f \leq g \implies \int_E f \ d \mu \leq \int_E g \ d \mu$
2. $A \subset B \land f \geq 0 \implies \int_A f \ d \mu \leq \int_B f \ d \mu$
3. $\forall c \in \R \quad f \geq 0 \implies c \cdot \int_E f \ d \mu = \int_E c \cdot f \ d \mu$
4. $\forall x \in E \quad f(x)=0 \implies \int_E f d \mu =0$
5. $\mu(E)=0 \implies \int_E f d \mu =0$
6. $f \geq 0 \implies \int_E f d \mu = \int_X \bm{1}_E \cdot f d \mu$

## **Lebesgue's Monotone Convergence Theorem**

Let $\{f_n\}$ be a sequence of measurable functions on $X$ that converge pointwise to $f$ and

$$\forall n \in \N \quad \forall x \in X \quad 0 \leq f_n(x) \leq f_{n+1}(x)$$

Then $f$ is measurable and as $n \to \infty$

$$ \int_X f_n d \mu \to \int_X f d \mu $$

$\underline{Proof}$

Need

## Correlaries of Lebesgue's Monotone Convergence Theorem

Let $\{f_n\}$ be a sequence of measurable functions on $X$ that converge pointwise then

$$\int_X \lim_{n \to \infty} f_n d \mu = \lim_{n \to \infty}\int_X f_n d \mu$$

## Fatou's Lemma

## A Theorem

## Lebesgue integrable functions

Let $\mu$ be a positive measure on $(X,\mathfrak{M}_X)$.  Then

$L^1(\mu):=\Big\{ f \in \mathcal{F}(X \to \mathbb{C}) \ : \ f \text{ is measurable } \ \land \ \int_X|f|d\mu < \infty \Big\}$

and we call the set $L^1(\mu)$ **Lebesgue Integrable** *functions*

## Integral of Complex Functions

for measurable $u,v \ : \ X \to \R$ if $f=u+v_i$ and $f \in L^1(\mu)$ we define

$$
\int_E f d \mu = \int_E u^+ d \mu - \int_E u^- d \mu + \int_E iv^+ d \mu - \int_E iv^- d \mu
$$

## Linearity of the Integral on $L^1(\mu)$

for $f, g \in L^1 (\mu)$ and $\alpha,\beta \in \mathbb{C}$ $\alpha f + \beta g \in L_1(\mu)$ and

$$\int_X (\alpha f + \beta g) d \mu = \alpha\int_X f \ d \mu  + \beta \int_X g \ d \mu $$

## Integrals and Absolute Values

If $f \in L^1(\mu)$

$$\bigg| \int_X f d \mu \bigg| \leq \int_X | f | d \mu$$

### Lebesgue's Dominated Convergence Theorem

Suppose $f_n$ is a sequence of complex measureable function on $X$ that converges pointwise to $f$.  If there is some $g \in L^1(\mu)$ such that

$$\forall x \in X \quad \forall n \in \N \quad |f_n(x)| \leq g(x)$$

then $f \in L^1(\mu)$ and

$$\lim_{n \to \infty} \int_X f_n d \mu = \int_X f d \mu$$

$\underline{Proof}$

Need

## Almost Everywhere

A property $P$ holds **almost everywhere** (abreviated a.e.) on $E$ provided it holds on $E - N$ where $\mu(N)=0$

## Measures can be completed

## Correlary

Suppose $\{f_n\}$ is a sequence of complex measureable functions defined a.e. on $X$ such that

$$\sum_{n=1}^\infty \int_X |f_n| d \mu < \infty$$

Then the series

$$f(x)= \sum^{\infty}_{i=0} f_n (x)$$

converges for almost all $x$, $f \in L^1(\mu)$ and

$$\int_X f d \mu = \sum_{n=1}^\infty \int_X f_n d \mu$$

$\underline{Proof}$

Need

## Instances of Almost Anywhere

1. For measurable function $f \ : \ X \to [0,\infty]$, $E \in \mathfrak{M}_X$ with $\int_E f d \mu=0$, $f=0$ a.e. on $E$
2. $f \in L^1(\mu)$ and $\forall E \in \mathfrak{M} \quad \int_E f d \mu=0$.  Then $f=0$ a.e. on $X$
3. Suppose $f \in L^1(\mu)$ and $\Big|\int_X f d \mu \Big| = \int_X |f|d \mu$ then there is a constant $\alpha$ such that $\alpha f =|f|$

$\underline{Proof}$

Need

## A set containing all average values must contain almost all values

Suppose $\mu(X)<\infty$, $f \in L^1(\mu), S \subset \mathbb{C}$ and for all $E \in \mathfrak{M}$

$$\Bigg(\frac{1}{\mu (E)} \int_E f \  d \mu \Bigg) \in \bar{S}$$

Then $f(x) \in S$ for almost all $x \in X$

## Borel–Cantelli lemma

For $E \in \mathcal{F}(\N \to \mathfrak{M}_X)$

$$\sum_{k=0}^\infty \mu (E_k) < \infty \quad \rightarrow \quad \mu(\bigcap_{n=0}^\infty \bigcup_{m\geq n}^\infty E_n)=0$$

$\underline{Proof}$

Need