---
layout: single
title: "Themes"
permalink: /themes/
---

**MLIR for cryptography** Cryptography poses specific challenges for compilers. One subtle aspect is *constant time* preservation: the run time of cryptographic routines should not depend on the value of the secrets, which precludes branching on secrets or even some multiplications. However, programs written in this style can be slower, and thus compilers break constant time while optimizing. Another, more recent, application of MLIR to cryptography are systems where programs are compiled into cryptographic schemes, endowing them with strong properties. For example, the [HEIR compiler](https://heir.dev/) based on MLIR implements *fully homomorphic encryption*, meaning the resulting program can operate on encrypted data without the party running the computation learning anything. Another example are *zero knowledge circuits*, which allow one to prove they ran a publicly known program on a secret input and obtained a specific result. [LLZK](https://veridise.github.io/llzk-lib/main/) is a recent MLIR-based infrastructure that can consume different types of circuits and can analyze and compile them.
