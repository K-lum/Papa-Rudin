# Positive Borel Measures

## **Vector Space Definitions**

 $V$ is a vector space over field $F$ provided the binary operations of vector addition and scalar multiplication satisfy the following axioms

1. Associativity of addition
2. Commutativity of addition
3. Identity element of addition
4. Inverse elements of addition
5. Compatibility of scalar multiplication with field multiplication ($a(bv) = (ab)v $)
6. Identity element of scalar multiplication 1v = v, where 1 denotes the multiplicative identity in F.
7. Distributivity of scalar multiplication with respect to vector addition
8. Distributivity of scalar multiplication with respect to field addition

For Vector Space $V_1$ and $V_2$, A mapping $\Lambda \ : \ V_1 \to V_2$ is a **linear transformation** provided for any scalars $\alpha$,$\beta$

$$\Lambda(\alpha x+\beta y)=\alpha \Lambda x + \beta \Lambda y $$

For V a vector space over field F a linear mapping $\Lambda \ : \ V \to F$ is called a **linear functional**

A *linear functional* on a ordered vector space satisfying $x\geq 0 \rightarrow \Lambda x \geq 0$ is a **positive linear function**

## **Topological Definitions**

- *closed*, *closure*, *compact*,
- A *neighborhood* of $p \in X$ is any open set containing $p$
- $X$ is *Hausdorff* when distinct elements of $X$ have disjoint neighborhoods
- $X$ is *locally compact* when every point has a neighborhood with compact closure

## Basic Topology results

1. The closed subset of a compact set is compact
2. A subset of a set with compact closure has compact closure
3. Hausdorf somethhing
4. Compact subsets of Hausdorf spaces are closed
5. for closed $F$ and $K$ compact in a Hausdorff space $F \cap K$ is compact
6. Theorem
7. Theorem

## Upper and Lower semicontinuous

for topological space $X$ and Y either $\R$ or $[-\infty,\infty] \quad f \ : \ X \to Y$ is **upper semicontinuous** when

$$\bigcup_{\alpha \in \R} \Big\{\{x \ : \ f(x) < \alpha \}\Big\} \subset \mathcal{T}_X$$

and is **lower semicontinuous** when

$$\bigcup_{\alpha \in \R} \Big\{\{x \ : \ f(x) > \alpha \}\Big\} \subset \mathcal{T}_X$$

## The Support

$S$ is the *support* of a complex function $f$ on topological space $X$ if it is the closure of $\{x: f(x) \neq 0\}$

The collection of all continuous complex functions on $X$ whose support is compact is denoted by $C_c(X)$

## Several Theorems and Urysohn's Lemma

$$\text{If } X \text{ is locally compact and Hausdorf, and } K \text{ is compact with } K \subset V \in \mathcal{T}_X \text{then there is a function}$$

## The Riez Representation Theorem

## Regularity Properties of Borel Measures

Let $(X,\mathscr{B}_X,\mu)$ with $X$ locally compact and Hausdorff.  

If for $E \in \mathfrak{M}$, we have

$$\mu (E) = \inf \big\{ \mu(V) \ : \ E \subset V, V \text{ open } \big\}$$

Then $E$ is **outer regular**

If for $E$, we have

$$\mu (E) = \sup \big\{ \mu(K) \ : \ K \subset E, K \text{ compact } \big\}$$

Then $E$ is **inner regular**

If every Borel set in X is both outer and inner regular, $\mu$ is called **regular**

## $\sigma$-compact and $\sigma$-finite measure

A set $E$ in a topological space is called **$\sigma$-compact** if $E$ is a countable union of compact sets

A set $E$ in a measure space (with measure $\mu$) is said to have **$\sigma$-finite measure** if E is a countable union of sets $E_i$ of finite measure.

## Theorem 2.18

## Construct the Lebesgue measure

## Results of the Lebesgue measure

## Lusin's Theorem

## The Vitali-Caratheodory Theorem