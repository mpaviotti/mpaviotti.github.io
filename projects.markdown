---
layout: archive
permalink: /projects/
title: Projects
---


## Undergrad Projects for Computer Scientists

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

### OS Development
Markix is an operating System I developed when I was little. It is a bare bone
operating system for x86 architectures written in Assembly and C and runs on x86
or the [bochs emulator](https://bochs.sourceforge.io). The idea is to have
something more minimal than Minix so that students can understand every
component of an operating system in isolation. Hence, Markix is built in
incremental stages. Each milestone corresponds to a Git tag, and improvements to
that module are developed on dedicated branches.

| Tag          | Component         | Description                                                                 |
|--------------|-------------------|-----------------------------------------------------------------------------|
| Bootloader   | Bootloader        | Initializes the CPU in real mode, loads the kernel, and switches to protected mode |
| Interrupts   | Interrupt System  | Implements the 8259 PIC, IDT setup, and interrupt service routines (ISRs) |
| Keyboard     | PS/2 Driver       | Handles keyboard input and interrupt handling                               |
| Scheduler    | Process Scheduler | Round-robin scheduling and context switching                                |
| Paging       | Memory Management | GDT, paging tables, and memory protection setup                             |
| FilesystemGRUB | File System     | Basic FAT filesystem and GRUB integration                                   |


Download the source code from my GitHub [page](https://github.com/mpaviotti/Markix). 
Software needed: NASM Compiler, C Compiler with support for cross compiling to i386 architectures, Bochs, GNU Debugger (gdb).


### Weak Memory Concurrency
Amongst other things I also helped the weak memory concurrency community in fixing some problem with the C++ and Java concurrency model.

The work which we published at [ESOP'20'](https://link.springer.com/content/pdf/10.1007/978-3-030-44914-8_22.pdf)
is being considered for the next ISO standard of C++. 
- Link to the draft [here](https://graymalk.in/iso-papers/p1780/p1780r2.html)
- Link to the WG21 discussion [here](https://eur01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgithub.com%2Fcplusplus%2Fpapers%2Fissues%2F554%23issuecomment-1311093994&amp;data=05%7C01%7CM.Paviotti%40kent.ac.uk%7C5e1fff970b0a4039205008dac71af6b3%7C51a9fa563f32449aa7213e3f49aa5e9a%7C0%7C0%7C638041215860503967%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&amp;sdata=V1PRIBvid5UxHNvEI2aOq2Rp4Sq9voNbcjb5rCEJ4sk%3D&amp;reserved=0)
- The WG21 group page: [https://isocpp.org/wiki/faq/wg21](https://isocpp.org/wiki/faq/wg21)
- The MRD Web Tool [link](https://www.cs.kent.ac.uk/projects/MRDer/)

### Other Projects B.Sc. and M.Sc. Projects for Computer Scientists
 
- Efficient Analysis of Chess games
- Buffer Overflow Analysis
- Kernel Hacking: Security, Hypervisors


## Undergrad topics for Mathematicians
TBA. 
