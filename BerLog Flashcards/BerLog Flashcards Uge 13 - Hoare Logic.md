___
#flashcards/BerLog/13-Hoare-Logic 

## Syntax and Semantics

What is the structure of a Hoare Triple?::It has the form $\langle \varphi\rangle\ P\ \langle \psi\rangle$, where $\varphi$ is the precondition, $P$ is the program, and $\psi$ is the postcondition.
<!--SR:!2025-06-15,6,250-->

What does partial correctness mean in program logic?::If the program terminates, then the result satisfies the postcondition.
<!--SR:!2025-07-09,30,270-->

What does total correctness mean in program logic?::The program terminates and the result satisfies the postcondition.
<!--SR:!2025-07-26,47,290-->

What must be fixed to reason about semantics in Hoare Logic?
?
1. Semantics of the programming language (operational semantics)
2. Semantics of properties (first-order logic)
3. Semantics of Hoare Triples (partial/total correctness)
<!--SR:!2025-06-14,5,230-->

What is the role of variables in linking logic and programs?::They are commonly used in both and interpreted in $\mathbb{Z}$.
<!--SR:!2025-06-18,9,190-->

How is a program modeled mathematically?::As a partial function $\langle\langle C\rangle\rangle : L \triangleright^* L'$, mapping an initial state $L$ to a final state $L'$ if it terminates.
<!--SR:!2025-07-07,28,230-->

## Formal Definitions

What is the formal definition of partial correctness?
?
$$
\models_{\mathrm{par}}\langle\langle\varphi\rangle\rangle\ C\ \langle\langle\psi\rangle\rangle \iff \forall L.\; (\mathbb{Z},L \models \varphi) \Rightarrow (\forall L'.\; \langle\langle C \rangle\rangle : L \triangleright^* L' \Rightarrow (\mathbb{Z},L' \models \psi))$$
<!--SR:!2025-06-14,5,230-->

What is the formal definition of total correctness?
?
$$ \models_{\mathrm{tot}}\langle\langle\varphi\rangle\rangle\ C\ \langle\langle\psi\rangle\rangle \iff \forall L.\; (\mathbb{Z},L \models \varphi) \Rightarrow (\exists L'.\; \langle\langle C \rangle\rangle : L \triangleright^* L' \wedge (\mathbb{Z},L' \models \psi))$$
<!--SR:!2025-06-21,8,210-->

## Proof Rules

What do proof rules for Hoare Logic specify?::They define how to prove pre-/post-conditions for each programming construct, and include loop invariants for loops.
<!--SR:!2025-07-10,31,230-->

Are the proof rules of Hoare Logic sound and complete?::They are sound for partial correctness and relatively complete assuming arithmetic reasoning is decidable.
<!--SR:!2025-06-22,9,190-->

What is the general method to verify programs using Hoare Logic?::Use backwards reasoning from the outermost Hoare Triple, applying proof rules down to arithmetic statements, then check these in a prover.
<!--SR:!2025-06-16,19,250-->