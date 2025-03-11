____
#flashcards/ComArk/6_X86-64-Assembly

**What is microprogramming?**::A method of implementing CPU control logic using microcode instead of hardwired logic.
<!--SR:!2025-03-14,3,250-->

**Why was microprogramming historically important?**::It allowed for easier bug fixes, new instruction additions, and instruction set emulation.
<!--SR:!2025-03-15,4,277-->

**What is the difference between horizontal and vertical microprogramming?**
?
- **Horizontal**: Each bit controls a specific hardware element, enabling parallel execution.
- **Vertical**: More compact, requires decoding before execution, typically lower parallelism.
<!--SR:!2025-03-15,4,276-->

**How many general-purpose registers does x86-64 have?**::16 (RAX, RBX, RCX, RDX, RSI, RDI, RBP, RSP, R8–R15).
<!--SR:!2025-03-15,4,270-->

**What are the two main x86 assembly syntax styles?**
?
- **Intel Syntax**: Destination first (e.g., `mov eax, ebx`).
- **AT&T Syntax**: Source first, uses `%` for registers (e.g., `movl %ebx, %eax`).
<!--SR:!2025-03-15,4,274-->

**What suffixes indicate operand sizes in AT&T syntax?**
?
- `b` = Byte (8-bit)
- `w` = Word (16-bit)
- `l` = Doubleword (32-bit)
- `q` = Quadword (64-bit)
<!--SR:!2025-03-15,4,270-->

What are the key components of an x86 instruction?
?
- **Prefixes (optional)**: Modify instruction behavior.
- **Opcode**: Specifies operation (e.g., `MOV`, `ADD`).
- **ModR/M Byte (optional)**: Specifies addressing mode.
- **SIB Byte (optional)**: Used for scaled indexed addressing.
- **Displacement (optional)**: Immediate value added to address.
- **Immediate Data (optional)**: Constant operand value.
<!--SR:!2025-03-12,1,237-->
