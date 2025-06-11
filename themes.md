---
layout: single
title: "Expert Themes"
permalink: /themes/
---

Our expert themes, we bring key stakeholders together, go into technical depth, and make forward progress technically and as a community.

**Cryptography, Crypto-IRs, and Crypto-Aware Design**

The crypto community has discovered MLIR as a tool and uses it to build systems where programs are compiled into cryptographic schemes, endowing them with strong properties. For example, the [HEIR compiler](https://heir.dev/) based on MLIR implements *fully homomorphic encryption*, meaning the resulting program can operate on encrypted data without the party running the computation learning anything. Another example are *zero knowledge circuits*, which allow one to prove they ran a publicly known program on a secret input and obtained a specific result. [LLZK](https://veridise.github.io/llzk-lib/main/) is a recent MLIR-based infrastructure that can consume different types of circuits and can analyze and compile them. In addition, cryptographic codes has specific requirements, e.g., *constant time* preservation: the run time of cryptographic routines should not depend on the value of the secrets, which precludes branching on secrets or even some multiplications. However, programs written in this style can be slower, and thus compilers break constant time while optimizing.
