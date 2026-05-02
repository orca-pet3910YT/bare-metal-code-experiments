# Bare Metal Coding Experiments
For the past month, alongside other typical projects, I've been trying out different CPU architectures to see which is the most fun to use.

The purpose of this experiment is to see which bare-metal architecture is the easiest and most friendly to code for. So far, quite surprisingly, RISC-V appears to be the hardest to code for, while AVR looks to be the easiest, except for direct hardware manipulation.

The testing program needs to meet these rules:
- Prints a "Hello, World!"
- Returns and stops the CPU
- Has UART access
- Has working stack that's used correctly
- Runs on bare metal

| Architecture | Complexity | Did it run? | Notes |
| --- | --- | --- | --- |
| x86 | Easy | Yes | Starts in 16-bit mode, may also run in 32-bit or 64-bit depending on environment. |
| RISC-V | Medium | Yes | Stack needs to be manipulated manually, unlike x86 CPUs. Also, ELF entry point data is ignored, and instead the first function in the binary is called. |
| Atmel AVR | Easy | Yes | The hardware is limited to 2KB RAM and 32KB ROM. A lot of code is abstracted behind its C runtime. |
| ARM | Untested | Untested | The architecture is RISC, but has so many extensions that make it look like CISC. |
