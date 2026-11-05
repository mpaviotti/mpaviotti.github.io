---
layout: archive
permalink: /projects/
title: Projects
---


## Projects for Computer Scientists

### Graded Monads for Efficient Database Implementations 
Functional programming languages such as Haskell make it easy to express
database queries using list comprehensions. For instance, the SQL query

`SELECT name, amount
FROM customers, invoices
WHERE cid = cust AND due < today`

can be written in Haskell as the following one-liner:


`[ (c.name, i.amount) |c ←customers, i ←invoices, c.cid i.cust, i.due < today ]`

This approach is highly convenient: monads allow us to concisely express fairly
complex operations over lists. However, this simplicity comes at a cost—such
implementations are often inefficient. A more performant alternative to lists is to use
indexed tables, which can be viewed as finite functions of type `Key ->
[Value]`. While this representation improves efficiency, it sacrifices the
ability to compose queries elegantly using monads.

This project will address this trade-off by implementing an efficient database
representation based on **graded monads**, thereby retaining compositionality
while improving performance.

### Quantum Functional Programming
This project investigates the design and implementation of a purely functional
domain-specific language for quantum programming, grounded in category-theoretic
semantics. Quantum circuits are represented as typed morphisms—e.g. `Hadamard ::
Qubit ⟶ Qubit` and `CNOT :: (Qubit ⊗ Qubit) ⟶ (Qubit ⊗ Qubit)` --- with
sequential and parallel composition expressed via categorical operators `(∘)`
and `(⊗)`. 

By leveraging linear or affine typing (possibly with the use of modal types),
the language enforces core quantum constraints such as no-cloning and
no-deleting at compile time, ensuring correct usage of quantum data by construction.

Selected circuits and algorithms developed in the DSL (e.g. Bell states,
teleportation, or Grover-style oracles) are reimplemented as exercises in
Quipper, enabling a comparative evaluation of expressiveness, safety guarantees,
and programmer effort. The project will delvier an executable prototype capable
of simulating or compiling circuits, illustrating how  structure in functional
programming together yield expressive, principled, and statically safe
abstractions for quantum computation.

### Reactive Dashboard with Functional Reactive Programming
Functional Reactive Programming (FRP) is a programming paradigm commonly used in
applications that involve time-varying or event-driven data, such as:
- Graphical User Interfaces (GUIs): handling interactive components like buttons, sliders, and animations.
- Games and simulations: managing continuously changing game states and reactive events.
- Robotics and embedded systems: controlling sensors and actuators in real-time.
- Financial or IoT dashboards: updating displays in response to live data streams.
- Audio/video processing: modeling signals and effects that change over time.

The goal of this project is to build a small interactive dashboard that responds
in real-time to multiple input streams, leveraging libraries such as Reflex or reactive-banana. The dashboard
may react to dynamic data --- such as simulated sensor readings, stock prices,
or game statistics --- which updates automatically as the underlying signals
change. The project should demonstrate compositional event handling, including
the creation of derived signals that combine multiple inputs and the detection
of complex events, such as threshold crossings. 

### OS Development and Weak Memory 
Markix is an operating System is a bare bone operating system for x86
architectures written in Assembly and C and runs on x86 or the [bochs
emulator](https://bochs.sourceforge.io). The task is to implement a spin lock in
assembly x86 relying on the optimisations of the TSO memory model provided by
the x86 architecture.  Another option is to rewrite this for the Apple M-series
chip, but you will have to provide a justification for the correctness of the
implementation since the ARM model is weaker than the Intel's one. 

Visit my GitHub [page](https://github.com/mpaviotti/Markix). 


### Other Projects B.Sc. and M.Sc. Projects for Computer Scientists
 
- Efficient Analysis of Chess games
- Buffer Overflow Analysis
- Kernel Hacking: Security, Hypervisors


## Projects for Mathematicians
I am happy to supervise theses in category theory, abstract algebra and
topology, particularly where these subjects connect with computability theory.

### Recursion and Induction in a Topos via Adjunctions 
A topos is a category that shares many features with the category of sets. In
particular, each object $$X$$ has a power object $$\mathcal{P}(X)$$, analogous to a
power set, which is isomorphic to the object of maps $$X \to \Omega$$, where $$\Omega$$ is the object of truth values.

Toposes support higher-order logic and provide an induction principle based on
the natural numbers. This project aims to study other forms
of induction systematically and proving them correct.

### Diagonalisation Arguments and Fixed-Point Theorems  
From Cantor’s theorem onwards, diagonalisation has been used to establish
fundamental limits in logic and computer science. Famous examples include
Russell’s paradox, Gödel’s incompleteness theorems and Turing’s halting problem.

Lawvere’s fixed-point theorem gives a categorical framework that connects many
diagonal arguments, self-reference paradoxes and limit theorems in logic and
mathematics.

The aim is to expand on other kinds of diagonal arguments outside the scope of computability. 
