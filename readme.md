# Readme
---

## Overview
---
These scripts implement a symmetry-based circuit mapping (SBCM) algorithm and benchmark its performance, demonstrating its computational advantage over existing methods. The SBCM algorithm leverages quantum hardware symmetries to enhance subgraph matching efficiency, a crucial aspect of finding feasible circuit mappings.

In our numerical experiments, we consider three typical quantum hardware architectures, featuring 2D square grid, octagonal, and heavy-hex entangling-gate topologies, respectively.

## Benchmarking
+ The `benchmark_subgraph_matching_<hardware_architecture>.ipynb` files benchmark the runtime of subgraph matching algorithms. 
+ The `benchmark_circuit_mapping_<hardware_architecture>.ipynb` files test the runtime of circuit mapping scoring as well as the total runtime required to find the optimal circuit mapping. 
+ The `batch_data_processing_<hardware_architecture>.ipynb` files convert the benchmarking results to `.csv` files, a common data format, and save them to the `data` folder.

## Functions
The components that make up the SBCM algorithm are located in the `functions` folder. Within this folder, you can find several key files:

1. `functions_test_circuits.ipynb`: This file contains the definition of the input quantum circuit used in our numerical experiments.

2. `functions_set_graph.ipynb`: Here, you'll find the definition of the three coupling graphs mentioned earlier.

3. `functions_precompilation.ipynb`: In this file, you can access the precompilation function. This function transforms an input quantum circuit into a format suitable for physical implementation on quantum hardware. It also provides an initial circuit mapping, ensuring implementability, though not necessarily optimizing the overall circuit fidelity.

4. `functions_subgraph_matching.ipynb`: This file implements our symmetry-based subgraph matching (SBSM) algorithm, which efficiently identifies all feasible circuit mappings.

5. `functions_circuit_mapping.ipynb`: This file serves two purposes: (1) It defines the data structure of the quantum hardware. (2) It scores these circuit mappings by estimating their corresponding overall circuit fidelity.