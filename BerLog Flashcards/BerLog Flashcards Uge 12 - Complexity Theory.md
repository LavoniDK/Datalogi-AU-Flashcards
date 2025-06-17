___
#flashcards/BerLog/12-Complexity-Theory 

## Complexity Basics

What is the form of a terminating computation by a Turing Machine?::$(q_0, \text{input}) \vdash^m_M (\text{halt}, \text{output})$ where $m$ is the length of the computation.
<!--SR:!2025-06-18,5,230-->

What does the time complexity function $\tau_M(n)$ represent?::It is the maximum number of steps that TM $M$ takes on any input of length $n$.
<!--SR:!2025-06-16,10,273-->

## Class P

What does it mean for a language to be in class P?::It is decidable by a deterministic TM in polynomial time: $L \in P \iff \exists M \exists k ; (M \text{ decides } L \text{ and } \tau_M(n) = O(n^k))$
<!--SR:!2025-06-15,8,253-->

Why are problems in P called feasible?::Because they can be solved in polynomial time, which is generally considered tractable, even if not always practical.
<!--SR:!2025-06-26,16,290-->

Does class P contain algorithms or problems?::Problems (languages), not algorithms. A problem in P might also have an inefficient algorithm.
<!--SR:!2025-06-18,8,250-->

## Class NP

What is the acceptance condition for a nondeterministic TM $M$ on input $w$?::There exists a computation such that $(q_0, w) \vdash_M^n (h_a, \text{output})$.
<!--SR:!2025-06-19,9,253-->

What does it mean for a language to be in class NP?::There exists a nondeterministic TM that accepts it in polynomial time: $L \in NP \iff \exists M \exists k ; (M \text{ accepts } L \text{ and } \tau_M(n) = O(n^k))$
<!--SR:!2025-07-01,21,250-->

How can NP be characterized using verifiers?::As the set of languages for which a deterministic TM can verify membership using a certificate in polynomial time.
<!--SR:!2025-06-25,12,270-->

What is a polynomial verifier?::A deterministic TM that decides a language $L_1$ over $wv$ in polynomial time, such that $w \in L \iff \exists v: wv \in L_1$.
<!--SR:!2025-06-15,5,233-->

Why is proof checking in NP easier than proof searching?::Because the verifier only needs to validate a given proof, not explore the entire solution space.
<!--SR:!2025-06-19,12,270-->

## Fundamental Results

Why is $P \subseteq NP$?::Because every deterministic TM is also a valid nondeterministic TM.
<!--SR:!2025-06-16,9,253-->

What does it mean that $L \in NP \iff L$ has a polynomial verifier?::It shows equivalence between nondeterministic acceptance and deterministic verification with a certificate.
<!--SR:!2025-06-24,11,270-->

Is NP closed under intersection and union?::Yes, NP is closed under both operations.
<!--SR:!2025-06-19,9,250-->

Is NP closed under complement?::It is an open question. The complement class is called co-NP.
<!--SR:!2025-06-21,11,273-->

Why is NP at most exponential deterministic time?::Because a deterministic TM can enumerate and check all certificates of polynomial length, resulting in $2^{p(n)}$ time.
<!--SR:!2025-06-19,9,250-->

## P = NP Question

What are two ways the P = NP question could be resolved?
?
1. Show NP $\subseteq$ P, to many this seems unlikely, and would (could) have major cryptographic impact.
2. Find a language in NP with proven non-polynomial lower bound, meaning P $\subsetneq$ NP, this seems very difficult, and is if we dont have the tools and insight to prove it yet.
<!--SR:!2025-06-19,9,250-->

Why is the P vs NP problem so hard?::Because proving absolute lower bounds on complexity seems extremely difficult.
<!--SR:!2025-06-22,12,270-->

## Polynomial-time Reduction

What is a polynomial-time reduction?::A function $f$ computable in polynomial time such that $w \in L_1 \iff f(w) \in L_2$. Denoted $L_1 \leq_P L_2$.
<!--SR:!2025-06-16,9,250-->

What are key properties of $\leq_P$ reductions?::They are transitive, and if $L_2 \in P$ and $L_1 \leq_P L_2$, then $L_1 \in P$.
<!--SR:!2025-06-16,9,250-->

## NP-hardness and NP-completeness

What does it mean for a language $L$ to be NP-hard?::Every language in NP reduces to $L$ in polynomial time: $\forall L_1 \in NP, L_1 \leq_P L$.
<!--SR:!2025-06-14,8,250-->

What does it mean for a language $L$ to be NP-complete?::$L \in NP$ and $L$ is NP-hard.
<!--SR:!2025-07-10,30,270-->

Why are NP-complete problems important?::They are the hardest in NP, and all are equally hard w.r.t. polynomial-time reducibility.
<!--SR:!2025-07-10,33,270-->

What happens if an NP-complete problem is in P?::Then P = NP.
<!--SR:!2025-06-24,11,270-->

What are consequences of reductions involving NP-hard languages?::If $L_1$ is NP-hard and $L_1 \leq_P L_2$, then $L_2$ is also NP-hard.
<!--SR:!2025-06-15,8,253-->

What is the significance of Cook-Levin theorem?::It proved the NP-completeness of SAT, establishing it as a universal NP-complete problem.
<!--SR:!2025-06-18,5,233-->