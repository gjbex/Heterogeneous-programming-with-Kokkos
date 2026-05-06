As the diversity of hardware accelerators increases, and CPUs keep adding more
cores, it becomes increasingly important to write software that can run in a
heterogeneous environment. This training will introduce you to Kokkos, a
programming model that allows you to write code that can run on CPUs, GPUs, and
other accelerators. Kokkos is a C++ library that provides abstractions for
parallel programming, and can generate code for different hardware platforms.


## Learning outcomes

When you complete this training, you will

* understand the principles of the Kokkos programming model;
* be able to write parallel code that can run on CPUs, GPUs, and other
  accelerators;
* know about relevant execution patterns and how to implement them with Kokkos;
* be able to handle data transfers between the host and the device.


## Schedule

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

4otal duration: 3 hours

  | Subject                             | Duration |
  |-------------------------------------|----------|
  | Kokkos executtion patterns          | 30 min.  |
  | Kokkos execution spaces             | 30 min.  |
  | code examples                       | 30 min.  |
  | coffee break                        | 10 min.  |
  | Kokkos nested parallelism           | 30 min.  |
  | Kokkos scratch pads                 | 20 min.  |
  | Kokkos libraries and kernels        | 20 min.  |
  | wrap-up & questions                 | 10 min.  |


## Training materials

Slides and source code are available in the
 [GitHub repository](https://github.com/gjbex/Heterogeneous-programming-with-Kokkos),
as well as example code and hands-on material.


## Target audience

This training is for you if you want to develop software that can run on CPUs,
GPUs, and other accelerators.


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



## Training materials

Slides and source code are available in the
 [GitHub repository](https://github.com/gjbex/Heterogeneous-programming-with-Kokkos),
as well as example code and hands-on material.


## Target audience

This training is for you if you want to develop software that can run on CPUs,
GPUs, and other accelerators.


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



## Training materials

Slides and source code are available in the
 [GitHub repository](https://github.com/gjbex/Heterogeneous-programming-with-Kokkos),
as well as example code and hands-on material.


## Target audience

This training is for you if you want to develop software that can run on CPUs,
GPUs, and other accelerators.


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
