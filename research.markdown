---
layout: archive
permalink: /research/
title: Research
---

My research is based on the idea that `Mathematical Logic`, `Type Theory` and
`Category Theory`  are essentially "three sides" of the same coin.

This is made formal via the **denotational interpretation** which is a
mathematical  interpretation of a programming language using an algebraic
structure such as that of category theory.

This trinitarianistic view of computer science connects very neatly to programming languages and computability, and has found several **applications** to **formal methods**, **functional programming**, **quantum computing**, **AI** and **databases**.   

## Possible PhD Topics
Below you can find a non-comprehensive list of PhD topics I'd be happy to supervise: 

- **Guarded type theory**
Guarded Type Theory (GTT) extends type theory with a delay (or later) modality
that internalises the notion of contractivity familiar from metric semantics. By
enforcing productivity and well-foundedness through the type system, GTT
provides a principled framework for reasoning about coinductive definitions and
it has found several important applications; for denotational semantics of
languages with recursion ([Paviotti,
2016](https://mpaviotti.github.io/assets/papers/paviotti-phdthesis.pdf)), for
models of *functional reactive programming* (FRP) ([Krishnaswami & Benton,
2011](https://www.cl.cam.ac.uk/~nk480/frp-lics11.pdf)), for models of
higher-order store ([Birkedal et al](https://cs.au.dk/~birke/papers/sgdt-conf.pdf)). 

You can find more information here: 
    - [Guarded Type Theory](https://ncatlab.org/nlab/show/synthetic+guarded+domain+theory) 
    - [Guarded Recursion](https://ncatlab.org/nlab/show/guarded+recursion). 

 

- **Functional Programming**
Functional programming has long been closely connected to abstract mathematics.
Since the turn of the century, this connection has been further strengthened
through the systematic application of category-theoretic ideas to typed
functional languages. A key insight was the observation that a functor can be
understood, in programming terms, as a parameterised type equipped with a
canonical map operation. Building on this idea, category theory has been applied
in several directions, including *generic
programming* ([Hinze et al.](https://www.cs.ox.ac.uk/ralf.hinze/LN.pdf)),
*relational algebra* ([Gibbons &
Hinze](https://www.cs.ox.ac.uk/jeremy.gibbons/publications/reladj.pdf)), *formal
reasoning* ([Danielsson et
al.](https://www.cs.ox.ac.uk/jeremy.gibbons/publications/fast+loose.pdf)). 

You can find more information about recursion schemes here: [Recursion Schemes](https://ncatlab.org/nlab/show/recursion+scheme)
 
- **Coalgebraic Semantics**
Coalgebraic semantics provides a uniform, abstract framework for modelling the
dynamic behaviour of computational systems. In this approach, the behaviour of a
system is represented as a coalgebra for a functor that specifies the shape of
observable transitions, such as state evolution, input/output, or
nondeterminism. This perspective naturally supports coinductive reasoning
principles, including *bisimulation* and *behavioural* equivalence, and applies
uniformly to a wide range of systems, from transition systems and automata to
programming language semantics and *reactive systems*. *Structural operational semantics* (SOS) is a particular kind of coalgebraic semantics firstly pioneered by [Plotkin](https://homepages.inf.ed.ac.uk/gdp/publications/Origins_SOS.pdf).  The biagebraic framework ([Turi & Plotkin](https://homepages.inf.ed.ac.uk/gdp/publications/Math_Op_Sem.pdf)) which was thoroughly expounded by [Klin](https://www.sciencedirect.com/science/article/pii/S0304397511002532) is a way of ensuring modular reasoning. 
This kind of semantics hasbeen used for reinforcement learning (RL) by [Mahadevan](https://arxiv.org/abs/2508.15128). 
  
 
