windbg-tracer
=============

Windbg Script to Reverse engineer Microsoft's Crypto API calls, finds the Cryptographic Service Provider function calls made during certificate enrollment  along with their specific arguments. 

Note:
- Works with win32 applications where all arguments are pushed to stack, handled with esp register.
- In order to trace API calls with 64 bit applications, the first 4 integer  arguments are pushed into rcx, rdx, r8 and r9 registers. Similarly,first 4 float arguments are pushed to some registers.
- The rest of the arguments are present on the stack. It's kind of tricky to handle those!
