____
#flashcards/ComArk/4_Instruction-Set-Architecture 

What is instruction representation?:: **Instruction representation** refers to how machine instructions are encoded and stored in a computer's memory. It defines how an instruction is structured, including its operation code (opcode), operands, and addressing modes. In short it is the format for each operation.
<!--SR:!2025-03-13,12,286-->

What two concepts combined define an Instruction Set Architecture (ISA)?::Instruction set and instruction representation.
<!--SR:!2025-03-17,16,300-->

What three elements define what an instruction does and how?::Opcode, operands, and a mechanism for handling results.
<!--SR:!2025-04-01,21,259-->

What are the benefits of Fixed-length instructions?::They simplify hardware design and can lead to faster processing
<!--SR:!2025-03-18,17,300-->

What do Branch instructions do::alter the program’s execution flow.
<!--SR:!2025-04-19,39,299-->

What is a Jump to Subroutine (CALL)?::An instruction that transfers control to a subroutine and stores the return address for later execution of a return instruction.
<!--SR:!2025-03-16,15,290-->

What is the principle of orthogonality in instruction set design?::that each instruction should be independent of others and operate consistently across different data types and addressing modes
<!--SR:!2025-03-15,14,290-->

What are Register banks?::A division of registers into separate physical units, allowing for simultaneous access and faster instruction execution
<!--SR:!2025-03-17,16,303-->

Why does Register banks often lead to register conflicts?::because certain instructions might mandate that operands reside in distinct register banks.
<!--SR:!2025-03-18,17,299-->

**What is register windowing?** :: Register windowing provides each procedure with its own set of registers (a register window) to reduce the overhead of saving/restoring registers and passing parameters. More registers are physically implemented than visible, with the **Current Window Pointer (CWP)** rotating between sets on subroutine calls. This allows efficient parameter passing and return value handling, by making windows overlap.
<!--SR:!2025-03-15,4,299-->

What two broad categories do computer architects classify instruction sets into, and what are their characteristics?
?
* **Complex Instruction Set Computer (CISC):** Large, complex instruction sets that can execute multi-step operations within a single instruction.
* **Reduced Instruction Set Computer (RISC):** Prioritizes a minimal instruction set consisting of simple, fixed-length instructions.
<!--SR:!2025-03-16,15,296-->

What does RISC processors implement to approach an execution rate of one instruction per clock cycle?::a five-stage instruction pipeline, where new instructions are staged for execution while others are executed.
<!--SR:!2025-03-18,17,300-->

What are Pipeline hazards?::A situation where an instruction cannot proceed through the pipeline as expected, causing the pipeline to stall.
<!--SR:!2025-03-15,14,296-->

What is **Data Hazards**?::Data hazards occur when an instruction depends on the result of a previous instruction that has not yet completed. This can be mitigated by forwarding results.
<!--SR:!2025-03-18,17,299-->

What are control hazards?::Control hazards, are hazards that occur when the execution path changes due to branching. Can be mitigated by branch prediction
<!--SR:!2025-03-17,16,290-->

What are structural hazards?::Hazards that arise when multiple instructions compete for the same hardware resource.
<!--SR:!2025-03-16,5,267-->

What does a no-op (NOP) instruction perform?::no operation, it is useful for timing adjustments, instruction alignment and pipeline padding, when the programmer needs to resolve pipeline hazards manually.
<!--SR:!2025-03-18,17,303-->

What is the Data Path?::the **Data Path** refers to the hardware components and connections that facilitate the movement and transformation of data within a processor.
<!--SR:!2025-03-13,12,279-->