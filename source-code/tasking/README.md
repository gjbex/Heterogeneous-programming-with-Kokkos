# Tasking

Kokkos 4 supported creating DAGs of tasks. This API was deprecated in
Kokkos 4.5 and removed in Kokkos 5.0, so this example is preserved only as
legacy material and is skipped by the build when using Kokkos 5.1.x.


## What is it?

1. `fib.cpp`: legacy application illustrating tasking that computes
   the Fibonnaci number using tasks.
1. `CMakeLists.txt`: CMake file to build the applications.


## Note

This doesn't build with CUDA or with Kokkos 5.x.
