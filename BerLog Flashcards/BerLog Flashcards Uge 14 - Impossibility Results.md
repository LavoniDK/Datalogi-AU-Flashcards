___
#flashcards/BerLog/14_Impossibility-Results

## Recap: Logics

What is a logic triple composed of? ::A logic consists of $(\Phi, \models, \vdash)$: formulas, semantics (validity), and proof system (provability).
<!--SR:!2025-06-20,9,250-->

What does it mean for an axiomatisation $\Gamma$ to be sound for a model $\mathcal{M}$? ::All axioms in $\Gamma$ are true in $\mathcal{M}$.
<!--SR:!2025-06-18,9,250-->

What does it mean for an axiomatisation $\Gamma$ to be complete for a model $\mathcal{M}$? ::All statements true in $\mathcal{M}$ are provable from $\Gamma$.
<!--SR:!2025-06-15,4,210-->

What is the relationship between $\models_{AR}\varphi$ and $\vdash_{AR}\varphi$ in Peano Arithmetic? ::We want to know if $PA$ is both sound and complete for $\mathbb{N}$, i.e., if $\models_{AR}\varphi \Leftrightarrow \vdash_{AR}\varphi$.
<!--SR:!2025-06-16,5,230-->

## Expressivity

What does expressivity refer to in logic? ::The ability of a logic to express properties or define languages.
<!--SR:!2025-06-23,14,290-->

What does it mean for a logic $(\Phi, \models)$ to express a language $L$? ::There exists a computable encoding $e$ such that $w \in L \Leftrightarrow \models e(w)$.
<!--SR:!2025-06-16,3,230-->

What does expressibility imply about reducibility? ::If $L$ is expressible, then $L \leq_m \models$ (many-one reducibility).
<!--SR:!2025-06-15,2,190-->

What happens if a logic can express a non-recursive language? ::Its validity relation $\models$ is undecidable.
<!--SR:!2025-06-17,8,250-->

What happens if a logic can express a non-recursively enumerable language? ::Its validity relation $\models$ is not even semi-decidable.
<!--SR:!2025-06-16,5,230-->

How do we show arithmetic is undecidable? ::By expressing an undecidable problem like BPCP using arithmetic, e.g., as a reachability problem.
<!--SR:!2025-06-20,9,250-->

## Exclusivity Principles

Why can't validity be decidable in a highly expressive logic? ::Because expressibility of non-recursive languages contradicts decidable validity.
<!--SR:!2025-06-16,5,230-->

Why can't provability be decidable if a logic is sound, complete, and expressive? ::Because it would imply decidability of non-recursive languages, which is impossible.
<!--SR:!2025-06-20,9,250-->

Why can't a logic be sound and complete if it expresses a non-recursively enumerable language? ::Because provability is recursively enumerable but validity would not be
<!--SR:!2025-06-18,5,230-->
## Gödel's Incompleteness Theorems

What was Hilbert's program? ::An effort to formalize all of mathematics and resolve foundational crises through logic.
<!--SR:!2025-06-20,9,250-->

What did the logicism program propose? ::That all of mathematics can be derived from logic.
<!--SR:!2025-06-17,11,270-->

What does Gödel's first incompleteness theorem state? ::In any consistent formal system capable of elementary arithmetic, there exist true statements that cannot be proven within the system.
<!--SR:!2025-06-15,2,170-->

Is the validity of arithmetic semi-decidable? ::No, it is not even recursively enumerable.
<!--SR:!2025-06-18,5,230-->

Is provability semi-decidable? ::Yes, because proofs can be enumerated.
<!--SR:!2025-06-27,16,290-->

Why don't truth and provability coincide in arithmetic? ::Because provability is semi-decidable, but truth is not.
<!--SR:!2025-06-19,8,250-->

What does Gödel’s first incompleteness theorem imply about arithmetic? ::There are true but unprovable statements in any sufficiently complex formal system.
<!--SR:!2025-06-23,12,270-->

## Proof Sketch Elements

What undecidable problem is used in the proof sketch of Gödel’s theorem? ::Affine Post Correspondence Problem (Affine PCP).
<!--SR:!2025-06-18,5,230-->

Why is Affine PCP relevant to Gödel’s incompleteness theorem? ::Because it's recursively enumerable but its complement is not, illustrating undecidability.
<!--SR:!2025-06-17,4,210-->

What is transitive closure used for in the proof? ::To define reachability and expressibility in the formal system.
<!--SR:!2025-06-16,3,230-->

What is Gödel numbering? ::A method of encoding syntactic elements of a formal system as natural numbers.
<!--SR:!2025-06-18,5,230-->

What is the prime power variant of Gödel numbering? ::Assigns each symbol a unique prime; a sequence is encoded as a product of primes raised to positional powers.
<!--SR:!2025-06-22,9,250-->

How does Gödel’s proof achieve self-reference? ::By constructing a statement that asserts its own unprovability using encoding and internal expressibility
<!--SR:!2025-06-18,5,230-->