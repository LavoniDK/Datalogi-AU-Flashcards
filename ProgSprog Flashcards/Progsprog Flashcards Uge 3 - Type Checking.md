____

#flashcards/ProgSprog/3_Type-Checking  


When designing a new language construct, what three things do we need to consider?::Grammar, Type Rules, and Operational Semantics.
<!--SR:!2025-05-08,58,316-->

What aspect of a language construct is addressed by Grammar?::Syntax.
<!--SR:!2025-03-13,16,297-->

What aspect of a language construct is addressed by Type Rules?::Static Semantics.
<!--SR:!2025-03-13,16,297-->

What aspect of a language construct is addressed by Operational Semantics?::Dynamic Semantics.
<!--SR:!2025-04-21,41,292-->

What language features become relevant when a programming language has multiple types?::Operator Overloading and Type Coercion.
<!--SR:!2025-05-07,57,317-->

What is type coercion?::The implicit (automatic) or explicit (by casting) conversion of one data type into another to perform an operation.
<!--SR:!2025-03-12,16,292-->

What does the zero tuple `()` represent?::a dummy output (Unit in Scala, Void in other languages).
<!--SR:!2025-03-13,16,297-->



If $$ \begin{aligned} &\rho \text{ is a variable environment:} \quad &\rho \in \textit{VarEnv} = \textit{Var} \hookrightarrow \textit{Val} \\ &v \text{ is a value:} \quad &v \in \textit{Val} = \mathbb{Z} \cup \mathbb{B} \end{aligned} $$how is $\textit{Val}$ extended to account for tuples, with integers and/or booleans?
?
- $\mathbb{Z} \subseteq \textit{Val}$ and $\mathbb{B} \subseteq \textit{Val}$
- if $v_1 \in \textit{Val}$ and $v_2 \in \textit{Val}$, then $(v_1, v_2) \in \textit{Val}$
<!--SR:!2025-04-22,42,296-->


What does a simple type system consist of?::An environment that maps variable names to their types.
<!--SR:!2025-04-20,40,292-->

What must be true with dynamic type checking, and where there annoted type is avalible?:annoted type must match the inferred type to be legal.

Type errors can cause a derivation tree, based on our operational semantics, to become ==stuck==
<!--SR:!2025-03-12,15,290-->

When we check for type errors during run-time, we are evaluating ==dynamic semantics==.
<!--SR:!2025-05-15,65,317-->

$VarTypeEnv \vdash Decl:VarTypeEnv$ represents how ==variable declarations== updates our ==type system environment==
<!--SR:!2025-03-13,16,297!2025-03-13,16,296-->

If expressions of a particular type evaluates to value with the same type, then we say that our type system and operational semantic has the property of ==type preservation==
<!--SR:!2025-04-27,47,296-->