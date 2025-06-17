___
#flashcards/ProgSprog/13-14_Abstract-Machine-Code-and-Compilation

## Abstract Machine Code

What is abstract machine code?::An imperative, low-level, compiled language resembling machine code, but without high-level features.
<!--SR:!2025-06-16,20,266-->

Where does abstract machine code run?::On abstract machines, which are software-based interpreters, often called virtual machines.
<!--SR:!2025-06-07,12,246-->

What is just-in-time compilation in the context of abstract machines?::The method of compiling abstract machine code to real machine code at execution time.
<!--SR:!2025-06-23,27,286-->

## Stack Machines

Why is MiniScala's abstract machine designed as a stack machine?::Because MiniScala execution follows a stack discipline in expression evaluation, scoping, and function calls.
<!--SR:!2025-07-01,31,285-->

What are the three types of stacks in MiniScala's stack machine?::Operand stack, environment stack, and call stack.
<!--SR:!2025-07-01,31,286-->

What is reverse polish notation used for in stack machines?::To evaluate arithmetic expressions by traversing their ASTs in post-order.
<!--SR:!2025-06-08,5,206-->

What is the effect of executing an expression's instruction sequence in MiniScala's stack machine?::It pushes the result (exactly one value, so nested expressions are contracting) of the expression onto the operand stack. This reasoning can be applied inductively.
<!--SR:!2025-06-30,32,285-->

How are stacks represented in the abstract machine?::As lists, with the top of the stack being the leftmost element.
<!--SR:!2025-06-29,29,285-->

## Compilation to Stack Code

How is the process of compilation structured for MiniScala's abstract machine?::As a recursive function that decomposes expressions and translates them into operand and operator instructions.
<!--SR:!2025-06-10,10,226-->

## Compilation Correctness

What is the correctness condition for MiniScala v1 compilation?::$\mathrm{eval}(e) = \mathrm{execute}(\mathrm{compile}(e))$
<!--SR:!2025-06-20,22,250-->

Why is formal verification of compilation correctness important?::Because even established compilers like GCC can have incorrect compilations.
<!--SR:!2025-06-22,26,286-->

## Environment Stacks

What is the consequence of static scoping on environment stacks?::Because static scoping binds variables based on where code is written (not called), the **structure of the environment stack** matches the **nesting of expressions and blocks in the source code**.
<!--SR:!2025-06-04,6,206-->

What is the role of environment stacks in the abstract machine?::They track variable values at runtime using statically determined positions instead of names.
<!--SR:!2025-06-12,9,226-->

How are variable positions determined in the abstract machine?::Statically at compile-time.
<!--SR:!2025-06-10,15,250-->

What is each frame in an environment stack?::A list of variable values for one lexical scope.
<!--SR:!2025-06-04,6,210-->

## Imperative Language Features

What do we introduce to support imperative features in the abstract machine?::A store for mutable state and loops.
<!--SR:!2025-06-07,7,245-->

## Functions and Call Stacks

Why do we need an explicit call stack in the abstract machine?::To simulate function calls without relying on meta-language recursion.
<!--SR:!2025-06-11,16,265-->

What are the components of a stack frame in the call stack?::Code to be executed, operand stack, and environment stack.
<!--SR:!2025-06-09,9,206-->

What happens on a function call in the abstract machine?::A new stack frame is pushed and initialized.
<!--SR:!2025-06-12,17,266-->

What happens when a function returns?::The return value is popped from the operand stack, the stack frame is popped, and the value is pushed onto the operand stack.
<!--SR:!2025-06-08,13,246-->

## Tail Recursion

What is tail recursion?::A form of recursion where the recursive call is the last operation before returning.
<!--SR:!2025-06-07,12,246-->

Why is tail recursion important for abstract machine optimization?::Because it allows reuse of the current stack frame, avoiding the overhead of creating new ones.
<!--SR:!2025-06-14,18,266-->

What is a tail call?::A function call in tail position, meaning it is the final action in a function.
<!--SR:!2025-07-23,50,306-->

How does tail call optimization improve efficiency?::By reusing the current function's stack frame instead of allocating a new one.
<!--SR:!2025-06-21,25,286-->