___
#flashcards/BerLog/7_Context-Free-Languages  

## Push-Down Automata

How does a PDA transition differ from a finite automaton transition?
?
PDA transitions use 5-tuples: $(q, a, B, x, q')$, meaning:
- Read symbol $a$
- Test top of stack $B$
- Replace $B$ with $x \in \Gamma^*$
- Go to state $q'$
Often written in shorthand as  $q \xrightarrow{a \; B/x} q'$
<!--SR:!2025-06-18,21,250-->

What is a configuration in a PDA?
?
A configuration is $[q, w, x]$ where:
- $q$: current state
- $w$: remaining input
- $x$: current stack content (top of stack on the left)
<!--SR:!2025-06-29,32,270-->

What defines a computation step $\vdash$ in a PDA?
?
- If $(q', x) \in \delta(q, a, B)$, then $[q, aw, By] \vdash [q', w, xy]$
- If $(q', x) \in \delta(q, \Lambda, B)$, then $[q, w, By] \vdash [q', w, xy]$
<!--SR:!2025-06-24,15,229-->

When is a word accepted by a PDA?
?
A word $w \in \Sigma^*$ is accepted if:
$[q_0, w, Z_0] \vdash^* [q, \Lambda, x]$ for some $q \in A$ and $x \in \Gamma^*$
<!--SR:!2025-06-17,20,250-->

What is the difference between PDA and finite automata?
?
A PDA has a stack ($\Gamma$), giving it infinite memory. If the stack is unused and $\Gamma = \{Z_0\}$, PDA behaves like an NFA.
<!--SR:!2025-06-30,33,289-->

How do we convert an NFA to a PDA?
?
For every NFA transition $q \xrightarrow{a} q'$, define PDA transition:
$q \xrightarrow{a \; Z_0/Z_0} q'$ (stack unchanged)
<!--SR:!2025-06-29,32,289-->

What is an atomic PDA?
?
A PDA where transitions are either:
- $q \xrightarrow{a \; B/\Lambda} q'$ (pop)
- $q \xrightarrow{a \; B/CB} q'$ (single push)
Any PDA can be transformed into an equivalent atomic PDA.
<!--SR:!2025-06-25,16,230-->

What are $\mathcal{L}_A(M)$ and $\mathcal{L}_E(M)$ for a PDA?
?
- $\mathcal{L}_A(M)$: language accepted by ending in an accepting state after reading input
- $\mathcal{L}_E(M)$: language accepted if both input and stack are empty at the end
<!--SR:!2025-07-05,26,270-->

Are $\mathcal{L}_A(M)$ and $\mathcal{L}_E(M)$ equivalent?
?
Yes. For any PDA, there exists another PDA accepting the same language under the alternate condition.
<!--SR:!2025-06-28,32,289-->

When is a PDA deterministic?
?
A PDA is deterministic if:
- $\delta(q, a, X)$ and $\delta(q, \Lambda, X)$ each have ≤1 element
- At most one of them is non-empty for any $(q, X)$
This definition differs from NFA, since we allow $\Lambda$-transitions.
<!--SR:!2025-07-08,29,249-->

What is the expressive power of deterministic PDAs?
?
They are less powerful than general PDAs. They recognize exactly the deterministic context-free languages.
<!--SR:!2025-06-21,24,250-->

What is the equivalence between CFGs and PDAs?
?
- For every CFG $G$, a PDA $M$ exists with $\mathcal{L}(M) = \mathcal{L}(G)$
- For every PDA $M$, a CFG $G$ exists with $\mathcal{L}(G) = \mathcal{L}_E(M)$
<!--SR:!2025-06-22,9,230-->

## Context-Free Languages

What is the formal hierarchy between regular, deterministic context-free, and context-free languages?
?
$\textbf{REG} \subsetneq \textbf{DCFL} \subsetneq \textbf{CFL}$
<!--SR:!2025-06-29,20,250-->

How can the Context-Free Pumping Lemma be used to prove a language is not context-free?
?
By using its **contrapositive**:
If for all $k \geq 1$, there exists $z \in L$ with $|z| \geq k$ such that **for all** decompositions $z = uvwxy$ with $|vwx| \leq k$, $|vx| > 0$, there exists some $i \geq 0$ such that $uv^iwx^iy \notin L$, then $L$ is not context-free.
<!--SR:!2025-06-15,4,210-->

What are the equivalent characterizations of CFLs?
?
A language $L$ is context-free iff:
1. $L = \mathcal{L}(G)$ for some CFG
2. $L = \mathcal{L}(M)$ for some PDA
3. $L = \mathcal{L}(G)$ for some grammar in CNF
4. $L = \mathcal{L}_E(M)$ for a PDA using empty stack
5. $L = \mathcal{L}(M)$ for some atomic PDA
<!--SR:!2025-06-24,27,270-->

What are strictly weaker characterizations than general CFLs?
?
1. $L = \mathcal{L}(G)$ for a regular grammar (REG)
2. $L = \mathcal{L}(M)$ for a deterministic PDA (DCFL)
3. $L$ generated by a non-ambiguous CFG
<!--SR:!2025-06-21,12,249-->

Which closure properties hold for context-free languages (CFL)?
?
CFLs are closed under:
- Union
- Concatenation
- Kleene star
- Intersection with regular languages
<!--SR:!2025-06-23,14,210-->

Which closure properties do CFLs not satisfy?
?
CFLs are **not** closed under:
- Intersection (general case)
- Complement
<!--SR:!2025-07-02,35,289-->
