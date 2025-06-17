___
#flashcards/ProgSprog/9_Imperative-Programming 

## Syntax & Semantics

What new syntactic constructs are introduced to support mutation in MiniScala?::`var Id = Exp` for variable declarations and `Id = Exp` for assignments.
<!--SR:!2025-06-11,16,255-->

Why does the order of evaluation matter in imperative languages with side effects?::Because evaluating expressions may modify shared state, so different orders can lead to different results.
<!--SR:!2025-06-27,32,270-->

==Statements== are expressions mainly evaluated for their ==side effects==.
<!--SR:!2025-07-15,49,307!2025-07-13,43,291-->

==Procedures== are functions mainly evaluated for their ==side effects==.
<!--SR:!2025-06-13,24,270!2025-07-18,45,295-->

What syntactic extensions are added for sequencing and control structures in expressions?::Block expressions `{ Exp ; Exp }` and loops `while (Exp) Exp`.
<!--SR:!2025-06-12,22,250-->

## Environment-Store Semantics

What structure do we use to maintain state when evaluating side-effecting expressions?::The **Environment-Store** model.
<!--SR:!2025-06-29,33,271-->

What does the store represent in the Environment-Store model?::A mapping from locations to values that tracks mutable state across evaluation steps.
<!--SR:!2025-06-25,30,271-->

==The environment== maps identifiers to ==values or locations==, while the ==store== maps locations to ==values==.
<!--SR:!2025-07-14,48,307!2025-07-05,38,295!2025-07-09,44,307!2025-07-07,42,290-->

What is the purpose of the store in operational semantics?::The store in operational semantics records changes from assignments and ensures all parts of a program see a consistent view of memory during evaluation.
<!--SR:!2025-06-14,19,255-->

In the Environment-Store model, what does the evaluation of expressions and declarations yield?::A value and updated store for expressions, and an updated environment and store for declarations.
<!--SR:!2025-07-17,44,267-->

How is a `val x = e` declaration evaluated?::First evaluate $e$ to value $v$, then extend the environment with $x ↦ v$.
<!--SR:!2025-06-22,24,255-->

How is a `var x = e` declaration evaluated?::Evaluate `e` to `v`, allocate a fresh location `ℓ`, bind `x ↦ ℓ` in the environment, and store `ℓ ↦ v`.
<!--SR:!2025-06-16,21,251-->

What is the key difference between reading a `val` and a `var` identifier?::Reading a `val` retrieves a value directly from the environment, while reading a `var` involves following a location in the store.
<!--SR:!2025-07-30,57,311-->

==Environments== reflect ==static scoping== while ==Stores== reflect ==dynamic execution== structure.
<!--SR:!2025-06-06,17,267!2025-06-16,26,287!2025-07-29,56,315!2025-06-04,15,295-->

## Type System Extension

What type is introduced to support side-effect-only expressions?::`Unit` - The empty tuple.
<!--SR:!2025-07-11,45,291-->

How are `var` identifiers represented in the type system?::As `Mut(τ)`, indicating a mutable value stored in the store.
<!--SR:!2025-06-30,34,271-->

$Mut(τ)$ is used only in the ==type checker== and not in the syntax or interpreter.
<!--SR:!2025-06-12,12,251-->

## Mutation-based Recursion

How does MiniScala implement recursion using mutation?::By first building the closures without recursive environments and then overwrite the `env` field in each closure, pointing to the new environment.
<!--SR:!2025-07-15,42,252-->

Why is mutation-based recursion preferred over higher-order/lazy recursion in this case?::It’s simpler and more efficient.
<!--SR:!2025-06-05,16,295-->

==Mutual- and self-recursion== can be enabled by mutating the environment instead of using ==lazy higher-order functions==.
<!--SR:!2025-06-29,33,270!2025-06-17,27,287-->
