____
#flashcards/ComArk/3_The-Digital-Level 

## Digital Logic

What distinguishes digital computers from analog computers?::Digital computers operate on discrete values, while analog computers handle continuously varying data.
<!--SR:!2025-11-27,198,314-->

What is the fundamental component of digital circuits?::A Metal Oxide Semiconductor Field Effect Transistor (MOSFET).
<!--SR:!2025-11-22,169,270-->

What are the three terminals of a MOSFET?::Source, Drain, and Gate.
<!--SR:!2025-08-12,121,290-->

What Boolean functions can be used to implement any Boolean function?
?
- `AND` and `NOT` gates
- `OR` and `NOT` gates
- `NAND` gates
- `NOR` gates.
Because of the expressiveness of `NAND` and `NOR` gates, they are known as **universal gates**.
<!--SR:!2025-11-03,181,310-->

What does a Half Adder compute?::Sum and carry for two input bits.
<!--SR:!2025-08-14,114,290-->

What does a Full Adder handle?::Carry from previous additions, as well as addition, forming multi-bit adders.
<!--SR:!2025-11-30,200,312-->

## Boolean Algebra

Why is it useful to represent logical operations with mathematical equations?::Because it allows us to simplify and manipulate logical expressions and design digital circuits systematically and efficiently.
<!--SR:!2025-12-11,198,310-->

$\overline{\overline{x}} = x$ is an example of what?:negation being **involutive**.


$\overline{x + y} =  \overline{xy}$ is known as ==De Morgans Law==.
<!--SR:!2025-08-09,109,290-->

$x(y + z) = xy + xz$ is known as ==Distributivity==.
<!--SR:!2025-12-27,204,314-->

The theorem $x + \overline{x} = 1$ is the ==excluded middle==, and the theorem $x\overline{x} = 0$ is the ==contradiction==.
<!--SR:!2026-01-16,253,334!2025-10-26,173,310-->

## Stateful Digital Systems

What is the key difference between combinational and sequential circuits?::Combinational circuits' outputs depend only on current inputs, while sequential circuits' outputs depend on both current inputs and previous states.
<!--SR:!2025-08-11,111,293-->

How does an SR latch differ from a combinational circuit?::The outputs of the latch are not uniquely determined by the current inputs; it maintains state.
<!--SR:!2025-08-16,116,290-->

What problem does a clocked SR latch solve?::Prevents unintended state changes by allowing transitions only at specific times.
<!--SR:!2025-10-19,135,270-->

What is a flip-flop?::An edge-triggered memory element.
<!--SR:!2025-11-22,193,310-->

How does a flip-flop differ from a latch?::Flip-flops transition state only on clock edges (rising or falling), while latches respond to level changes.
<!--SR:!2026-02-15,266,330-->

What is the function of a multiplexer (MUX)?::Selects one of multiple input signals and forwards it to the output based on control signals.
<!--SR:!2025-09-17,157,313-->

What is another way to describe what a multiplexer does::It functions as a conditional switch in circuits.
<!--SR:!2025-08-12,86,254-->

What is the function of a decoder?::Converts an n-bit input into $2^n$ unique output lines.
<!--SR:!2025-06-28,53,270-->

What is a common use of decoders?::Address decoding (e.g., selecting memory locations).
<!--SR:!2025-06-18,43,250-->

What can decoders implement, and how?::Sequential execution, by activating components in a predefined order, by using a **counter** which feeds into the **decoder**, and the decoder's outputs are wired to **control lines** for various components. As the counter increments, the decoder activates exactly one output at a time, triggering a specific action in the CPU's datapath.
<!--SR:!2025-06-27,21,214-->