# High-Level Synthesis for FPGA
## Overview
This exercise delves into the realm of High-Level Synthesis (HLS) for FPGA programming, focusing on optimizing and accelerating C code for the **Xilinx Zybo FPGA** hardware.

Context
The optimization target is an application related to neural networks, specifically **Generative Adversarial Networks** (GANs). The task involves reconstructing half images from handwritten digits sourced from the ([MNIST dataset](https://en.wikipedia.org/wiki/MNIST_database)). The primary objective is to enhance the algorithm's speed compared to its software implementation while evaluating the quality of image reconstruction.

Utilized Tool: SDSoC 2016.4
The development process employs the [SDSoC](https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/vitis/archive-sdsoc.html) tool, providing an Eclipse-like environment for creating an accelerator running on the embedded Zybo FPGA. SDSoC facilitates performance and resource estimation, bitstream creation, and the generation of an sd boot card for system boot-up.

HLS Pragmas: Fine-Tuning the Design
To optimize the design, the HLS compiler's pragmas are harnessed, enabling adjustments in latency, throughput performance, device resource usage, and I/O port control. Key pragmas include Loop Pipelining for reduced latency, Loop Unrolling for enhanced parallelism, array partitioning for increased memory bandwidth, allocation for resource management, and tripcount for precise analysis.

Part 1: Performance and Resources Assessment
The initial performance estimation involves running the application with no optimizations. The subsequent steps include creating an sd card, uploading it to Zybo, and comparing it with the initial estimation. Design Space Exploration is conducted, testing various HLS pragmas to estimate their impact on performance. The final optimized sd boot card is uploaded to Zybo, and the application is executed, with results documented in output.txt. The optimized version demonstrates a remarkable Speed-Up from 2.16 to 120.65, making it over 55 times faster than the original.

Part 2: Quality Evaluation
The quality measurement phase combines half images from the input with those generated by both software and hardware (stored in output.txt). Image reconstruction quality is assessed using a Jupyter notebook, employing metrics such as Max Pixel Error and Peak Signal-to-Noise Ratio (PSNR). Additionally, different datatypes (8-bit, 4-bit, and 10-bit) are explored to discern any variations in performance.

For comprehensive details, including insights into the application, HLS pragmas, tools used, and detailed results, refer to the full report.