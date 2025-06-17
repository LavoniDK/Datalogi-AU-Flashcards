___
#flashcards/BerLog/8_Turing-Machines

## Turing Machines

What is the Church-Turing Thesis?
?
The hypothesis that every effective procedure can be encoded as a Turing Machine; it posits that Turing Machines are as expressive as any mechanical model of computation.
<!--SR:!2025-07-10,46,295-->


What does a TM transition $q \xrightarrow{a/bR} q'$ mean?
?
- If $a$ under head, replace with $b$
- Move to state $q'$
- Move head right (R)
<!--SR:!2025-06-18,31,270-->


What is a recursively enumerable language?
?
A language $L$ such that $w \in L$ iff TM $M$ halts in $h_a$ on $w$. TM may reject or loop on $w \notin L$.
<!--SR:!2025-06-24,30,275-->

What is a recursive language?
?
A language $L$ is recursive if some TM $M$ decides it, i.e. always halts:
- $w \in L \Rightarrow M$ halts in $h_a$
- $w \notin L \Rightarrow M$ halts in $h_r$
<!--SR:!2025-07-06,42,295-->

What is the difference between acceptance and decision by a TM?
?
- Acceptance: TM halts in $h_a$
- Decision: TM halts in $h_a$ or $h_r$ (no looping)
<!--SR:!2025-06-28,34,275-->

How does a TM compute a partial function $f: (\Sigma^*)^k \hookrightarrow \Sigma^*$?
?
- Start with input $q_0 \Delta x_1 \Delta x_2 \ldots \Delta x_k \Delta$
- TM halts in $h_a \Delta f(x_1,\dots,x_k)\Delta$
- TM accepts iff $(x_1, ..., x_k) \in dom(f)$
<!--SR:!2025-07-28,49,255-->


What is the characteristic function $\chi_L$ of a language $L$?
?
$\chi_L(w) = 1$ if $w \in L$, otherwise 0
<!--SR:!2025-07-27,60,315-->


When is a language recursive in terms of characteristic function?
?
If and only if its characteristic function is computable by a TM
<!--SR:!2025-09-16,95,295-->


What are some variants of Turing Machines?
?
- Multi-track tape
- Infinite two-way tape
- Multi-tape
- Non-deterministic TM
- Acceptance by halting
<!--SR:!2025-07-08,44,290-->

Are all TM variants equivalent in power?
?
Yes, they all accept exactly the recursively enumerable languages
<!--SR:!2025-07-26,59,315-->

What is a composable TM?
?
A TM built from smaller, reusable TMs like:
- Copy, Insert, Erase, Reverse, Equal, etc.
Composed with $\rightarrow$ notation, e.g. $Copy \rightarrow Reverse \rightarrow Equal$. Using composable TMs require us to be very specific about the formatting of input and output.
<!--SR:!2025-06-19,32,270-->

What is the type of the transition function of a non-deterministic TM?
?
$\delta : Q \times (\Gamma \cup \{\Delta\}) \rightarrow 2^{(Q \cup \{h_a, h_r\}) \times (\Gamma \cup \{\Delta\}) \times \{L, R, S\}}$
<!--SR:!2025-08-01,51,255-->


What is the acceptance condition for non-deterministic TMs?
?
$w$ is accepted if *some* execution path halts in $h_a$
<!--SR:!2025-07-24,47,295-->

What is a Universal Turing Machine (UTM)?
?
A TM that simulates any other TM $M$ given encoding $e(M)$ and input $w$
<!--SR:!2025-07-06,47,290-->

Is the halting problem decidable?
?
No. The language $\{e(M)w \mid M \text{ halts on } w\}$ is recursively enumerable but not recursive
<!--SR:!2025-06-26,32,275-->

What does the Church-Turing thesis imply about undecidable problems?
?
That problems not solvable by TM are unsolvable in general, as no effective procedure exists
<!--SR:!2025-07-05,41,290-->
