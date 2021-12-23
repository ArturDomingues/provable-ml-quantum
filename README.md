# Provably efficient machine learning for quantum many-body problems

This is an open source implementation for the paper https://arxiv.org/abs/2106.12627. We require `g++` and `python` version 3. The Python package we used are given in `requirements.txt`.

### Quick Start

```shell
#
# C++ code is only used for classifying topological phases
#

# Compile the C++ code
> g++ -O3 -std=c++0x shadow_kernel_topological.cpp -o shadow_kernel_topological

# Run the C++ code
#    ./shadow_kernel_topological [length L in toric code (total number of qubits = 2 L x L)]
#                                [number of randomized Pauli measurements (for creating classical shadow)]
#                                [number of random states (half trivial, half topologically-ordered)]
#                                [maximum depth for generating random states]
#                                [random seed]
#                                [gamma in shadow kernel (1.0 is usually a good choice)]
> ./shadow_kernel_topological 10 500 10 5 13131 1.0 > topological_alldep_tr=10.txt

# Open the iPython notebook
# jupyter notebook
```
