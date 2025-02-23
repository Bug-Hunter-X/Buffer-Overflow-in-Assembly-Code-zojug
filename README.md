# Assembly Buffer Overflow Example

This repository demonstrates a simple buffer overflow vulnerability in assembly code. The `bug.asm` file contains code that's prone to buffer overflow if the base pointer `ebx` is not carefully managed. The `bugSolution.asm` file shows a potential solution using bounds checking.

## Vulnerability

The vulnerability lies in the lack of bounds checking before accessing and writing to memory locations relative to `ebx`. If `ebx` points to a small buffer, writing beyond the buffer's limits could lead to unpredictable consequences, such as program crashes or security exploits.

## Mitigation

The best way to prevent buffer overflows is to perform thorough bounds checking before every memory access.  This involves verifying that the memory address is within the allocated range for a given buffer.  Consider using dedicated functions to handle memory allocation and access for increased security and robustness.