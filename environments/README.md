# Environments

This directory contains tools to set up your environment for
this training.


## What is it?

1. `nvidia_hpc_sdk.py`: an HPCCM recipe to create a Docker or Singularity
   recipe.  It is based on the NVIDIA HPC SDK container, and adds a few
   extra packages and tools to make it suitable for this training.
1. `nvidia_hpc_sdk.recipe`: the generated HPCCM recipe.  You can use this to
   build a container image with the NVIDIA HPC SDK and the extra tools.
