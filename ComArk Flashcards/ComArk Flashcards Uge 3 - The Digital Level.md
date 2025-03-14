____
#flashcards/ComArk/3_The-Digital-Level 

## Digital Logic

What distinguishes digital computers from analog computers?::Digital computers operate on discrete values, while analog computers handle continuously varying data.
<!--SR:!2025-05-13,63,314-->

What is the fundamental component of digital circuits?::A Metal Oxide Semiconductor Field Effect Transistor (MOSFET).
<!--SR:!2025-03-25,24,270-->

What are the three terminals of a MOSFET?::Source, Drain, and Gate.
<!--SR:!2025-04-02,32,270-->

What Boolean functions can be used to implement any Boolean function?
?
- `AND` and `NOT` gates
- `OR` and `NOT` gates
- `NAND` gates
- `NOR` gates.
Because of the expressiveness of `NAND` and `NOR` gates, they are known as **universal gates**.
<!--SR:!2025-04-25,45,290-->

What does a Half Adder compute?::Sum and carry for two input bits.
<!--SR:!2025-04-19,39,290-->

What does a Full Adder handle?::Carry from previous additions, as well as addition, forming multi-bit adders.
<!--SR:!2025-05-14,64,312-->

## Boolean Algebra

Why is it useful to represent logical operations with mathematical equations?::Because it allows us to simplify and manipulate logical expressions and design digital circuits systematically and efficiently.
<!--SR:!2025-03-12,16,290-->

$\overline{\overline{x}} = x$ is an example of what?:negation being **involutive**.


$\overline{x + y} =  \overline{xy}$ is known as ==De Morgans Law==.
<!--SR:!2025-04-18,38,290-->

$x(y + z) = xy + xz$ is known as ==Distributivity==.
<!--SR:!2025-03-12,16,294-->

The theorem $x + \overline{x} = 1$ is the ==excluded middle==, and the theorem $x\overline{x} = 0$ is the ==contradiction==.
<!--SR:!2025-05-08,58,314!2025-04-23,43,290-->

## Stateful Digital Systems

What is the key difference between combinational and sequential circuits?::Combinational circuits' outputs depend only on current inputs, while sequential circuits' outputs depend on both current inputs and previous states.
<!--SR:!2025-04-19,39,293-->

How does an SR latch differ from a combinational circuit?::The outputs of the latch are not uniquely determined by the current inputs; it maintains state.
<!--SR:!2025-04-20,40,290-->

What problem does a clocked SR latch solve?::Prevents unintended state changes by allowing transitions only at specific times.
<!--SR:!2025-03-17,6,250-->

What is a flip-flop?::An edge-triggered memory element.
<!--SR:!2025-05-12,62,310-->

How does a flip-flop differ from a latch?::Flip-flops transition state only on clock edges (rising or falling), while latches respond to level changes.
<!--SR:!2025-03-12,16,290-->

What is the function of a multiplexer (MUX)?::Selects one of multiple input signals and forwards it to the output based on control signals.
<!--SR:!2025-04-09,38,293-->

What is another way to describe what a multiplexer does::It functions as a conditional switch in circuits.
<!--SR:!2025-03-19,18,254-->

What is the function of a decoder?::Converts an n-bit input into $2^n$ unique output lines.
<!--SR:!2025-04-10,30,270-->

What is a common use of decoders?::Address decoding (e.g., selecting memory locations).
<!--SR:!2025-04-11,31,270-->

What can decoders implement, and how?::Sequential execution, by activating components in a predefined order.
<!--SR:!2025-04-01,31,274-->