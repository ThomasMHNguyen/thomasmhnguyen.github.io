---
title: "Vectorization Calculations for Fast CFD Computation Times"
excerpt: "I developed an innovative vectorization algorithm for my CFD-FSI simulations to speed up intra-particle interaction computations. Benchmarked against other methods, the vectorization results in an approximately 100x decrease in computation times."
collection: portfolio
---


<img width="520" src='/images/vect_times.png'>


I developed an innovative vectorization algorithm for my CFD-FSI simulations to speed up intra-particle interaction computations. This vectorization algorithm was benchmarked against the following (see graphic):

1. Simulations **without** intra-particle interaction computations (with time-steps of \\(\Delta t = 10^{-3}\\)); listed as "Local:Optimized"

2. Simulations **without** intra-particle interaction computations (with time-steps of \\(\Delta t = 10^{-4}\\)); listed as "Local:Unoptimized"

3. Simulations **with** intra-particle interaction computations (with time-steps of \\(\Delta t = 10^{-4}\\)) using nested *for*-loops; listed as "Non-Local:Non-Vectorized"

4. Simulations **with** intra-particle interaction computations (with time-steps of \\(\Delta t = 10^{-4}\\)) using nested back-end C/C++ compiler for the nested *for*-loops; listed as "Non-Local:Numba Optimized"

5. Simulations **with** intra-particle interaction computations (with time-steps of \\(\Delta t = 10^{-4}\\)) using full vectorization of these computations; listed as "Non-Local:Vectorized"


### Notes

The benchmarks displayed here are for single-particle simulations. For multi-particle calculations, the vectorization boost in decreased computation times is expected to be approximately the same amount for single-particle calculations or even greater.

[Link to GitHub Repo will be created soon!]()
