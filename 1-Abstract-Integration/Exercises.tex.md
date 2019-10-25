# Chapter 1 Exercises

## #1

There is no countable $\sigma$-algebra.

## *proof*

1. Suppose FTSOC there is some countable $\sigma$-algebras $\big($call it $\mathfrak{M}_X \subseteq \mathcal{P}(X)$$\big)$
2. Consider the function $f : X \to \mathfrak{M}_X$ defined by $x \mapsto \bigcap_{x \in A \in \mathfrak{M}_X}$
3. Notice that $\forall x \neq y \in X \quad f(x) \cap f(y) = \emptyset$.  To see this we note that $x \in f(y)$ and $y \in f(x)$, because if this weren't the case $x \in f(x) / f(y) \subsetneq f(x)$ and $y \in f(y) / f(x) \subsetneq f(y)$ contradicting the definition of $f$.  Hence, $f(x)=f(x)\cap f(y)= f(y)$ and then $x=y$ contradictiong our assumption.
4. Since the sets of $f(X)$ are at least countable disjoint sets we see taking countable unions of sets from $f(x)$ (each distinct) we can form at least uncountably many elements that all must be contained in $\mathfrak{M}_X$ showing that $\mathfrak{M}_X$ cannot be countable.

## #2

Prove that For $(X,\mathfrak{M}_X)$ and $(Y,\mathcal{T}_Y)$, $u_1,u_2,\ldots u_n: X \to \mathbb{R}$ and $\Phi \in C(\mathbb{R}^n \to Y)$,
$x \mapsto \Phi\big(u_1(x),u_2(x),\ldots u_n(x)\big)$
 defines a measurable function on $X$

 Instead we show more generally that the product topology (also known as the Tychonoff topology) is 

## #3

