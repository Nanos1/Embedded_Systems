# Dynamic Data Type Refinement - Optimization of Dynamic Data Structures
## Overview
This document outlines the process of optimizing dynamic data structures in two network applications using the "Dynamic Data Type Refinement" (DDTR) methodology. We focus on enhancing the performance of the Deficit Round Robin (DRR) and the Dijkstra algorithm.

###Deficit Round Robin (DRR)
In the case of DRR, we aim to improve its dynamic data structures for the list of packets and nodes. We evaluate the impact of different data structure combinations, such as Single Linked List (SLL), Double Linked List (DLL), and Dynamic Array (DYN_ARR) on two key aspects:

1. Memory Accesses: This pertains to any read and write operations involving the main memory.
2. Memory Footprint: This refers to the amount of main memory utilized or referenced during program execution.
Our assessment leverages the following tools:

DDTR library
- Massif tool from the Valgrind suite
- Lackey tool from the Valgrind suite
- The results are analyzed to identify the optimal solutions that provide the best trade-off between memory access and memory footprint.

Dijkstra Algorithm
For the Dijkstra algorithm, which is responsible for finding the shortest path in a 100x100 table, we implement the DDTR methodology. The nodes are stored in a list, and after integrating the DDTR library into the application, we replace the original data structures with those provided by DDTR. The comprehensive process is detailed in the associated report.

We experiment with various combinations of data structures, including Single Linked List (SLL), Double Linked List (DLL), and Dynamic Array (DYN_ARR). Similar to the DRR evaluation, we measure the memory access and memory footprint for each combination to identify the Pareto Optimal solution that offers the best balance between the two metrics.

This document serves as an introduction to our efforts in optimizing these network applications, highlighting the key goals, methodologies, and tools employed for the task. Further insights and findings can be found in the associated reports for each application.
