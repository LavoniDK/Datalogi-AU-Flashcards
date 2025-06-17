___
#flashcards/ProgSprog/8_Lambda-Calculus 


What is the abstract syntax of untyped lambda calculus with call-by-value semantics?::$Exp::=Id\mid Id \Rightarrow Exp\mid Exp(Exp)$
<!--SR:!2025-06-05,7,238-->


How do we interpret programs in lambda calculus?
?
We interpret programs under an environment of identifiers:
$$
\begin{align}
&Env \vdash Exp \Rightarrow Val \\
&Env = Id \hookrightarrow Val \\
&Val = Id \times Exp \times Env \\
\end{align}
$$
<!--SR:!2025-07-02,29,252-->


How is function calling evaluated in lambda calculus(associativity and precedence rules)?
?
Function calling is left associative:
$$
e_1(e_2)(e_3) \equiv (e_1(e_2))(e_3) \not\equiv e_1((e_2)(e_3))
$$
Function call also has precedence over function definition:
$$
x \Rightarrow e_1(e_2) \equiv x \Rightarrow (e_1(e_2)) \not\equiv (x \Rightarrow e_1)(e_2)
$$
<!--SR:!2025-08-07,68,272-->


What is Church Encoding?
?
Church encoding is a way to represent data and operators in lambda calculus, ensuring that every encoded term can be decoded, and operations on decoded terms can also be performed on the encoded terms.
<!--SR:!2025-07-11,46,257-->


How are natural numbers represented in Church Encoding?
?
Natural numbers are represented in a successor-zero manner:
$$
\begin{align}
0 &\equiv s \Rightarrow z \Rightarrow z\\
1 &\equiv s \Rightarrow z \Rightarrow s(z)\\
2 &\equiv s \Rightarrow z \Rightarrow s(s(z))\\
\end{align}
$$
The value of a number is the amount of function applications.
<!--SR:!2025-07-03,59,310-->


How are Boolean values represented in Church Encoding?
?
Boolean values are lambda expressions that returns the first one if it represents true or the second on if it represents false. Thereby making them useful for constructing if-then-else clauses:
$$
\begin{align}
true &\equiv t \Rightarrow e \Rightarrow t \\
false &\equiv t \Rightarrow e \Rightarrow e \\
\end{align}
$$
<!--SR:!2025-06-04,22,257-->


How can logical operations be represented in Church Encoding?
?
$$
\begin{align}
\text{if }(e_1)e_{2}\text{ else }e_{3} &\equiv e_{1}(e_{2})(e_{3})\\
e_{1} \land e_{2}&\equiv e_{1}(e_{2})(t \Rightarrow e \Rightarrow e) \\
e_{1} \lor e_{2}&\equiv e_{1}(t \Rightarrow e \Rightarrow t)(e_{2})\\
!e &\equiv e(t \Rightarrow e \Rightarrow e)(t \Rightarrow e \Rightarrow t)
\end{align}
$$
Inherently both branches is always evaluated before being passed to the function (call-by-value), if this is a problem, then it can be solved by [[Functional Programming#Call-by-Name|thunking]].
<!--SR:!2025-07-21,55,257-->


How are pairs represented in Church Encoding?
?
Pairs are functions that take a selector function and apply it to both elements:
$$
\begin{align}
(e_{1}, e_{2}) &\equiv p \Rightarrow p(e_1)(e_{2}) \\
e[1] &\equiv e(x \Rightarrow y \Rightarrow x) \\
e[2] &\equiv e(x \Rightarrow y \Rightarrow y)
\end{align}
$$
<!--SR:!2025-06-06,11,232-->

**How is recursion handled in lambda calculus?**
?
Recursion is achieved using a **fixed-point combinator**, such as the **Turing fixed-point combinator** `fix`. In call-by-value style, recursion can be expressed as:
$$
\{\text{def } f(x) = e_1 ; e_2 \} \Rightarrow (f \Rightarrow e_2)\big(\text{fix}(f \Rightarrow x \Rightarrow e_1)\big)
$$
This transforms a recursive function definition into a form where `fix` produces a **self-referential function**.
<!--SR:!2025-06-15,41,270-->


How is type checking introduced in lambda calculus?
?
Types are introduced as tagged values where the tag represents the type and the value holds the data. Type correctness is ensured by checking the type tags before performing operations.
<!--SR:!2025-06-12,38,292-->
