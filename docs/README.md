As the diversity of hardware accelerators increases, and CPUs keep adding more
cores, it becomes increasingly important to write software that can run in a
heterogeneous environment. This training introduces Kokkos, a C++ programming
model that lets you write parallel code for CPUs, GPUs, and other accelerators.

Kokkos provides abstractions for parallel execution and data management, and it
can target different hardware platforms through backends such as Serial, OpenMP,
CUDA, HIP, and SYCL.


## Learning outcomes

When you complete this training, you will be able to

* explain the main ideas behind the Kokkos programming model;
* write basic Kokkos programs that can run on CPUs, GPUs, and other
  accelerators;
* use Kokkos execution patterns such as `parallel_for`, `parallel_reduce`, and
  `parallel_scan`;
* use Kokkos views to manage data used by parallel kernels;
* reason about host/device data movement and synchronization;
* recognize when execution spaces, memory spaces, team policies, scratch memory,
  and Kokkos kernels become relevant.


## Schedule

Total duration: 6 hours, split over two sessions.


### Session one

Total duration: 3 hours

  | Subject                                     | Duration |
  |---------------------------------------------|----------|
  | introduction and motivation                 |  5 min.  |
  | GPU hardware and general programming model  | 85 min.  |
  | coffee break                                | 10 min.  |
  | installation and building                   | 20 min.  |
  | Kokkos views                                | 60 min.  |


### Session two

Total duration: 3 hours

  | Subject                             | Duration |
  |-------------------------------------|----------|
  | Kokkos execution patterns           | 30 min.  |
  | Kokkos execution spaces             | 30 min.  |
  | code examples                       | 30 min.  |
  | coffee break                        | 10 min.  |
  | Kokkos nested parallelism           | 30 min.  |
  | Kokkos scratch pads                 | 20 min.  |
  | Kokkos libraries and kernels        | 20 min.  |
  | wrap-up and questions               | 10 min.  |


## Training materials

The [slide deck](slides/heterogeneous_programming_with_kokkos.html) is
available as a Quarto RevealJS presentation.

Slides, source code, environment recipes, and supporting material are available
in the [GitHub repository](https://github.com/gjbex/Heterogeneous-programming-with-Kokkos).


## Target audience

This training is for you if you write C++ software and want to understand how
Kokkos can help target CPUs, GPUs, and other accelerators without rewriting the
core algorithm for each backend.

It is especially relevant for scientific-computing, high-performance-computing,
and technical-software developers who need portable performance across changing
hardware platforms.


## Prerequisites

You should be familiar with C++. Familiarity with a Linux environment is also
required.

More concretely, participants should already be comfortable with the following:

* writing and reading small to medium C++ programs;
* functions, classes or structs, references, and `const` correctness;
* compiling and running C++ programs from the command line or with CMake at a
  basic level;
* standard-library containers and loops;
* lambda expressions at a basic reading level;
* working from the shell: navigating directories, editing files, and running
  commands;
* basic parallel-programming ideas such as loops over many elements,
  reductions, and the fact that race conditions can occur when many threads
  update shared data.

You do not need prior experience with Kokkos itself, execution spaces, views,
team policies, device memory, or backend-specific GPU programming such as CUDA
or HIP. Those are part of the training itself.


### Quick self-assessment

If you can do most of the tasks below without looking up basic C++ or shell
syntax, you are likely ready for this training.

* read a short C++ program that uses a struct or class and explain what it does;
* compile and run a small C++ program from the command line;
* store values in a `std::vector`-like container and loop over them;
* read a lambda expression and understand what values it uses;
* understand at a high level what a reduction such as a sum over many elements
  does;
* understand at a high level why updating a shared variable from many threads
  can cause incorrect results;
* make a small change to an existing C++ source file and rebuild it.

If several of these items still feel difficult, the training will probably move
too fast. In that case, it is better to first refresh modern C++ basics and,
if needed, take a short introduction to parallel programming concepts.


### Software and access requirements

To follow hands-on, you need a C++ development environment with CMake and Kokkos
available. For CPU-only examples, a modern C++ compiler and a Kokkos build with
Serial or OpenMP support are sufficient.

For GPU examples, you need access to appropriate accelerator hardware and a
matching Kokkos backend, such as CUDA for NVIDIA GPUs or HIP for AMD GPUs. Some
examples in `source-code/cuda_required` only compile when Kokkos is configured
with CUDA support.

The repository contains example CMake projects under `source-code/` and
environment recipes under `environments/`. The environment recipes are based on
the NVIDIA HPC SDK container and can be used to build a Docker, Apptainer, or
Singularity image for the training.

If you use an HPC system, make sure you know how to load compilers, CMake,
Kokkos, and GPU runtime modules provided by that system.


## Level of the Material

For participants who already have basic to intermediate C++ programming
experience, the material in this training is approximately

* Introductory: 15 %
* Intermediate: 40 %
* Advanced: 45 %

These percentages describe the level of the heterogeneous-programming and
Kokkos topics covered in the training, not the required entry level in C++
itself.


## Trainer(s)

* Geert Jan Bex ([geertjan.bex@uhasselt.be](mailto:geertjan.bex@uhasselt.be))
