# ARM Assembly Emulator
## Overview - Emulator
In the realm of ARM assembly, we delve into the world of emulation. Our tool of choice? **QEMU** ([Quick Emulator](http://wiki.qemu.org/Main_Page)) (Quick Emulator), an open-source emulator capable of simulating diverse systems and processors. The twist? It runs on a system with a different processor, typically of the x86 variety.

## Phase 1: Terminal Input Conversion
Our journey begins with crafting an ARM assembly program. It graciously accepts a string, up to 32 characters in length, from the terminal. Should the input exceed this limit, the surplus characters are shrugged off. Within this string, transformations unfold:

Capital letters gracefully shift to lowercase and vice versa.
Numeric characters in the range ['0', '9'] undergo a unique metamorphosis:
'0' → '5'
'1' → '6'
'2' → '7'
'3' → '8'
'4' → '9'
'5' → '0'
'6' → '1'
'7' → '2'
'8' → '3'
'9' → '4'
This program persists until it encounters a one-character string featuring the majestic 'Q' or its lowercase counterpart 'q'.
Further details await in the report.

## Phase 2: Guest-Host Communication via Serial Port
Behold the seamless communication between two realms—the host machine and the ARM-powered guest machine. A symbiotic duo emerges:

Host Machine (C): Consumes a string of up to 64 characters and dispatches it through a virtual serial port.
Guest Machine (ARM): Analyzes the incoming string, identifies the character with the highest frequency (excluding the blank character), and reports its occurrence count. In case of a tie, the character with the smallest ASCII code triumphs.
Consult the report for an intricate dance of strings and frequencies.

## Phase 3: C-ARM Synergy - Linking Code
Harmony unfolds as we weave C and ARM assembly code into a seamless tapestry. The mission? To seamlessly replace functions from the string.h library within the string_manipulation.c program. Here's the ballet of functions:

- size_t strlen(const char *str)
- char *strcpy(char *dest, const char *src)
- char *strcat(char *dest, const char *src)
- int strcmp(const char *str1, const char *str2)
  
Each function declares its presence with an extern in C and dances its way into an assembly code file. The .global directive ensures visibility to the linker. A meticulous compilation and linking ritual, orchestrated by a Makefile, births the final executable.

Discover the intricate steps in the report.
