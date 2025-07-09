---
layout: single
title: "Expert Themes"
permalink: /themes/
---


Covering a number of pressing technical themes, we bring key stakeholders
together, go into technically depth, and make forward progress through
conversation, coding, and community alignment. Our topics this year are
hardware accelerators, crypto, quantum, performance modeling, scheduling
languages, compiler backends, formal verification, and EDA."

**Hardware Accelerators for AI and More**

**Crypto-IRs and Crypto-Aware Design**

The crypto community has discovered MLIR as a tool and uses it to build systems where programs are compiled into cryptographic schemes, endowing them with strong properties. For example, the [HEIR compiler](https://heir.dev/) based on MLIR implements *fully homomorphic encryption*, meaning the resulting program can operate on encrypted data without the party running the computation learning anything. Another example are *zero knowledge circuits*, which allow one to prove they ran a publicly known program on a secret input and obtained a specific result. [LLZK](https://veridise.github.io/llzk-lib/main/) is a recent MLIR-based infrastructure that can consume different types of circuits and can analyze and compile them. In addition, cryptographic codes have specific requirements, e.g., *constant time* preservation: the run time of cryptographic routines should not depend on the value of the secrets, which precludes branching on secrets or even some multiplications. However, programs written in this style can be slower, and thus compilers break constant time while optimizing.

**Quantum Computing**

As quantum computers scale, compilation becomes a fundamental challenge at all levels of abstraction. Quantum compilers are not just about the abstract representation of programs/intermediate representations in the compilation stack, but — especially in the non-Clifford and fault-tolerant regimes — also about the logical representation, layout, scheduling and distribution of compute. This is made more difficult by the target hardware — qubit architectures and their control systems — being an evolving target. 
Further, no system is purely quantum — even textbook algorithms such as Shor’s include structure, control flow, and classical instructions, and we need compiler toolchains that take this into account. While industrial-scale, open source tooling for classical compilation develops at high velocity and is heavily used, in contrast bespoke quantum compilers often reimplement the infrastructure as proprietary, closed source tools. 
The MLIR School is an opportunity to advance the state of compilers to make quantum computing first-class in the MLIR ecosystem. We will also learn from other domain-specific compilers, and investigate problems at the intersection of domains such as how noise models in quantum programs relate to noise in Fully Homomorphic Encryption

**Performance Modeling and Evaluation**

The modern hardware landscape is a diverse collection of compute engines: out-of-order CPUs, GPUs, VLIWs, DSPs, ML accelerators, and various embedded devices. Often, compilers remain largely oblivious to the microarchitectural performance characteristics that performance and compiler engineers meticulously embed directly into heuristics.

Prior modeling efforts, primarily focused on CPUs, like LLVM's TableGen schedule models, precisely capture instruction latencies and resource usage. However, MLIR offers a compelling new avenue with the direct embedding of multi-level abstractions. This capability, coupled with the new computational domains it unlocks, compels us to rethink our design. How can we truly integrate target-aware information as a first-class citizen for this complex and heterogeneous compute landscape?

**Scheduling Languages**

For a long time, performance engineers had to choose between relying on the fragile and opaque heuristics of compilers and manually writing compute kernels in assembly. The emergence of scheduling languages such as [Halide](https://halide-lang.org/) made it possible to control transformations while still benefiting from automatic code generation; the primitives of these languages act as an interface to trigger the compiler’s transformation functions (vectorize, unroll, tile, etc.), but the decision is not delegated to heuristics --it is made by the engineer.

These approaches have now been adopted in MLIR through the [Transform dialect](https://mlir.llvm.org/docs/Dialects/Transform/), where the ecosystem of dialects allows for precise manipulation of computations at various levels of abstraction. New opportunities are emerging, both for manual optimization and for autotuning. What is the next step?

**Backends and Code Generation**

Today, most MLIR-based compilation pipelines still rely on the traditional LLVM backend for the final lowering stages. After transformations in MLIR, the IR is typically handed off to ```opt``` and ```llc``` for code generation, leaving the instruction selection, register allocation, and low-level optimizations to the classic LLVM toolchain. While this leverages a mature and battle-tested backend, it also imposes a boundary: once lowered to LLVM IR, the benefits of MLIR’s structured abstractions are lost.

However, the landscape is shifting. MLIR now offers the possibility to extend backend infrastructure directly within the MLIR framework. This opens the door to backend passes that are composable, retargetable, and aware of the high-level semantics preserved throughout the MLIR pipeline. It invites a rethinking of backend design: can instruction selection be made more declarative? Can we build customizable register allocators as passes? How far can we push code generation within MLIR itself, before handing off to a target-specific assembler?

** Formal Verification
