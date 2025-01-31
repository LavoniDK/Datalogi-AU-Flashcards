___

#flashcards/ComArk/Uge1 
### Single-line Flashcards

**What is a bit?**::A bit represents a binary digit, either 0 or 1.
<!--SR:!2025-02-01,4,270-->

**What is a byte?**::A byte is the smallest unit of data larger than a bit that hardware can manipulate, typically consisting of 8 bits.
<!--SR:!2025-02-01,4,270-->

**How many values can a byte of size k represent?**::$2^k$ values.
<!--SR:!2025-02-01,4,270-->

**How many distinct values can an 8-bit byte represent?**::256 distinct values.
<!--SR:!2025-02-01,4,277-->

**What is the Most Significant Bit (MSB)?**::The leftmost bit in a binary number.
<!--SR:!2025-02-01,4,270-->

**What is the Least Significant Bit (LSB)?**::The rightmost bit in a binary number.
<!--SR:!2025-02-01,4,277-->

**What prefix is used for hexadecimal constants?**::`0x`
<!--SR:!2025-02-01,4,270-->

**What prefix is used for binary constants?**::`0b`
<!--SR:!2025-02-01,4,282-->

**What is ASCII?**::ASCII is a 7-bit standard for encoding characters, often extended to 8 bits for modern systems.
<!--SR:!2025-02-01,4,270-->

**What is Unicode used for?**::Unicode expands character representation beyond ASCII, enabling multilingual support with larger bit encodings.
<!--SR:!2025-01-31,3,257-->

**What are unsigned integers?**::Numbers that represent only non-negative values.
<!--SR:!2025-02-01,4,277-->

**What is overflow?**::It occurs when a calculation exceeds the representable range.
<!--SR:!2025-02-01,4,277-->

**What is underflow?**::It occurs when a calculation is smaller than the smallest representable value.
<!--SR:!2025-01-31,3,250-->

**What is endianness?**
?
Endianness is the order in which bytes are arranged in memory:
- **Little-endian**: The least significant byte is stored first.
- **Big-endian**: The most significant byte is stored first.
<!--SR:!2025-01-31,3,262-->

What are the three methods for representing signed binary integers?
?
1. **Sign-Magnitude**: Divides bits into a sign bit (1 for negative, 0 for positive) and magnitude bits (absolute value).
2. **One’s Complement**: Negative numbers are formed by using a sign bit and inverting all bits of the positive value.
3. **Two’s Complement**: Negative numbers are formed by using a sign bit and subtracting 1 from the positive value, then inverting all bits.
<!--SR:!2025-02-01,4,270-->

Explain floating-point representation components.
?
1. **Sign bit**: Indicates the sign (positive or negative).
2. **Mantissa**: Represents the significant digits.
3. **Exponent**: Specifies the power of 2.
<!--SR:!2025-01-31,2,230-->

What are the optimizations in floating-point representation?
?
1. **Normalization**: Eliminates leading zeros in the mantissa by adjusting the exponent.
2. **Implicit MSB**: Omits the leading 1 in the mantissa for normalized numbers.
3. **Exponent Bias**: Adds a bias to the exponent for easier comparisons.
<!--SR:!2025-01-31,3,250-->

**What is sign extension?**::Sign extension increases the size of a signed binary number by copying the sign bit to the extended bits to preserve its value.
<!--SR:!2025-02-01,4,270-->

**In two’s complement, to represent a negative number, subtract ==1== from the positive value, then ==invert all bits==.**
<!--SR:!2025-02-01,4,270!2025-02-01,4,277-->

**Normalization in floating-point representation ensures the mantissa always starts with a leading ==1==.**
<!--SR:!2025-02-01,3,250-->

**The IEEE 754 standard specifies single precision as ==32 bits== and double precision as ==64 bits==.**
<!--SR:!2025-02-01,4,277!2025-02-01,4,277-->

## Stack Machines


### Single-line Flashcards

**What is infix notation?**::Infix notation is the standard mathematical notation where operators are placed between operands (e.g., `3 + 4 × 2`).

**How is the expression `3 + (4 × 2)` written in RPN?**::`3 4 2 × +`

**What is Polish Notation (prefix notation)?**::A notation where the operator precedes the operands (e.g., `+ 3 × 4 2`).

**What is a stack machine?**::A computational model that primarily uses a stack for executing instructions.

**How do operations work in a stack machine?**::Operands are pushed onto a stack, operations pop operands, compute results, and push them back onto the stack.

**Why don't stack machines require registers?**::Because all computation happens via the stack without explicit operand addressing.

How is Reverse Polish Notation (RPN) evaluated using stack operations?
?
1. Read tokens from left to right.
2. Push operands onto a stack.
3. When an operator is encountered:
   - Pop the required number of operands.
   - Perform the operation.
   - Push the result back onto the stack.
4. The final value in the stack is the result.

**In infix notation, operators are placed ==between== operands, requiring parentheses for clarity due to ==precedence== and ==associativity== rules.**

## Simple Model of A Processor


**What is the purpose of the program counter (PC)?**::It stores the address of the next instruction to be executed.

**How does a processor handle branching instructions?**::The program counter is set to a new destination instead of incrementing sequentially.

**Does the clock rate describe the speed of a fetch-decode-execute cycle?**::No, it describes how fast the control unit synchronizes instructions via pulses.

**What does the instruction rate measure?**::The number of instructions executed per second, for a specific instruction.

**Why is instruction rate not an exact measure of fetch-decode-execute speed?**::Because different instructions take varying numbers of clock cycles.

Describe the fetch-decode-execute cycle.
?
1. **Fetch**: Get the instruction from memory at the program counter address.
2. **Decode**: Determine the instruction type and its operands.
3. **Execute**:
   - Perform the computation.
   - Read/write registers or interact with coprocessors.
   - Update the program counter for the next instruction or a branch.

**The three stages of instruction execution are ==fetch==, ==decode==, and ==execute==.**
