# Cross-compiling for ARM
## Part 1
* We set up two virtual machines in QEMU.
* The first one has the **armel** architecture (arm EABI little-endian).
* The second one is configured with the **armhf** architecture (arm hard-float).
* We install the crosstool-ng custom cross-compiler building toolchain and the linaro pre-compiled building toolchain.
* A comparative analysis of the two cross-compilers is conducted by testing executables on the host machine and the virtual machines.
* For a detailed overview of the installation process and the results of the cross-compilers' comparison, refer to the report.

Part 2
* Utilizing the custom cross-compiler building toolchain crosstool-ng from Part 1, we compile a **new kernel** for the Debian Operating System.
* A new system call is incorporated into the kernel, utilizing the printk function to log a message in the kernel.
* The modifications made to the kernel source code are outlined in the report.
* The final kernel image can be found in the [linux-source-3.16](https://github.com/chrisbetze/Embedded-System-Design/tree/main/Lab5/linux-source-3.16) directory.
* Lastly, a C program (test.c) is written to test the proper functioning of the new system call.
* For a comprehensive walkthrough of the new kernel building process and the integration of the new system call, please refer to the detailed report.
