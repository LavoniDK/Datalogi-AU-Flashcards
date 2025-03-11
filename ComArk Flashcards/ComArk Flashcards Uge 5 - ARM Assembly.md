___
#flashcards/ComArk/5_ARM-Assembly

## Assembly

**What are the main sections of an assembly program?**::`.text` (code), `.data` (initialized data), `.bss` (uninitialized data), **stack** (temporary storage), **heap** (dynamic memory).
<!--SR:!2025-03-12,1,230-->

**What are common features of assembly languages?**::Labels, comments, global variables, directives.
<!--SR:!2025-03-15,4,272-->

**What is the purpose of labels in assembly?**::They aid readability and can be used for jump instructions.
<!--SR:!2025-03-15,4,270-->

**What aspects does an ABI govern?**::Calling conventions, system call interfaces, register usage, memory layout, executable formats.
<!--SR:!2025-03-14,3,250-->

**What is an ELF file?**::Executable and Linkable Format, a common format for executables, object code, shared libraries, and core dumps. ELF is important in Unix-like systems as it standardizes how executables interact with the OS and hardware.
<!--SR:!2025-03-14,3,250-->

**What is the Von Neumann Bottleneck?**::A performance limitation caused by the time spent accessing memory. It can be alleviated by using immediate operands and registers instead of frequent memory access.
<!--SR:!2025-03-14,3,250-->

**What is the difference between assembling and disassembling?**
?
- **Assembling**: The process of converting assembly language into machine code using an **assembler**.
- **Disassembling**: The reverse process—converting machine code back into assembly language using a **disassembler**.
- Disassemblers may not fully recov**What is the A32 instruction set?**er original labels, comments, or high-level constructs.
<!--SR:!2025-03-15,4,270-->

## ARM

**What are the main data types in ARM A32?**::Byte (1B), Halfword (2B), Word (4B).
<!--SR:!2025-03-15,4,272-->

**What kind of architecture is ARM?**::A RISC (Reduced Instruction Set Computing) architecture with a load-store model.
<!--SR:!2025-03-14,3,250-->

**What are ARM instruction suffixes used for?**::They modify the behavior of general instructions (e.g., conditional execution).
<!--SR:!2025-03-14,3,252-->

**Why are conditional instructions useful in ARM?**::They enable efficient branching without needing extra jump instructions.
<!--SR:!2025-03-15,4,272-->

**What are the four addressing modes in ARM?**::Preindexed, Preindexed with Writeback, Postindexed, `ldr` (pseudoinstruction).
<!--SR:!2025-03-14,3,250-->

**What is the purpose of the `ldr` instruction?**::It is a pseudoinstruction that loads a value into a register.
<!--SR:!2025-03-15,4,272-->

**What instruction is used to return from a function?**::`bx` (Branch and Exchange).
<!--SR:!2025-03-15,4,270-->

Describe the ARM `PSTATE` flags register.
?
- **N (Negative flag, bit 31)**: Set if the result is negative.
- **Z (Zero flag, bit 30)**: Set if the result is zero.
- **C (Carry flag, bit 29)**: Set if an operation generates a carry/borrow.
- **V (Overflow flag, bit 28)**: Set if an arithmetic operation results in an overflow.
<!--SR:!2025-03-14,3,250-->

How does the second operand work in ARM A32?
?
- It can be either:
  1. A register (`Rm`) with an optional shift:
     - `lsl` (logical shift left)
     - `lsr` (logical shift right)
     - `asl` (arithmetic shift left)
     - `asr` (arithmetic shift right)
     - `ror` (rotate right)
     - `rrx` (rotate right with extend)
  2. An immediate value computed from a 4-bit rotation of an 8-bit constant.
<!--SR:!2025-03-14,3,252-->

Explain the problem with nested function calls in ARM A32.
?
- The `bl` (Branch with Link) instruction saves the return address in `lr` (r14).
- If another `bl` instruction is executed before returning, `lr` is overwritten.
- This can cause the program to return to the wrong address.
- **Solution**: Save `lr` to the stack (`sp`, r13) before making a nested call.
<!--SR:!2025-03-15,4,272-->

What happens when executing `svc #0` in ARM A32?
?
- It triggers a **supervisor call (system call)**.
- An exception is raised, executing from the vector base address (`VBAR`).
- The CPU switches to a higher privilege level.
- The immediate value `#0` has no hardware effect but can be inspected by software.
- Used to interact with the operating system.
<!--SR:!2025-03-14,3,252-->
