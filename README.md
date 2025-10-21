# Ginkgo and its Application in Solving Large Sparse Linear Systems

**Seminar Paper | June 2025**

This repository contains a seminar paper dedicated to the analysis of the modern C++ library **Ginkgo** for high-performance computing (HPC).

The main goal of the paper is to investigate the architecture and components of Ginkgo for efficiently solving large sparse linear systems ($Ax=b$) and achieving performance portability on heterogeneous hardware (CPU/GPU).

## [Read the Full Paper (PDF)](./IN2107_paper.pdf)

---

### Key Topics Investigated

The paper provides a deep dive into the key components necessary for building efficient solvers:

* **Sparse Matrix Storage Formats:** Analysis of the trade-offs between formats like **CSR**, **ELL**, and **SELL-P**, and their impact on Sparse Matrix-Vector Multiplication (SpMV) performance.
* **Iterative Solvers:** Overview and application of standard Krylov subspace methods, including **Conjugate Gradient (CG)**, **GMRES**, and **BICGSTAB**.
* **Preconditioning Methods:** Study of various strategies, from simple (e.g., **Jacobi**) to advanced (e.g., **ILU** and **Algebraic Multigrid (AMG)**).

### Main Conclusion: The Importance of Algorithms

One of the key takeaways from the paper is that selecting an advanced algorithm often has a greater impact on performance than simply upgrading hardware.

As shown in the analysis (Fig. 1 in the paper), using a more complex preconditioner like **ParILUT** (implemented in Ginkgo) provides a **3.8x algorithmic speedup** compared to a standard ILU. This demonstrates the value of modern libraries that provide such complex yet highly efficient components.

### Technologies and Concepts

* **Language:** C++
* **Libraries:** Ginkgo, Boost
* **Concepts:** HPC, Numerical Algorithms, Linear Algebra, Sparse Linear Algebra, GPGPU, CUDA, Performance Portability, SpMV, Preconditioning.
