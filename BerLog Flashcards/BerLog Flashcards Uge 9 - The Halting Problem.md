___
#flashcards/BerLog/9_The-Halting-Problem

## The Recursive Languages

Why are recursive languages closed under complement?
?
Given a TM that decides $L$, swap its accepting/rejecting states to decide $\overline{L}$
<!--SR:!2025-06-21,12,273-->

Are recursively enumerable languages closed under union and intersection?
?
Yes, this can be constructed by running two TMs simultaneously and accepting if one or both accept
<!--SR:!2025-07-11,32,270-->

If $L$ and $L'$ are recursively enumerable, then $L$ is recursive, i.e. a language and it's complement cannot both be recursively enumerable. Why is that?
?
If both were recursively enumerable, we could enumerate both the yes- and no instance simultanously, if $M$ halts then accept, if $M'$ halts then don't accept, by definition of accepting TMs one of either would accept in finite time, making the language decidable by a composed TM.
<!--SR:!2025-06-16,3,251-->


Are recursively enumerable languages closed under complement?
?
No, they are not closed under complement
<!--SR:!2025-06-22,13,250-->

What is the relation between recursive and recursively enumerable languages?
?
Every recursive language is recursively enumerable, but not vice versa
<!--SR:!2025-06-17,8,254-->

What does it mean for a TM to enumerate a language?
?
It lists all words of the language (possibly in arbitrary order) without repetition: $x_1, x_2, x_3, \dots$
<!--SR:!2025-06-18,22,252-->

What is the equivalence between enumeration and acceptance?
?
A language $L$ is enumerable $\iff$ there exists a TM that accepts $L$
<!--SR:!2025-06-18,12,273-->

What is the benefit of enumerating a language in canonical order?
?
It allows us to halt when the current word has been passed — enabling decision, not just acceptance
<!--SR:!2025-06-16,5,235-->

What is the equivalence between canonical enumeration and decision?
?
$L$ is decidable $\iff$ $L$ can be enumerated in canonical order
<!--SR:!2025-06-29,20,250-->

What are the languages SA and NSA?
?
- $SA = \{ e(M) \mid M \text{ accepts } e(M) \}$ (Self-accepting)
- $NSA = \{ e(M) \mid M \text{ does not accept } e(M) \}$ (Not self-accepting)
<!--SR:!2025-07-03,24,250-->

Is the language SA recursively enumerable?
?
Yes — simulate $M$ on its own encoding and accept if it halts and accepts
<!--SR:!2025-06-18,9,254-->

Is the language SA recursive?
?
No — If it were, NSA would be too, which leads to contradiction
<!--SR:!2025-06-15,2,193-->

Is NSA recursively enumerable?
?
No — A contradiction arises from assuming it is and examining $e(M) \in NSA \iff e(M) \notin NSA$
<!--SR:!2025-07-09,30,234-->

What is the Halting Problem?
?
Given a TM $M$ and an input $w$, determine whether $M$ halts on $w$
<!--SR:!2025-06-30,34,272-->

Is the halting problem recursively enumerable?
?
Yes — we can simulate $M$ on $w$ and accept if it halts
<!--SR:!2025-06-16,5,253-->

Is the halting problem recursive?
?
No — proven via diagonalization and contradiction
<!--SR:!2025-06-20,11,274-->

What is the proof outline for the undecidability of the halting problem?
?
1. Assume $H$ decides halting
2. Construct $D$ that does the opposite of $H(e(M),w)$
3. Evaluate $D(e(D),e(D))$:
	- If $D$ halts, then $H(e(D), e(D))$ loops, meaning $e(D)$ does not halt on it's own encoding according to the definition of $H$ → contradiction
	- If $D$ loops, then the opposite case also leads to an contradiction.
4. Thus, $H$ cannot exist
<!--SR:!2025-07-02,23,252-->

What does the halting problem imply about computation?
?
Some functions are impossible to compute, and some recognizable languages are undecidable
<!--SR:!2025-07-09,33,273-->

What is the relationship between recursively enumerable and recursive languages?
?
Recursive $\subset$ recursively enumerable. A language is recursive if it is both recursively enumerable and decidable
<!--SR:!2025-06-17,8,253-->

Why is the complement of the halting problem, not recursively enumerable?
?
Because there's no way to construct a Turing machine that always halts and accepts when $M$ doesn't halt. We can't confirm non-halting behavior in finite time.
<!--SR:!2025-07-12,33,274-->

What does _semidecidability_ mean?
?
A language is **semidecidable** if it is recursively enumerable. Think of it as "we can recognize _yes_-instances, but not _no_-instances."
<!--SR:!2025-06-17,8,255-->

## Countability of Sets

When do two sets, $A,B$ have the same cardinality?
?
When there exists a bijection $f: A \rightarrow B$, i.e., $f$ is injective and surjective
<!--SR:!2025-07-03,24,254-->

What does it mean for a set to be countably infinite?
?
A set is countably infinite if there exists a bijection from $\mathbb{N}$ to the set
<!--SR:!2025-06-18,9,253-->

What is a countable set?
?
A set that is either finite or countably infinite
<!--SR:!2025-07-06,27,272-->

What are some examples of countable sets?
?
- $\mathbb{Z}$, $\mathbb{Q}$
- $\mathbb{N} \times \mathbb{N}$, and inductively also $\mathbb{N}^k$
- $\mathbb{N}^*$, $\Sigma^*$, all subsets of countable sets
- The set of Turing Machines
- The set of recursively enumerable languages
<!--SR:!2025-06-15,9,254-->

What is the cardinality of $\mathbb{R}$ or $2^{\mathbb{N}}$?
?
$2^{\aleph_0}$, which is uncountable
<!--SR:!2025-06-14,5,235-->

How does Cantor’s diagonal argument prove $2^\mathbb{N}$ is uncountable?
?
Assume a list of all subsets of $\mathbb{N}$. Define $D = \{i \mid i \notin X_i\}$. Then $D \neq X_i$ for all $i$, which is contradiction to the original assumption.
<!--SR:!2025-06-16,7,254--> 

How does the diagonal argument relate to the language NSA?
?
It constructs a language $NSA := \{e(M) \mid e(M) \notin \mathcal{L}(M)\}$, which leads to the contradiction $e(D) \in \mathcal{L}(D) \iff e(D) \notin \mathcal{L}(D)$
<!--SR:!2025-06-14,5,235-->


What conclusion about language- and automata theory can we draw from comparing the countability of $\Sigma^*$ and $2^{\Sigma^*}$?
?
- $\Sigma^*$ (all strings) is **countably infinite**.
- $2^{\Sigma^*}$ (all languages) is **uncountable**.
- There are only **countably many** Turing machines (as they can be encoded as a finite string), meaning that there are only **countably many recursively enumerable languages**.
- So **most languages are not recursively enumerable** - they cannot be recognized by any Turing machine.
<!--SR:!2025-06-24,18,254-->


Why are there non-recursive languages?
?
Because there are **uncountably many languages** but only **countably many Turing machines**, so most languages cannot be decided by any TM.
<!--SR:!2025-07-02,23,252-->

What is the Continuum Hypothesis?
?
The hypothesis that there is no cardinality strictly between $\aleph_0$ and $2^{\aleph_0}$; i.e., $\aleph_1 = 2^{\aleph_0}$
<!--SR:!2025-06-16,7,255-->

## Unrestricted Grammars


What is the key difference in unrestricted grammars compared to context-free grammars?
?
The left-hand side of a production rule may include both terminals and variables, allowing rewriting of terminal-containing substrings.
<!--SR:!2025-06-18,9,254-->

What kind of languages can unrestricted grammars generate?
?
Exactly the recursively enumerable languages
<!--SR:!2025-06-17,8,255-->

Give an example of a language generated by an unrestricted grammar that is not context-free.
?
$\{a^i b^i c^i \mid i \geq 0\}$
<!--SR:!2025-06-16,5,234-->

What is the equivalence between unrestricted grammars and Turing machines?
?
- For any TM $M$, there is an unrestricted grammar $G_M$ such that $\mathcal{L}(G_M) = \mathcal{L}(M)$
- For any unrestricted grammar $G$, there is a TM $T_G$ such that $\mathcal{L}(T_G) = \mathcal{L}(G)$
<!--SR:!2025-07-12,33,272-->

How do you construct a TM $T_G$ from an unrestricted grammar $G$?
?
Use a 3-tape non-deterministic TM:
1. Tape 1: input word
2. Tape 2: encoded grammar rules
3. Tape 3: start symbol $S$, simulate derivations
<!--SR:!2025-06-15,2,214-->

When does the TM $T_G$ accept an input word $w$?
?
If there exists a derivation in $G$ that produces $w$, i.e., Tapes 1 and 3 match at termination
<!--SR:!2025-06-18,5,234-->

How do you construct an unrestricted grammar $G_M$ from a Turing Machine $M$?
?
1. Use grammar rules to generate $w[q_0 \Delta w]$
2. Simulate TM transitions with rules like $q_i x y \rightarrow z q_j y$
3. Remove tape simulation only when $h_a$ is reached
<!--SR:!2025-06-18,5,234-->
