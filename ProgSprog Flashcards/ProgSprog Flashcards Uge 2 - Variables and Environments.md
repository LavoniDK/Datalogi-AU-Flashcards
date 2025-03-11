____
#flashcards/ProgSprog/2_Variables-and-Environments  

## Operational Semantics

What is operational semantics?::Operational semantics defines the meaning of a programming language by describing how each statement or expression executes on an abstract machine, providing a step-by-step execution model.
<!--SR:!2025-04-10,45,290-->

How are arithmetic expressions evaluated in MiniScala using inference rules?
?
Inference rules specify how an expression is evaluated by breaking it into smaller sub-expressions. Example:
$$
\frac{\vdash e_{1}\Rightarrow v_{1} \quad \vdash e_{2}\Rightarrow v_{2} \quad v = v_{1}+v_{2}}{\vdash e_{1}\textcolor{blue}{+} e_{2}\Rightarrow v}
$$
(Where blue symbols denote MiniScala syntax and black symbols denote meta-language notation.)
<!--SR:!2025-04-10,45,290-->

What are two key properties of operational semantics?
?
  - **Determinism**: Each expression evaluates to at most one value.
  - **Totality**: Every valid expression evaluates to a result in a finite number of steps.
<!--SR:!2025-05-06,66,318-->

What is a variable environment ($VarEnv$)?::A variable environment ($VarEnv$) is a partial function mapping variables to values: $VarEnv: Var \hookrightarrow \mathbb{Z}$.
<!--SR:!2025-04-21,56,310-->

How does operational semantics extend to handle variables?
?
The semantic judgment for evaluating a variable expression includes a variable environment:
$$\frac{\rho (x) = v}{\rho \vdash x \Rightarrow v}$$
where $\rho$ maps variables to values and $x\in Var, \rho \in VarEnv$.
<!--SR:!2025-03-28,32,276-->


How does MiniScala handle variable declarations?
?
A `val` declaration binds an identifier to a value, modifying the environment:
$$\frac{ \rho \vdash e \Rightarrow v \quad \quad \rho' = \rho[x \mapsto v] }{ \rho \vdash \textcolor{blue}{val} \ x \textcolor{blue}{=} e \Rightarrow \rho' }$$
<!--SR:!2025-03-27,31,270-->

What is a free variable?::A free variable is a variable that appears in an expression but is not bound by a local (determined by scope) definition or quantifier.
<!--SR:!2025-04-26,60,310-->


What is the result of the following `freeVars` computation? `freeVars(z + { val x = y + 1; x * x }) =`==` {y, z}`==
<!--SR:!2025-05-07,67,317-->

## Inductive Data Types

What is an `IntList` in functional programming?
?
An `IntList` is an inductive data type where:
  - `x::xs` represents a list where `x` is the first element and `xs` is the rest of the list.
  - `Nil` represents an empty list.
  - The list can be recursively defined and processed using pattern matching.
<!--SR:!2025-04-22,57,315-->

What is structural recursion?::Structural recursion is a recursion pattern where a function decomposes a data structure and applies itself recursively to subcomponents. It is commonly used in functional programming for processing lists and trees.
<!--SR:!2025-04-09,44,295-->

How does pattern matching work in functional programming?::Pattern matching allows **destructuring** values by branching on type variants and extracting sub-values, binding them to local variables based on the pattern.
<!--SR:!2025-03-19,27,297-->
