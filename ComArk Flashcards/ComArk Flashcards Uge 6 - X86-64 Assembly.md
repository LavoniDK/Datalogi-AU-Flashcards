____
#flashcards/ComArk/6_X86-64-Assembly

**What is microprogramming?**::A method of implementing the control logic of a CPU using **microcode**, rather than hardwired circuits. Microinstructions direct internal data flows and operations.
<!--SR:!2025-07-17,70,270-->

**Why was microprogramming historically important?**::It enabled **easier debugging**, **simpler modification** of the instruction set, and **emulation** of other architectures—especially valuable in the early evolution of complex CPUs.
<!--SR:!2025-06-23,47,297-->

**What is the difference between horizontal and vertical microprogramming?**
?
- **Horizontal microprogramming**: Uses **wide microinstructions**, where each bit directly controls part of the CPU (e.g., ALU op, register load). Enables **parallel operations**, but consumes more memory.
- **Vertical microprogramming**: Uses **narrower microinstructions** that are **encoded** and must be **decoded** before use. More compact, but often **slower** and less parallel.
<!--SR:!2025-07-22,52,276-->


**What are the two main x86 assembly syntax styles?**
?
- **Intel Syntax**: Destination first (e.g., `mov eax, ebx`).
- **AT&T Syntax**: Source first, uses `%` for registers (e.g., `movl %ebx, %eax`).
<!--SR:!2025-08-08,85,274-->

**What suffixes indicate operand sizes in AT&T syntax?**
?
- `b` = Byte (8-bit)
- `w` = Word (16-bit)
- `l` = Doubleword (32-bit)
- `q` = Quadword (64-bit)
<!--SR:!2025-06-24,8,190-->


**Tip**: x86 syntax is more **compact but inconsistent**, while ARM is **verbose but regular and predictable**
<!--SR:!2025-04-16,3,256-->

