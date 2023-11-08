# Embedded_Systems
## Part 1: Loop Transformations and Design Space Exploration
### Overview
In this section, we delve into the Parallel Hierarchical One-Dimensional Search (PHODS) algorithm, a multimedia domain algorithm specifically designed for Motion Estimation. The primary objective of PHODS is to detect object movement within consecutive frames of a video.

### Loop Transformations and Optimization Objectives
Our main focus in this section is to explore various loop transformations to optimize the PHODS algorithm, with the overarching goal of enhancing its performance. The specific optimization objectives include:

* Enhancing data reuse and data locality.
* Efficient utilization of the memory hierarchy.
* Reducing overheads associated with executing loops.
* Streamlining instructions for efficient pipelining.
* Maximizing parallelism within the algorithm.

We employ several key loop transformations to achieve these optimization goals, thus reducing the overall execution time. These transformations include:

* Loop Fusion (Merge): Merging two adjacent isomorphic loops to consolidate their functionality.
* Loop Unrolling: Aggregating consecutive loop steps and explicitly writing them without loop controls.
* Data Reuse strategies.

### Design Space Exploration
Within the optimized code, we engage in Design Space Exploration to identify the most suitable block dimensions for improved performance. Two specific scenarios are considered:

* Exploring a square block of dimensions Β to determine the optimal block size (B).
* Exploring a rectangular block of dimensions Βx-By to identify the optimal size for the block (Bx-By).

## Part 2: Automated Code Optimization
The [Orio](https://brnorris03.github.io/Orio/) Tool
Orio is a Python-based framework that specializes in code transformation and automatic performance tuning. It supports various source and target languages, making it a versatile tool for optimizing code.

Code Optimization with Orio
In this section, we leverage the power of the Orio tool to optimize the tables.c code. The function within this code involves simple data accesses and operations with tables. Our optimization efforts involve conducting Design Space Exploration to determine the optimal loop unrolling factor for enhanced performance.

We employ three different optimization algorithms, each with its unique approach to code optimization:

* Exhaustive
* Randomsearch
* Simplex
By employing these optimization techniques, we aim to significantly improve the performance and efficiency of the tables.c code, making it more robust and resource-efficient.
