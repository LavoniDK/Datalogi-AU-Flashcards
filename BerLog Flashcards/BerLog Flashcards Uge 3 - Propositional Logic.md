___

#flashcards/BerLog/3_Propositional-Logic 

## Overview of Logic

What are the three essential components of a logic?::Syntax, Semantics, and Proof Rules.
<!--SR:!2025-08-21,130,303-->

What does it mean if a logic is both Sound and Complete?::$\vDash$ (semantic entailment) and $\vdash$ (syntactic derivation) coincide, meaning that a formula is provable if and only if it is true in all models. Soundness ensures that everything provable is true, while completeness ensures that everything true is provable. Together, they establish a perfect correspondence between truth and provability.
<!--SR:!2025-07-15,93,281-->

## Syntax and semantics

What is another name for Propositional Logic?::Zero-Order Logic.
<!--SR:!2025-07-29,81,348-->

Let $φ$ be a propositional formula and let $M$ be a valuation for $φ$. What does it mean that $M ⊨ φ$?::It means that $M$ satisfies $φ$ (so $M$ is a model of $φ$), such that $φ$ evaluates to $T$ under valuation $M$.
<!--SR:!2025-07-20,72,276-->

What does $\varphi ⊨ ψ$ mean?::$ψ$ holds in all models where $φ$ holds ($\psi$ *entails* $\varphi$)
<!--SR:!2025-12-04,204,317-->

How is $\models \varphi$ defined?::For all valuations $M$, we have $M \models \varphi$. Meaning that $\varphi$ is a tautology, we say that $\varphi$ is valid.
<!--SR:!2026-01-10,211,319-->

If there exists a valuation $M$, s.t. $M \models \varphi$, what is $\varphi$?::satisfiable ($\varphi$ is SAT)
<!--SR:!2025-09-17,134,292-->

What can be said about the validity of a contingent formula?:It is satisfiable but not valid

Is it true that $(\varphi \text{ is NOT satisfiable}) \iff (\neg \varphi \text{ is a tautology})$?::yes
<!--SR:!2025-06-15,63,310-->

How does Semantic Equivalence relate to Semantic Entailment?::Semantic equivalence ($\varphi \equiv ψ$) means that $\varphi \models ψ$ AND $\psi \models \varphi$. In other words, each formula semantically entails the other, meaning they have the same truth value in every possible valuation.
<!--SR:!2025-09-12,91,292-->

## Proof and Theory

What is a Disjunctive Normal Form (DNF)?::A formula expressed as a disjunction of one or more conjunctions of literals.
<!--SR:!2025-11-13,188,318-->

How can you systematically and mechanically represent any boolean function?::take the disjunction of the conjunction of parameter values (DNF) that returns true according to each row of the truth table of any function
<!--SR:!2025-06-19,72,321-->

What is natural deduction?::A kind of proof calculus in which logical reasoning is expressed by inference rules closely related to the natural way of reasoning.
<!--SR:!2025-11-22,200,321-->

What are the options for assumptions in a proof tree?::They can be kept open, replaced by their own subproofs, discharged by special proof rules.
<!--SR:!2025-07-25,57,270-->

Describe the *open* option for assumptions in a proof tree::If assumptions are kept open, they remain a premise of the proof. These are the leaves of the tree.
<!--SR:!2025-06-18,71,323-->

Describe the "discharged" option for assumptions in a proof tree::Assumptions are discharged to prove a conclusion that is valid in general without relying on potentially false starting points. This means that they are local assumptions, denoted by closed boxes which separate scopes.
<!--SR:!2025-09-18,97,262-->

What does $φ_1 , . . . , φ_n ⊢ ψ$ mean?::that $ψ$ is provable from the assumptions $\Gamma=\{\varphi_{1}, \ldots , \varphi_{n}\}$ .
<!--SR:!2025-07-31,63,270-->


What are some of the most prominent non-constructive principles in natural deduction?:Double Negation Elimination, Law of Excluded Middle, Proof By Contradiction

Classical logic fundamentally relies on at least one ==non-constructive principle==.
<!--SR:!2025-06-17,70,319--> 

The ==Soundness Theorem== states that, if $\Gamma \vdash \varphi$, then $\Gamma \vDash \varphi$.
<!--SR:!2025-12-31,239,334-->

The ==Completeness Theorem== states that, If $\Gamma \vDash \varphi$, then $\Gamma \vdash \varphi$.
<!--SR:!2026-03-13,292,341-->


How can you quickly classify a Natural Deduction rule as either "Introduction" or "Elimination?"
?
* **Introduction Rules:** These rules *introduce* a connective (∧, ∨, →, ¬) into the conclusion. The connective *appears* in the conclusion that was *not* present in the premises.
* **Elimination Rules:** These rules *eliminate* a connective from a premise. The connective *disappears* from the main formula being considered, and some conclusion is extracted.
* _**Think**: The connective is being "taken apart" or "used up" to derive something simpler._
<!--SR:!2025-08-18,119,290-->