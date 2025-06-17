____

#flashcards/ProgSprog/3_Type-Checking  


When designing a new language construct, what three things do we need to consider?::Grammar, Type Rules, and Operational Semantics.
<!--SR:!2026-01-16,253,336-->

What aspect of a language construct is addressed by Grammar?::Syntax.
<!--SR:!2026-03-18,288,337-->

What aspect of a language construct is addressed by Type Rules?::Static Semantics.
<!--SR:!2026-02-28,275,337-->

What aspect of a language construct is addressed by Operational Semantics?::Dynamic Semantics.
<!--SR:!2025-08-19,120,292-->

What language features become relevant when a programming language has multiple types?::Operator Overloading and Type Coercion.
<!--SR:!2025-11-05,181,317-->

What is type coercion?::The implicit (automatic) or explicit (by casting) conversion of one data type into another to perform an operation.
<!--SR:!2025-12-16,199,312-->

What does the zero tuple `()` represent?::a dummy output (Unit in Scala, Void in other languages).
<!--SR:!2025-06-04,69,317-->



If $$ \begin{aligned} &\rho \text{ is a variable environment:} \quad &\rho \in \textit{VarEnv} = \textit{Var} \hookrightarrow \textit{Val} \\ &v \text{ is a value:} \quad &v \in \textit{Val} = \mathbb{Z} \cup \mathbb{B} \end{aligned} $$how is $\textit{Val}$ extended to account for tuples, with integers and/or booleans?
?
- $\mathbb{Z} \subseteq \textit{Val}$ and $\mathbb{B} \subseteq \textit{Val}$
- if $v_1 \in \textit{Val}$ and $v_2 \in \textit{Val}$, then $(v_1, v_2) \in \textit{Val}$
<!--SR:!2025-10-24,172,316-->


What does a simple type system consist of?::An environment that maps variable names to their types.
<!--SR:!2025-08-16,117,292-->

What must be true with dynamic type checking, and where annoted types is available also must be true with static type checking?::annoted type must match the inferred type to be legal.
<!--SR:!2025-06-11,11,312-->

How are dynamic typechecking rules structured in MiniScala?
?
- Evaluate an expression in the interpreter
- Update environements according to the type of expression
- If the expression has type annotation, check if the types of the interpreted program match the annotated types.
- This is for example used in type-annotated value-, variable- and function declarations.
<!--SR:!2025-06-09,9,292-->

Type errors can cause a derivation tree, based on our operational semantics, to become ==stuck==
<!--SR:!2026-02-06,256,330-->

When we check for type errors during run-time, we are evaluating ==dynamic semantics==.
<!--SR:!2026-02-24,285,337-->

$VarTypeEnv \vdash Decl:VarTypeEnv$ represents how ==variable declarations== updates our ==type system environment==
<!--SR:!2026-03-24,294,337!2026-03-11,284,336-->

If expressions of a particular type evaluates to value with the same type, then we say that our type system and operational semantic has the property of ==type preservation==
<!--SR:!2025-09-22,140,296-->