___

#flashcards/ComArk/Uge1 

## Data Representation

**What is a byte?**::A byte is the smallest unit of data larger than a bit that hardware can manipulate, typically consisting of 8 bits.
<!--SR:!2025-02-15,14,290-->

**How many values can a byte of size $k$ represent?**::$2^k$ values.
<!--SR:!2025-02-15,14,290-->

**What is the Most Significant Bit (MSB)?**::The leftmost bit in a binary number.
<!--SR:!2025-02-15,14,290-->

**What is the Least Significant Bit (LSB)?**::The rightmost bit in a binary number.
<!--SR:!2025-02-17,16,297-->

**What prefix is used for hexadecimal constants?**::`0x`
<!--SR:!2025-02-16,15,290-->

**What prefix is used for binary constants?**::`0b`
<!--SR:!2025-02-18,17,302-->

**What is ASCII?**::ASCII is a 7-bit standard for encoding characters, often extended to 8 bits for modern systems.
<!--SR:!2025-02-17,16,290-->

**What is Unicode used for?**::Unicode expands character representation beyond ASCII, enabling multilingual support with larger bit encodings.
<!--SR:!2025-02-11,11,277-->

**What are unsigned integers?**::Numbers that represent only non-negative values.
<!--SR:!2025-02-16,15,297-->

**What is overflow?**::It occurs when a calculation exceeds the representable range.
<!--SR:!2025-02-17,16,297-->

**What is underflow?**::It occurs when a calculation is smaller than the smallest representable value.
<!--SR:!2025-02-12,12,270-->

**What is endianness?**
?
Endianness is the order in which bytes are arranged in memory:
- **Little-endian**: The least significant byte is stored first.
- **Big-endian**: The most significant byte is stored first.
<!--SR:!2025-02-08,8,262-->

What are the three methods for representing signed binary integers?
?
1. **Sign-Magnitude**: Divides bits into a sign bit (1 for negative, 0 for positive) and magnitude bits (absolute value).
2. **One’s Complement**: Negative numbers are formed by using a sign bit and inverting all bits of the positive value.
3. **Two’s Complement**: Negative numbers are formed by using a sign bit and subtracting 1 from the positive value, then inverting all bits.
<!--SR:!2025-02-13,12,270-->

What is the components of a floating-point representation?
?
1. **Sign bit**: Indicates the sign (positive or negative).
2. **Mantissa**: Represents the significant digits.
3. **Exponent**: (minus the bias/offset) - Specifies the power of 2.
<!--SR:!2025-02-22,17,250-->

What are the optimizations in floating-point representation?
?
4. **Normalization**: Eliminates leading zeros in the mantissa by adjusting the exponent.
5. **Implicit MSB**: Omits the leading 1 in the mantissa for normalized numbers.
6. **Exponent Bias**: Adds a bias/offset to the exponent for easier comparisons.
<!--SR:!2025-02-08,8,250-->

**What is sign extension?**::Sign extension increases the size of a signed binary number by copying the sign bit to the extended bits to preserve its value.
<!--SR:!2025-02-15,14,290-->

**In two’s complement, to represent a negative number, subtract ==1== from the positive value, then ==invert all bits==.**
<!--SR:!2025-02-17,16,290!2025-02-16,15,297-->

**Normalization in floating-point representation ensures the mantissa always starts with a leading ==1==.**
<!--SR:!2025-02-13,12,270-->

**The IEEE 754 standard specifies single precision as ==32 bits== and double precision as ==64 bits==.**
<!--SR:!2025-02-16,15,297!2025-02-17,16,297-->

**What is precision loss in floating-point arithmetic?**::Some decimal numbers cannot be exactly represented in binary (e.g., 0.1), which leads to inaccuracies. 
<!--SR:!2025-02-20,13,308-->

**What happens to floating-point precision as numbers get larger?**::The difference between consecutive representable numbers increases, making small changes undetectable.
<!--SR:!2025-02-20,13,308-->

**Why is floating-point addition not associative?**:: Rounding imprecision  cause `(a + b) + c ≠ a + (b + c)` in some cases, especially for large (absolute value) numbers.
<!--SR:!2025-02-08,4,307-->

## Stack Machines


**What is infix notation?**::Infix notation is the standard mathematical notation where operators are placed between operands (e.g., `3 + 4 × 2 = 11`).
<!--SR:!2025-02-21,17,310-->

**How is the expression (in infix notation): `3 + (4 × 2)`, written in RPN?**::`3 4 2 × +`
<!--SR:!2025-02-07,3,248-->

**What is Polish Notation (prefix notation)?**::A notation where the operator precedes the operands (e.g., `+ 3 × 4 2 = 11`).
<!--SR:!2025-02-21,17,310-->

**What is a stack machine?**::A computational model that primarily uses a stack for executing instructions.
<!--SR:!2025-02-15,12,290-->

**How do operations work in a stack machine?**::Operands are pushed onto a stack, operations pop operands, compute results, and push them back onto the stack.
<!--SR:!2025-02-20,16,310-->

How is Reverse Polish Notation (RPN) evaluated using stack operations?
?
7. Read tokens from left to right.
8. Push operands onto a stack.
9. When an operator is encountered:
   - Pop the required number of operands.
   - Perform the operation.
   - Push the result back onto the stack.
10. The final value in the stack is the result.
<!--SR:!2025-02-15,12,290-->

**In infix notation, operators are placed ==between== operands, requiring parentheses for clarity due to ==precedence== and ==associativity== rules.**
<!--SR:!2025-02-21,17,305!2025-02-21,17,305!2025-02-21,17,310-->

## Simple Model of A Processor


**What is the purpose of the program counter (PC)?**::It stores the address of the next instruction to be executed.
<!--SR:!2025-02-21,17,307-->

**How does a processor handle branching instructions?**::The program counter is set to a new destination instead of incrementing sequentially.
<!--SR:!2025-02-21,17,308-->

**What does the clock rate describe?**::It describes how fast the control unit synchronizes instructions via pulses, not the speed of a fetch-decode-execute cycle.
<!--SR:!2025-02-20,16,308-->

**What does the instruction rate measure?**::The number of instructions executed per second.
<!--SR:!2025-02-21,17,310-->

**Why is the instruction rate not an exact measure of fetch-decode-execute speed?**::Because different instructions take varying numbers of clock cycles.
<!--SR:!2025-02-21,17,308-->

Describe the fetch-decode-execute cycle.
?
11. **Fetch**: Get the instruction from memory at the program counter address.
12. **Decode**: Determine the instruction type and its operands.
13. **Execute**:
   - Perform the computation.
   - Read/write registers or interact with coprocessors.
   - Update the program counter for the next instruction or a branch.
<!--SR:!2025-02-14,11,287-->

**The three stages of instruction execution are ==fetch==, ==decode==, and ==execute==.**
<!--SR:!2025-02-20,16,305!2025-02-21,17,307!2025-02-21,17,305-->

**What is the difference between registers and memory?**::Registers are small, fast storage units inside the CPU that hold temporary data for immediate processing, while memory (RAM) is larger, slower storage located outside the CPU, used to store program instructions and data for active processes.
<!--SR:!2025-02-08,4,307-->