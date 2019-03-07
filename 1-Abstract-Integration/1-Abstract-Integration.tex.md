# Abstract Integration

### **Topological Space**
Let $\mathcal{T}_X \subset \mathcal{P}(X)$.  Then $(X,\mathcal{T}_X)$ is a **topological space** $\iff$
1. $\emptyset , X \in \mathcal{T}_X$
2. $\forall I_n \in \mathcal{F}\big(\Z^+ \to \mathcal{T}_X\big)\quad\bigcap_{n=1}^\infty I_n \in \mathcal{T}_X$
3. $\forall U \in \mathcal{P}(\mathcal{T}_X)\quad \bigcup_{u \in U} u \in  \mathcal{T}_X$

$\mathcal{T}_X$ is a **topology** and $\mathscr{T}_X$ is the *family of topologies* on $X$.

For $(X,\mathcal{T}_X)$ and $(Y,\mathcal{T}_Y)$, we say a function $f : X \to Y$ is **continuous** when $\bigcup_{V \in \mathcal{T}_Y}\{f^{-1}(V)\} \subseteq \mathcal{T}_X$.  Equivalently we write $f \in \mathcal{C}(X \to Y)$

Locally, we can say $g : X \to Y$ is *continuous at the point* $x_0$ provided every neighborhood of $g(x_0)$ contains the image of a neighborhood of $x_0$.  It can be proven that a function is continous if and only if it is continuous at all points.


### **Measurable Space**
##### *Rudin's Minimal Definition*
Let $\mathcal{M}_X \subset \mathcal{P}(X)$.  Then $(X,\mathcal{M}_X)$ is a measurable space $\iff$
1. $X \in \mathcal{M}_X$
2. $\forall A_n \in \mathcal{F}\big(\Z^+ \to \mathcal{M}_X\big)\quad \bigcup_{n=1}^\infty A_n \in \mathcal{M}$
3. $\forall C \in \mathcal{M}_X \quad C^c \in  \mathcal{M}_X$

##### *Working Maximal Definition*
Let $\mathcal{M}_X \subset \mathcal{P}(X)$.  Then $(X,\mathcal{M}_X)$ is a measurable space $\iff$
1. $\emptyset , X \in \mathcal{M}_X$
2. $\forall A_n \in \mathcal{F}\big(\Z^+ \to \mathcal{M}_X\big)\quad\bigcap_{n=1}^\infty A_n,\bigcup_{n=1}^\infty A_n \in \mathcal{M}$
3. $\forall A,B \in \mathcal{M}_X \quad A-B \in  \mathcal{M}_X$

$\mathcal{M}_X$ a $\bm{\sigma}$**-algebra** and $\Omega_X$ is the *family of all $\sigma$-algebras* on $X$

For $(X,\mathcal{M}_X)$ and $(Y,\mathcal{T}_Y)$, we say a function $f : X \to Y$ is **measurable** when $\bigcup_{V \in \mathcal{T}_Y}\{f^{-1}(V)\} \subseteq \mathcal{M}_X$


#### Proposition

The composition of a continuous function with codomain $B$ and a continuous function with domain $B$ will be continuous and 

the composition of a measurable function with codomain $B$ and a continuous function with a codomain of B will be measurable


### **Metric Space**
Let $d : X \times X \to \R^+ \cup \{0\}$.  Then $(X,d) \text{is a metric space} \iff \forall x,y,z \in X$
1. $\infty> d(x,y) \geq 0$ (redundant as I defined the codomain already as such)
2. $d(x,y)=0 \iff x=y$
3. $d(x.y)=d(y,x)$
4. $d(x,z) \leq d(x,y)+d(y,z)$


#### Proposition
for $(X,\mathcal{M}_X)$ and $(Y,\mathcal{T}_Y)$, $u,v: X \to \mathbb{R}$ and $\Phi \in \mathcal{C}(\mathbb{R}^2 \to Y)$ 

Then $x \mapsto \Phi(u(x),v(x))$ defines a measurable function on X

##### Correlaries:
1. A complex function with measurable real and imaginary parts is measurable
2. if $f$ and $g$ are complex measureable functions then so are $\mathrm{Re}\circ f$, $\mathrm{Im}\circ f$, $|f|$ and $f+g$ and $f\circ g$
3. If $f$ is a complex measureable function on $X$ there is a complex measurable function $\alpha$ on $X$ such that $|\alpha|=1$ and $f=\alpha|f|$

### **Theorem: The Existence of Borel Sets**
Let $\mathcal{X} \subset \mathcal{P}(X)$  Then there is some $\sigma$-algebra $\mathscr{M}^*$ such that
$\mathcal{X}\subseteq \mathscr{M}^* \subseteq \bigcup_{M\in\Omega_X}$

##### Borel Set 
The Borel sets of  $(X,\mathcal{T}_X)$ are given $\mathscr{B}=\bigcup_{M\in\Omega_X} M$

##### *Skipped alot that needs to be filled in from this point on limsup, liminf and nity gritty integral machinery*

### **Measures**
1. A function is $\mu$ is **countably additive** if $\forall A \in \mathcal{F}(\N \to X)$ such that $A(\N)$ are disjoint $\mu(\bigcup_{i=1}^\infty A_i)=\sum_{i=1}^\infty A_i$
2. A **positive measure** is a function $\mu: \mathcal{M}_X \to [0,\R]$ such that it is *countably additive*
3. A **complex measure** is a complex-valued countably additive function defined on a $\sigma$-algebra

### **Lebesgue's Monotone Convergence Theorem**
A sequence of dominating functions that converges pointwise to some $f$
1. Is measurable
2. the limit of the integral values of the sequence converge to the integral of $f$

### Lebesgue integrable functions 
Let $\mu$ be a positive measure on an arbirary measurable space $X$

$L^1(\mu):=\Big\{ f \in \mathcal{F}(X \to \mathbb{C}) \ : \ \bigcup_{V \in \mathcal{T}_\mathbb{C}}\{f^{-1}(V)\} \subseteq \mathcal{M}_X \ \land \ \int_X|f|d\mu < \infty \Big\}$

### Lebesgue's Dominated Convergence Theorem
suppose $f_n$ is a sequence of complex measureable function on $X$ that converges pointwise to $f$ if there is some $g \in L^1(\mu)
