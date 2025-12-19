---
layout: archive
permalink: /projects/
title: Projects
---


## Operating System Development (OSDev)
*The Markix Operating System*  I developed when I was little. It is a bare bone operating system for x86 architectures written in Assembly and C and runs on x86 or the [bochs emulator](https://bochs.sourceforge.io). The idea is to have something more minimal than Minix so that students can understand every component of an operating system in isolation.  
Hence, Markix is built in incremental stages. Each milestone corresponds to a Git tag, and improvements to that module are developed on dedicated branches.

| Tag          | Component          | Description                                                                 |
|--------------|------------------|-----------------------------------------------------------------------------|
| Bootloader   | Bootloader        | Initializes the CPU in real mode, loads the kernel, and switches to protected mode |
| Interrupts   | Interrupt System  | Implements the 8259 PIC, IDT setup, and interrupt service routines (ISRs) |
| Keyboard     | PS/2 Driver       | Handles keyboard input and interrupt handling                               |
| Scheduler    | Process Scheduler | Round-robin scheduling and context switching                                |
| Paging       | Memory Management | GDT, paging tables, and memory protection setup                             |
| FilesystemGRUB | File System     | Basic FAT filesystem and GRUB integration                                   |


Download the source code from my GitHub [page](https://github.com/mpaviotti/Markix). 
Software needed: NASM Compiler, C Compiler with support for cross compiling to i386 architectures, Bochs, GNU Debugger (gdb).  


## ISO Standards for Weak Memory Concurrency
Amongst other things I also helped the weak memory concurrency community in fixing some problem with the C++ and Java concurrency model.

The work which we published at [ESOP'20'](https://link.springer.com/content/pdf/10.1007/978-3-030-44914-8_22.pdf))
is being considered for the next ISO standard of C++. 
- Link to the draft [here](https://graymalk.in/iso-papers/p1780/p1780r2.html)
- Link to the WG21 discussion [here](https://eur01.safelinks.protection.outlook.com/?url=https%3A%2F%2Fgithub.com%2Fcplusplus%2Fpapers%2Fissues%2F554%23issuecomment-1311093994&amp;data=05%7C01%7CM.Paviotti%40kent.ac.uk%7C5e1fff970b0a4039205008dac71af6b3%7C51a9fa563f32449aa7213e3f49aa5e9a%7C0%7C0%7C638041215860503967%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000%7C%7C%7C&amp;sdata=V1PRIBvid5UxHNvEI2aOq2Rp4Sq9voNbcjb5rCEJ4sk%3D&amp;reserved=0)
- The WG21 group page: [https://isocpp.org/wiki/faq/wg21](https://isocpp.org/wiki/faq/wg21)
- The MRD Web Tool [link](https://www.cs.kent.ac.uk/projects/MRDer/)

## B.Sc. and M.Sc. Projects for Computer Scientists
If you are looking for a project for your final year exam here are some, however, fair warning, these projects are not the fainted hearted: 
- Operating System Development (OSDev)
- Algorithms implementation 
- Efficient Analysis of Chess games
- Buffer Overflow Analysis
- Kernel Hacking: Security, Hypervisors


## B.Sc. and M.Sc. topics for Mathematicians
I can (and have) supervised mathematicians in the past who wanted to study some applications of group theory, abstract algebra and category to computer science and, in particular, programming languages. 
Feel free to reach out to me if interested. 
