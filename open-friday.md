---
layout: splash
title: "MLIR (Un)School Meets UK Compiler Community"
excerpt: "Public Workshop - Fri, Sep 12 @ William Gates Building"
permalink: /open-friday/
header:
  overlay_color: "#000"
  overlay_filter: "0.5"
  overlay_image: /images/wgb.jpg
---

Join us for our Open Friday, titled **MLIR (Un)School Meets Compiler
Community**, on Friday 12th of September. This public workshop is the final
day of our MLIR (Un)School and offers an opportunity for our international MLIR
(Un)School attendees to connect with the UK compiler community.

**Note:** The MLIR (Un)School is a dynamic event → Our Schedule (for this Friday) evolves until and throughout the MLIR (Un)School.
{: .notice--info}

## Registration

[Please register](https://docs.google.com/forms/d/e/1FAIpQLSeRaSREk5sSVvNChBagRcR2R0c_-OpgR2EDHMXMKkyAl6hI1A/viewform?usp=header)! While attendance is free, your registration will help us
with catering and badge printing. (Un)School participants do not need to
register.

## Schedule | Friday, Sep 12th

| Time  |  Core Track                                                         |
|-----: |:------------------------------------------------------------------- |
|  9:30 | --- Arrival ---                                                     |
| 10:00 | Welcome                                                             |
| 10:15 | **Building an ecosystem around machine readable ISA specifications - Alastair Reid @ Intel** |
| | Specifications of Instruction Set Architectures (ISAs) lie at the heart of compilers: telling us what an instruction does and how to use it. They are also critical to activities like translation validation, binary translation, JITing, formal verification, binary lifting, OS implementation, and binary level security analysis. There are official specifications for both Arm and RISC-V (and, soon, for Intel Architecture) are publicly available but many projects that could use these specifications are not using the official, machine readable specifications. It has become clear that "if we build it, they will come" is not true. This talk will look at what is missing and what can be done to fill this gap and, in particular, how adopting MLIR can help with both the technical and ecosystem challenges. <br/> *Bio: Dr Alastair Reid is a Senior Principal Engineer at Intel Labs working at the intersection of formal verification, security, privacy, software, hardware, compilers, processor architecture and microarchitecture. For the last 15 years or so, his focus has been on creating high-quality machine readable formal specifications of computer architecture and using those specifications to support formal verification. Arm's formal specification was published in 2017 and Alastair hope to release Intel's formal specification soon.*
| 11:00 | **Scaling ML models with MLIR-based partitioners: an intro to Shardy + MPMD - Joel Wee @ Google DeepMind** |
| | As machine learning models grow to billions or even trillions of parameters, they can no longer fit onto a single accelerator. However, partitioning these models can be complicated, and there is often a tradeoff between research velocity and efficient hardware utilization. To this end, we have built Shardy and Shardy:MPMD, MLIR-based partitioning systems aimed at effortlessly partitioning these large ML models while retaining single-device programming semantics. <br> *Bio: Joel is a software engineer at Google DeepMind, working on compilers for ML performance – PartIR and Shardy:MPMD in particular. Prior to this, he worked on other non-compiler software (e.g. distributed computing, etc.).*
| 11:30 | -- Break -- |
| 12:00 | **TileIR: a New Programming Model for CUDA - Théo Degioanni & Lorenzo Chelini @ NVIDIA** |
||One of the key factors behind the success of the NVIDIA ecosystem is a frequently overlooked aspect of the hardware–software contract: forward compatibility. PTX, the intermediate instruction set for NVIDIA GPUs, was designed with this in mind. PTX code can be embedded in a binary and, thanks to just-in-time (JIT) compilation by the driver, executed safely on future GPU architectures. However, with the growing number of coarse-grained acceleration primitives in GPU architectures (e.g., Tensor Cores), maintaining this contract has become increasingly difficult. The traditional SIMT programming model of GPUs does not map naturally to primitives that go beyond register-level operations. To address this challenge, we introduce TileIR, a new block-level programming model for CUDA. TileIR provides a higher-level abstraction for programming NVIDIA GPUs that restores forward portability and is designed to express coarse-grained primitives such as Tensor Cores. <br> *Bio: Lorenzo Chelini is a compiler engineer at NVIDIA. He holds a Ph.D. in Computer Engineering from the Technical University of Eindhoven, a Master's degree from the Polytechnic of Turin, and a Bachelor's from the University of Pisa. Lorenzo actively contributes to the LLVM ecosystem, mainly MLIR and Polygeist. Théo is a compiler engineer at NVIDIA working on the TileIR spec and compiler. Previously, he worked on compiler acceleration with dedicated hardware at the University of Cambridge.*|
| 12:30 | **XTC, a research platform for ML compilation - Christophe Guillon @ INRIA** |
|| In this talk, we introduce XTC (Xdsl Transform Compiler), a compiler framework that provides high-level scheduling specifications for linear algebra operations over dataflow graphs. We present a practical use case where we define an operational graph and apply a scheduling strategy to it. We then generate several variants of the scheduled graph using predefined strategy parameters, targeting both the TVM and MLIR backends to produce optimized executables. Finally, we run a basic auto-tuning loop to explore the scheduling space and identify the best-performing set of parameters, illustrating how XTC bridges abstract algorithm definitions with efficient, backend-specific implementations. <br>*Bio: Christophe Guillon is a senior research engineer at INRIA Grenoble.  He has been working on compiler IRs, backend optimizations and auto-tuning strategies for C/C++ compilers. He is currently exploring compilation for ML DSLs, performance modeling and iterative optimization.*||
| 13:00 | --- Lunch ---                                                       |
| 14:00 | **CASCADE @ Cambridge Computer Laboratory - Timothy Jones**           |
| 14:15| **Summer School Lightning Talks**                                   |
| 15:30 | **Social & Snacks - Bring posters if you feel like it**             |
| 17:00 | End of day program                                                  |


## Location

[Department of Computer Science and Technology, University of Cambridge](https://cst.cam.ac.uk)

William Gates Building,  15 JJ Thomson Avenue, Cambridge, UK

<iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d19559.08383344916!2d0.09906737841796864!3d52.20912859760371!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47d8774a3f6e55cd%3A0xabf8227343e684c7!2sComputer%20Laboratory!5e0!3m2!1sen!2suk!4v1756152356920!5m2!1sen!2suk" width="800" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
