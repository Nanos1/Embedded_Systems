# Embedded_Systems

## Lab 1: Loop Transformations - Design Space Exploration
### Description
This lab focuses on optimizing the *Parallel Hierarchical One Dimensional Search (PHODS)* algorithm for motion estimation in multimedia. Key optimizations include loop fusion, loop unrolling, and data reuse to enhance data locality and reduce execution time.

**Design Space Exploration**
The optimized code undergoes Design Space Exploration to determine the optimal block dimensions (Β and Βx-By) for improved parallelism.

## Lab 2: Dynamic Data Type Refinement
### Description
This lab employs *Dynamic Data Type Refinement (DDTR)* to optimize the dynamic data structures of network applications, specifically Deficit Round Robin (DRR) and Dijkstra's algorithm. Evaluation tools include the DDTR library, Massif, and Lackey from the Valgrind suite.

*DRR and Dijkstra Optimization*
Optimizations involve testing different data structure combinations (SLL, DLL, DYN_ARR) for memory accesses and footprint, resulting in Pareto Optimal Solutions.

## Lab 3: ARM Assembly
### Description - Emulator
This lab explores ARM assembly programming using **QEMU** as a system simulator. Part 1 involves converting input from the terminal, and Part 2 focuses on communication between guest and host machines via a virtual serial port. Part 3 combines C and ARM assembly code.

## Lab 4: High-Level Synthesis for FPGA
### Description
This lab delves into **High-Level Synthesis (HLS)** for **FPGA** programming, optimizing a Generative Adversarial Network (GAN) application for the Xilinx Zybo FPGA using the SDSoC 2016.4 tool. HLS pragmas such as loop pipelining and loop unrolling are applied for performance improvement.

Performance and Quality Measurement
The lab includes performance and resource measurement, Design Space Exploration, and quality measurement via Max Pixel Error and Peak Signal-to-Noise Ratio (PSNR).

## Lab 5: Cross-compiling for ARM
- Part 1
This lab involves creating **ARM** virtual machines, installing cross-compilers (crosstool-ng and Linaro), and comparing their performance by testing executables.

 - Part 2
Using crosstool-ng, a new Linux kernel is built for Debian with a new system call using the printk function. The process includes changes to the kernel source code, and a test program (test.c) verifies the proper operation of the new system call.
