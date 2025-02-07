___
#flashcards/BerLog/Uge2 

## Compositions of NFA


How do you construct the complement of a DFA?::Invert the accepting and non-accepting states. (can only be done for total DFA)
<!--SR:!2025-02-10,4,272-->

What is the purpose of a product automaton?::A product automaton accepts a word if it is accepted by both automata simultaneously.
<!--SR:!2025-02-10,4,276-->

What are the possible operations when constructing a composite DFA from two DFAs?::Union, intersection, and set difference.
<!--SR:!2025-02-10,4,278-->

How can we construct a composite DFA that recognizes $L_1 \cup L_2$, $L_1 \cap L_2$, or $L_1 \setminus L_2$?
?
Given two DFAs $M_1$ and $M_2$ recognizing $L_1$ and $L_2$, we construct a composite DFA $M = (Q, \Sigma, q_0, A, \delta)$ with:
- **State set**: $Q = Q_1 \times Q_2$.
- **Alphabet**: $\Sigma$.
- **Initial state**: $q_0 = (q_1^0, q_2^0)$.
- **Transition function**: $\delta((p, q), \sigma) = (\delta_1(p, \sigma), \delta_2(q, \sigma))$.
- **Acceptance conditions**:
	- **Union**: $A = \{(p, q) \mid p \in A_1 \text{ or } q \in A_2\}$.
	- **Intersection**: $A = \{(p, q) \mid p \in A_1 \text{ and } q \in A_2\}$.
	- **Difference**: $A = \{(p, q) \mid p \in A_1 \text{ and } q \notin A_2\}$.
<!--SR:!2025-02-07,1,232-->


A product automaton's state set consists of **==pairs of states==** from both input automata.
<!--SR:!2025-02-10,4,272-->

A **composite DFA** can recognize operations such as:
- **Union** (or): **==$A = \{(p, q) \mid p \in A_1 \text{ or } q \in A_2\}$==**.
- **Intersection** (and): **==$A = \{(p, q) \mid p \in A_1 \text{ and } q \in A_2\}$==**.
- **Difference**: **==$A = \{(p, q) \mid p \in A_1 \text{ and } q \notin A_2\}$==**.
<!--SR:!2025-02-10,4,278!2025-02-09,3,252!2025-02-10,4,284-->

## NFA

What is a key characteristic of nondeterministic choice in an NFA?::At certain points, multiple transitions are possible and all are explored concurrently.
<!--SR:!2025-02-10,4,274-->

What is the acceptance criterion for an NFA?::A string is accepted if at least one computational path reaches an accepting state.
<!--SR:!2025-02-10,4,278-->

What are $\Lambda$-transitions in an NFA?::Transitions that allow movement between states without consuming an input symbol.
<!--SR:!2025-02-10,4,277-->

How does an NFA process a string using its extended transition function $\delta^*$?
?
The function $\delta^*$ is defined recursively:
1. **Base case**: $\delta^*(q, \Lambda) = \Lambda$-closure$(\{q\})$.
2. **Recursive case**:
   $\delta^*(q, x\sigma) = \Lambda\text{-closure} \left( \bigcup_{p \in \delta^*(q, x)} \delta(p, \sigma) \right)$.
A string is accepted if $\delta^*(q_0, x) \cap A \neq \emptyset$.
<!--SR:!2025-02-10,4,272-->

How can we construct a composable NFA?
?
A **composable NFA** has:
1. A unique **initial state** with in-degree 0.
2. A unique **final state** with out-degree 0.
3. $\Lambda$-transitions to connect different NFAs without state explosion.
<!--SR:!2025-02-10,4,274-->

How does an NFA process a string using its extended transition function $\delta^*$?
?
Think of an NFA as exploring multiple paths at once, like a branching tree.
1. **Start at the initial state** and include any states reachable by $\Lambda$-transitions.
2. **For each input symbol**, the NFA follows **all possible transitions** from the current set of active states.
3. **At each step**, it also includes any states reachable via $\Lambda$-transitions.
4. **If at least one path** reaches an accepting state after reading the full string, the NFA accepts.
<!--SR:!2025-02-10,4,277-->

## Kleene's Theorem and REG = DFA = NFA

What are the three equivalent ways to define regular languages?::Regular expressions (REG), deterministic finite automata (DFA), and nondeterministic finite automata (NFA).
<!--SR:!2025-02-10,4,283-->

What does Kleene's theorem establish?::Kleene’s theorem states that **regular languages are exactly the languages recognized by finite automata and described by regular expressions**.
<!--SR:!2025-02-10,4,278-->


To convert an NFA into a DFA, we use **==state subset construction==**, where each DFA state represents **==a set of NFA states==**.
<!--SR:!2025-02-10,4,270!2025-02-10,4,278-->  


How does the **Expression Graph Elimination** method convert an NFA into a regular expression?
?
1. Ensure the NFA has **one accepting state**.  
2. Iteratively **eliminate states** by updating transition labels with equivalent regular expressions.  
3. Continue eliminating states until only the **start state and final state** remain.  
4. The final transition label represents the **regular expression** for the language.  

Why is the **Dynamic Programming (Floyd-Warshall-style) method** preferred for NFA → REG conversion?
?
Instead of eliminating states one by one (which is inefficient), this method:  
1. Uses a **table-based approach** to compute the smallest regular expressions between states.  
2. Avoids unnecessary recomputation.  
3. Has a **worst-case complexity of $\mathcal{O}(n^3)$**, making it much more efficient than naive elimination.  

How does the **subset construction** method transform an NFA into a DFA?
?
4. Each DFA state represents a **set of NFA states**.  
5. The DFA transition function **computes the set of possible next states** for each input symbol.  
6. The DFA accepts if any of its states correspond to **an accepting NFA state**.  
7. This transformation **guarantees determinism** but may exponentially increase the number of states.  

## More RegEx

What does the regular expression `(a+b)*` represent?::It represents the set of all strings over `{a, b}`, including the empty string.
<!--SR:!2025-02-10,4,285-->

What does the regular expression `ab+` match?::It matches any string that starts with `a` followed by **at least one** `b` (e.g., `ab`, `abb`, `abbb`).
<!--SR:!2025-02-10,4,285-->


How do you interpret the regular expression `(a+b)c*`?
?
- `(a+b)`: The string must **start** with either `a` or `b`.
- `c*`: After `a` or `b`, there can be **zero or more** occurrences of `c`.
- Example matches: `"a"`, `"b"`, `"ac"`, `"bccccc"`.
- Example non-matches: `"c"`, `"ba"`, `"abc"`.
<!--SR:!2025-02-10,4,284-->