____
#flashcards/ProgSprog/4_First-Order-Functions  

What is a function, as used in PLT?::a named, parameterized abstraction of an expression
<!--SR:!2025-09-09,112,310-->

What is the process of a function evaluation in the call-by-value strategy?::evaluate the argument, then pass the value to the formal parameter and evaluate the function body
<!--SR:!2025-06-05,30,235-->

How can type checking be compared to interpreting, and how do they differ?
?
Type checking is a sort of abstract interpretation of a program
They differ by the fact that type checking always terminate, and that the type checking of a function does not involve the function body, whereas the interpreter may go in an infinite loop and requires interpreting a functions body
<!--SR:!2025-09-20,117,294-->

What needs to be captured within the block to fully support mutual recursion?
?
The set of declarations within the block, which is some subset of $\mathcal{P}(Decl)$
<!--SR:!2026-02-13,269,330-->

What is the type of a function environment that supports free variables and mutual recursion?
?
$$FunEnv = Fun \rightarrow Var \times Exp \times VarEnv \times FunEnv \times \mathcal{P}(Decl)$$
<!--SR:!2025-06-14,62,270-->

How does MiniScala support lexical scoping in function calls?::Lexical scoping is supported by storing the variable- and function environments at the time of function declaration in the function closure, enabling correct resolution of free variables.
<!--SR:!2025-08-29,95,301-->

What is dynamic scoping, and how does it differ from lexical scoping?::Dynamic scoping determines a function's variable environment at the time of the function call, whereas lexical scoping determines it based on where the function is declared. Dynamic scoping makes program behavior difficult to understand and predict, as variable resolution depends on runtime context rather than static structure.
<!--SR:!2025-06-16,21,281-->
