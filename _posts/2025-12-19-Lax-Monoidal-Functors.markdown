---
title:  "On Lax Monoidal Functors" 
date:   2025-12-19 21:17:21 +0000
permalink: /posts/2025/12/Lax-Monoidal-Functors/
tags:
  - monoids
  - categories
  - monads
---

What is the difference between 
- a lax monoidal functor 
- a monoid in a Day-monoidal category
- a morphism of lax-algebras for the free monoid 2-monad, and 
- a codistributive law with the tensor product?

*Well, None. Let's see why*. 

To keep this post as concise as humanly possible I will assume knowledge of (symmetric)[monoidal categories](https://ncatlab.org/nlab/show/monoidal+category), [kan extensions](https://ncatlab.org/nlab/show/Kan+extension) and [enriched categories](https://ncatlab.org/nlab/show/enriched+category).

We show informally the following proposition. 

**Proposition.**
Let
$$
(\mathcal{C}, \otimes_{\mathcal{C}}, I_{\mathcal{C}})
$$
be a small monoidal closed category enriched in a monoidal closed category 
$$
(\mathcal{D}, \otimes_{\mathcal{D}}, I_{\mathcal{V}})
$$
 and let
$$
F : \mathcal{C} \to \mathcal{D}
$$
be a functor. The following statements for $$F$$ are equivalent:

1. It is a lax monoidal functor
2. It is a monoid in the monoidal category
   $$
   ([\mathcal{C}, \mathcal{D}], \otimes_\text{Day}, y(I_{\mathcal{C}}))
   $$
3. It is a homomorphism of lax algebras for the free monoid 2-monad
4. It is a $$\mathbb{N}$$-indexed family of (co)distributive laws for a functor $$F : \mathcal{C} \to \mathcal{C}$$
   
   $$
   \text{Nat}(\otimes^{n} \circ F^{n}, F \circ \otimes^{n})
   $$
   
   where
   $$
   \otimes^{n} : \mathcal{C}^{n} \to \mathcal{C}
   $$

Let us assume the hypothesis of the proposition.

**Proof(Sketch).** 
(1) $$\Leftrightarrow$$ (2).

A *lax
monoidal functor* is a functor which lax-preserves the monoidal structure of $$
\mathcal{C}$$ that is, there is a morphism

$$ u : I_{\mathcal{D}} \to F I_{\mathcal{C}} $$ 

and a family of morphisms

$$\circledast_{X,Y} : F X \otimes_{\mathcal{D}} F Y \to F (X \otimes_{\mathcal{C}} Y)$$

indexed by $$X,Y$$ and natural therein, subject to some [coherence conditions](https://ncatlab.org/nlab/show/monoidal+functor). 

On the other hand, the *Day convolution* provides a natural way to define a
monoidal structure on the category of functors.  In other words, the task is to
turn the category of functors $$[\mathcal{C}, \mathcal{D}]$$ into a monoidal
category by equipping it with a tensor product and a unit. Hence, for two
functors
$$
F, G : \mathcal{C} \to \mathcal{D}
$$
the Day convolution $$\otimes_\text{Day}$$ is defined as follows:

$$
\begin{align*}
(F \otimes_\text{Day} G) C & := \int^{X,Y \in \mathcal{C}} \mathcal{C}(X \otimes_{\mathcal{C}} Y, C) \otimes_{\mathcal{D}} F X \otimes_{\mathcal{D}} G Y\\
    & = \text{Lan}_{\otimes_{\mathcal{C}}}(\otimes_{\mathcal{D}} \circ F \times F)
\end{align*}
$$

while the unit of $$[\mathcal{C}, \mathcal{D}]$$ is given by the Yoneda embedding applied to
the unit $$I_\mathcal{C}$$ that is $$y(I_\mathcal{C}) = \mathcal{C}(I_\mathcal{C},-)$$.

Now, a monoid in $$([\mathcal{C}, \mathcal{D}], \otimes_\text{Day}, y(I))$$ is called a Day-monoid. This is a functor
$$
F : \mathcal{C} \to \mathcal{D}
$$
together with a unit and multiplication map.

- The __unit map__
$$
\eta : y(I) \to F
$$
is obtained from the unit of the lax monoidal functor (and viceversa) via the enriched Yoneda lemma

$$
\text{Nat}(y(I), F) \cong \mathcal{D}(I_{\mathcal{D}}, F(I_{\mathcal{C}}))
$$

- The __multiplication map__ 
$$
\mu : F \otimes_{\text{Day}} F \to F
$$
is obtained from $$\circledast$$ (and viceversa) by using the adjunction $$\text{Lan}_J \dashv - \circ J$$ as follows 

$$
\text{Nat}(\text{Lan}_{\otimes_\mathcal{C}}(\otimes_\mathcal{D} \circ F \times F), F)
\cong
\text{Nat}(\otimes_\mathcal{D} \circ F \times F, F \circ \otimes_\mathcal{C})
$$

It remains to prove that the laws of the unit and multiplication of the monoid  imply
the lax monoidal properties of $$u$$ and $$\circledast$$ (left as exercise to the reader).

$$(2) \Leftrightarrow (3)$$. 

This is a rather easy statement which generalises the free monoid construction to 2-categories.

In particular, the cheapest way of turning a set $$A$$ into a monoid is to take the set of words over $$A$$, namely $$A^*$$. This is the free monoid over $$A$$ where the empty word is the unit and concatenation is the multiplication of the monoid. The Eilenberg-Moore algebras of $$A^*$$ are equivalent to the algebraic structure of the monoid $$A^*$$.  
In particular, the category of Eilenberg-Moore algebras over $$A^*$$ is
equivalent to the category of monoids 

$$
\mathcal{C}^{A^*} \simeq \textbf{Mon}
$$

Similarly, given a category $$\mathcal{C}$$, the cheapest way of turning this category into a monoid (a monoidal category) is to send $$\mathcal{C}$$ to the category of finite sequences of objects $$(A_1, \dots, A_n)$$ and componentwise sequences of morphisms in $$\mathcal{C}$$. 
In other words, $$T$$ is the free monoid 2-monad in $$\textbf{Cat}$$ defined as the $$\mathbb{N}$$-coproduct $$\mathcal{C}^n$$, that is 

$$
  T\mathcal{C} = \sum_{n : \mathbb{N}} \mathcal{C}^{n}
$$

Now, similarly to what happens in the 1-category case, we have the following equivalence 

$$
\textbf{Cat}^T \simeq 2\text{-Mon}
$$

where $$\textbf{Cat}^T$$ is the 2-category of algebras for a 2-monad $$T$$ and $$T$$-algebra homomorphisms and $$2$$-Mon is the 2-category of monoidal categories and monoidal functors (monoids in $$\textbf{Cat}$$). Hence (lax) $$T$$-algebra homomorphisms are (lax) monoidal functors. 


$$(3 \Leftrightarrow 4)$$.

Clearly, if $$T$$ is the free monoid 2-monad, an algebra for  $$T$$ is a map 

$$a : \sum_{n : \mathbb{N}} \mathcal{C}^n \to \mathcal{C}$$

The previous point states that this is a monoidal category where $$A \otimes_\mathcal{C} B := a (A,B)$$ and $$I_\mathcal{C} = a()$$, thus $$a$$ sends $$(A_1, \dots, A_n)$$ to $$A_1 \otimes_\mathcal{C} \dots \otimes_\mathcal{C} A_n$$.

A lax monoidal functor $$F$$ is a lax $$T$$-algebra homomorphism, thus it has to satisfy

$$F(A_1) \otimes_\mathcal{D} \dots \otimes_\mathcal{D} F(A_n) \to F(A_1 \otimes_\mathcal{C} \dots \otimes_\mathcal{C} A_n)$$

which is defined at all $$n$$ and $$A_i$$ hence it is a (co)distributive law

$$ \text{Nat}(\otimes^{n}_{\mathcal{D}} \circ F^{n}, F \circ \otimes^{n}_{\mathcal{C}})$$

