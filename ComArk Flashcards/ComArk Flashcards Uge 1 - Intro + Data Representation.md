____

#flashcards/ComArk/1_Into-and-Data-Representation 

## Data Representation


**What is the Most Significant Bit (MSB)?**::The leftmost bit in a binary number.
<!--SR:!2025-12-09,240,330-->

**What is the Least Significant Bit (LSB)?**::The rightmost bit in a binary number.
<!--SR:!2026-03-04,302,337-->

**What are unsigned integers?**::Numbers that represent only non-negative values.
<!--SR:!2026-01-13,266,337-->

**What is overflow?**::It occurs when a calculation exceeds the representable range.
<!--SR:!2026-02-18,288,337-->

**What is underflow?**::It occurs when a calculation is smaller than the smallest representable value.
<!--SR:!2025-09-20,173,310-->

**What is endianness?**
?
Endianness is the order in which bytes are arranged in memory:
- **Little-endian**: The least significant byte is stored first.
- **Big-endian**: The most significant byte is stored first.
<!--SR:!2025-07-08,119,302-->

What are the three methods for representing signed binary integers?
?
1. **Sign-Magnitude**: Divides bits into a sign bit (1 for negative, 0 for positive) and magnitude bits (absolute value).
2. **One’s Complement**: Negative numbers are formed by using a sign bit and inverting all bits of the positive value.
3. **Two’s Complement**: Negative numbers are formed by using a sign bit and subtracting 1 from the positive value, then inverting all bits.
<!--SR:!2025-08-18,131,290-->

What is the components of a floating-point representation?
?
1. **Sign bit**: Indicates the sign (positive or negative).
2. **Mantissa**: Represents the significant digits.
3. **Exponent**: (minus the bias/offset) - Specifies the power of 2.
<!--SR:!2025-10-10,157,270-->

What are the optimizations in floating-point representation?
?
4. **Normalization**: Eliminates leading zeros in the mantissa by adjusting the exponent.
5. **Implicit MSB**: Omits the leading 1 in the mantissa for normalized numbers.
6. **Exponent Bias**: Adds a bias/offset to the exponent for easier comparisons.
<!--SR:!2025-12-16,204,270-->

**What is sign extension?**::Sign extension increases the size of a signed binary number by copying the sign bit to the extended bits to preserve its value.
<!--SR:!2025-12-08,239,330-->

**In two’s complement, to represent a negative number, subtract ==1== from the positive value, then ==invert all bits==.**
<!--SR:!2026-02-17,287,330!2026-01-14,267,337-->

**Normalization in floating-point representation ensures the mantissa always starts with a leading ==1==.**
<!--SR:!2025-06-23,33,250-->

**The IEEE 754 standard specifies single precision as ==32 bits== and double precision as ==64 bits==.**
<!--SR:!2026-02-02,272,337!2026-02-28,298,337-->

**What is precision loss in floating-point arithmetic?**::Some decimal numbers cannot be exactly represented in binary (e.g., 0.1), which leads to inaccuracies.
<!--SR:!2025-09-11,87,308-->

**What happens to floating-point precision as numbers get larger?**::The difference between consecutive representable numbers increases, making small changes undetectable.
<!--SR:!2026-01-05,244,348-->

**Why is floating-point addition not associative?**:: Rounding imprecision  cause `(a + b) + c ≠ a + (b + c)` in some cases, especially for large (absolute value) numbers.
<!--SR:!2026-02-23,278,347-->

## Stack Machines


**What is infix notation?**::Infix notation is the standard mathematical notation where operators are placed between operands (e.g., `3 + 4 × 2 = 11`).
<!--SR:!2026-04-24,346,350-->

**How is the expression (in infix notation): `3 + (4 × 2)`, written in RPN?**::`3 4 2 × +`
<!--SR:!2025-07-08,43,228-->

**What is Polish Notation (prefix notation)?**::A notation where the operator precedes the operands (e.g., `+ 3 × 4 2 = 11`).
<!--SR:!2025-10-05,111,310-->

**What is a stack machine?**::A computational model that primarily uses a stack for executing instructions.
<!--SR:!2025-09-08,152,310-->

**How do operations work in a stack machine?**::Operands are pushed onto a stack, operations pop operands, compute results, and push them back onto the stack.
<!--SR:!2025-12-29,237,330-->

How is Reverse Polish Notation (RPN) evaluated using stack operations?
?
7. Read tokens from left to right.
8. Push operands onto a stack.
9. When an operator is encountered:
   - Pop the required number of operands.
   - Perform the operation.
   - Push the result back onto the stack.
10. The final value in the stack is the result.
<!--SR:!2025-06-24,47,270-->

**In infix notation, operators are placed ==between== operands, requiring parentheses for clarity due to ==precedence== and ==associativity== rules.**
<!--SR:!2026-03-20,318,345!2026-03-11,309,345!2026-04-04,331,350-->

## Simple Model of A Processor


**What is the purpose of the program counter (PC)?**::It stores the address of the next instruction to be executed.
<!--SR:!2026-03-22,320,347-->

**How does a processor handle branching instructions?**::The program counter is set to a new destination instead of incrementing sequentially.
<!--SR:!2025-10-08,114,308-->

**What does the clock rate describe?**::It describes how fast the control unit synchronizes instructions via pulses (not the speed of a fetch-decode-execute cycle)
<!--SR:!2026-03-14,312,348-->

**What does the instruction rate measure?**::The number of instructions executed per second.
<!--SR:!2026-04-19,341,350-->

**Why is the instruction rate not an exact measure of fetch-decode-execute speed?**::Because different instructions take varying numbers of clock cycles.
<!--SR:!2025-12-22,230,328-->

Describe the fetch-decode-execute cycle.
?
1. **Fetch**: Get the instruction from memory at the program counter address.
2. **Decode**: Determine the instruction type and its operands.
3. **Execute**:
   - Perform the computation.
   - Read/write registers or interact with coprocessors.
   - Update the program counter for the next instruction or a branch.
<!--SR:!2025-08-13,135,307-->

**The three stages of instruction execution are ==fetch==, ==decode==, and ==execute==.**
<!--SR:!2026-03-18,316,345!2026-03-18,316,347!2025-12-28,234,325-->

**What is the difference between registers and memory?**::Registers are small, fast storage units inside the CPU that hold temporary data for immediate processing, while memory (RAM) is larger, slower storage located outside the CPU, used to store program instructions and data for active processes.
<!--SR:!2026-06-11,386,367-->