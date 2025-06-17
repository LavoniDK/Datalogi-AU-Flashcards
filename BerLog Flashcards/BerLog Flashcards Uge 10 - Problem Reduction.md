___
#flashcards/BerLog/10_Problem-Reductions 
## Problem Reductions

What is a decision problem?
?
A decision problem consists of:
- A definition of its inputs (instances)
- A yes/no question about each instance
<!--SR:!2025-07-09,43,295-->

What is a decidable decision problem?
?
A problem is decidable if the set of yes-instances $Y(P)$ is a recursive language under a reasonable encoding
<!--SR:!2025-06-27,33,275-->

How do we partition the domain of strings for a decision problem under encoding $e$?
?
$\Sigma^* = E(P)' \uplus Y(P) \uplus N(P)$ where:
- $Y(P)$: yes-instances
- $N(P)$: no-instances
- $E(P)'$: strings that are not valid instances
<!--SR:!2025-07-25,46,255-->

What does the Self-Accepting TM problem ask?
?
Given TM $M$, does $M$ accept $e(M)$?
<!--SR:!2025-06-20,11,239-->

Is the Self-Accepting problem decidable?
?
No, it is undecidable (NSA is not recursively enumerable)
<!--SR:!2025-06-25,30,274-->

What is the Halting Problem?
?
Given TM $M$ and input $w$, does $M$ halt on $w$?
<!--SR:!2025-07-23,44,299-->

Is the Halting Problem decidable?
?
No, it is undecidable
<!--SR:!2025-07-28,61,315-->

What is the complementary decision problem $P'$?
?
The problem where yes/no answers are flipped. If $P$ is decidable, then $P'$ is also decidable.
<!--SR:!2025-06-24,29,275-->

What does it mean for a language $L_1$ to be reducible to $L_2$?
?
$L_1 \leq L_2$ if there exists a computable function $f$, not necessarily invertible, such that:
$x \in L_1 \iff f(x) \in L_2$
<!--SR:!2025-06-17,23,255-->

What does it mean for decision problem $P_1$ to be reducible to $P_2$?
?
$P_1 \leq P_2$ if an algorithm translates instances of $P_1$ to $P_2$ preserving the yes/no answer
<!--SR:!2025-06-20,24,259-->

How is reduction used positively?
?
If $P_1 \leq P_2$ and $P_2$ is decidable, then $P_1$ is decidable
<!--SR:!2025-06-15,6,261-->

How is reduction used negatively?
?
If $P_1 \leq P_2$ and $P_1$ is undecidable, then $P_2$ is undecidable
<!--SR:!2025-06-25,16,240-->

What is Rice’s Theorem?
?
Any non-trivial language property of Turing Machines is undecidable. This implies that any non-trivial question about the language recognized by a TM is undecidable
<!--SR:!2025-06-25,38,290-->

What is a language property of Turing Machines?
?
- A property $R$ such that: If $\mathcal{L}(M_1) = \mathcal{L}(M_2)$ then $R(M_1) \iff R(M_2)$
- Intuitively think:  if two TMs recognize the **same language**, then either **both** have the property $R$, or **neither** does.
- You're saying that $R$ depends only on the **language** $\mathcal{L}(M)$, not on the **internal structure** or behavior of the Turing machine.
- Think of $R$ as answering questions like:
	- _Does the machine accept a regular language?_
	- _Is the language finite?_
	- _Is the language empty?_
<!--SR:!2025-06-18,23,254-->

What makes a language property non-trivial?
?
There exist TMs $M_1$, $M_2$ such that $R(M_1)$ and $\neg R(M_2)$
<!--SR:!2025-06-26,29,281-->

## PCP

What is the Post's Correspondence Problem (PCP)?
?
Given two lists of strings $A = A_1, ..., A_k$ and $B = B_1, ..., B_k$, does there exist a sequence of indices $i_1,...,i_m$ such that:
$$A_{i_1}...A_{i_m} = B_{i_1}...B_{i_m}?$$
<!--SR:!2025-06-15,25,274-->

Is PCP decidable?
?
No, PCP is undecidable
<!--SR:!2025-07-13,48,295-->

What is the Modified Post's Correspondence Problem (MPCP)?
?
Like PCP, but the sequence must start with $A_1$ and $B_1$:
$$A_1 A_{i_2}...A_{i_m} = B_1 B_{i_2}...B_{i_m}$$
<!--SR:!2025-06-21,26,275-->

What is the relationship between Accepts$_{TM}$, MPCP, and PCP?
?
Accepts$_{TM} \leq$ MPCP $\leq$ PCP
<!--SR:!2025-07-06,27,255-->

How is MPCP reduced to PCP?
?
Using functions $ir(x)$ and $il(x)$ to insert '#' after/before letters and adding start/end markers to force the initial match
<!--SR:!2025-07-13,34,281-->

What is the proof strategy for Accepts$_{TM} \leq$ MPCP?
?
Encode the TM's computation steps as domino pieces such that a solution exists iff the TM accepts the input
<!--SR:!2025-07-08,29,234-->

What does the kitchen tiling problem ask?
?
Can an $m \times m$ floor be tiled with a set of square tiles with matching edges?
<!--SR:!2025-07-01,37,295-->

Is the kitchen tiling problem decidable?
?
No, it is undecidable
<!--SR:!2025-07-26,47,299-->

What does it mean for a CFG to be ambiguous?
?
A CFG is ambiguous if some string in its language has more than one derivation tree
<!--SR:!2025-06-18,28,275-->

What is the CFG ambiguity problem?
?
Given CFG $G$, is $G$ ambiguous?
<!--SR:!2025-07-25,46,294-->

Is the CFG ambiguity problem decidable?
?
No, it is undecidable
<!--SR:!2025-07-31,52,299-->

How is PCP related to CFG ambiguity?
?
PCP $\leq$ AmbiguousCFG; a CFG is constructed to be ambiguous iff the PCP instance has a solution
<!--SR:!2025-06-19,24,254-->

Which CFG-related problems are undecidable?
?
- $L(G_1) \cap L(G_2) = \emptyset$?
- $L(G_1) = L(G_2)$?
- $L(G) = \Sigma^*$?
<!--SR:!2025-06-17,4,210-->

Which CFG-related problems are decidable?
?
- Membership
- Emptiness
- Infiniteness
- Union
<!--SR:!2025-06-19,10,215-->

What is a language property?
?
A property $R$ such that: If $\mathcal{L}(M_1) = \mathcal{L}(M_2)$, then $R(M_1) \iff R(M_2)$
<!--SR:!2025-06-16,26,275-->

How does Rice’s theorem prove undecidability?
?
By reducing Accepts-$\Lambda$ to $R$ or $R'$ using a TM composition that mimics behavior
<!--SR:!2025-06-15,2,201-->

What is Busy Beaver $\Sigma(n)$?
?
The max number of 1s a halting $n$-state TM with input $\Lambda$ can write on the tape
<!--SR:!2025-06-19,23,259-->

Why is Busy Beaver important?
?
$\Sigma(n)$ eventually grows faster than every computable function
<!--SR:!2025-07-24,45,300-->


What is the **decidability frontier** in the context of Turing Machines with limited states and symbols?
?
It is the **emergent boundary** (often visualized as a table or chart) that separates **decidable** from **undecidable** cases of the **halting problem** for Turing Machines with fixed numbers of **states** and **tape symbols**.
<!--SR:!2025-06-14,24,274-->
