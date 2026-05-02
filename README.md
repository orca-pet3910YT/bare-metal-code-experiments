# Bare Metal Coding Experiences
For the past month, alongside other typical projects, I've been trying out different CPU architectures to see which is the most fun to use.

The purpose of this experiment is to see which bare-metal architecture is the easiest and most friendly to code for. So far, quite surprisingly, RISC-V appears to be the hardest to code for, while AVR looks to be the easiest, except for direct hardware manipulation.

The testing program needs to meet these rules:
- Prints a "Hello, World!"
- Returns and stops the CPU
- Has UART access
- Has working stack that's used correctly

| Architecture | Complexity | Did it run? | Notes |
| --- | --- | --- | --- |
| x86 | Easy | Yes | Starts in 16-bit mode, may also run in 32-bit or 64-bit depending on environment |
| RISC-V | Medium | 3/4 points | Stack needs to be manipulated manually, unlike x86 CPUs |
| Atmel AVR | Easy | Yes | The hardware is limited to 2KB RAM and 32KB ROM |
