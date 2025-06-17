___
#flashcards/DiscreteMath/Logic 

## Logic and Proof Methods

What is a logical proposition?
?
- A logical proposition (or statement) is a declarative sentence that is either true or false, but not both.
- Often written with variables $p,q,r$ in statements like $(p\land q)\Rightarrow q$ , which can either be true or false.
- Often truth tables is used
<!--SR:!2025-10-27,186,310-->

What is a logical predicate?
?
- A logical predicate is a function that returns a truth value (true or false) when applied to specific values. It expresses a property or relationship involving variables.
- Often written as $P(x)$ or $Q(x, y)$, where $P$ and $Q$ are predicates, and $x,y$ are variables.
- **Examples:**
	  - $P(x)= x > 5$ (Predicate indicating whether $x$ is greater than 5)
	  - $Q(x, y)= x < y$ (Predicate indicating whether $x$ is less than $y$)
<!--SR:!2025-12-17,247,334-->

Explain what the following logic symbols represent $\neg,\land,\lor,\Rightarrow,\Leftrightarrow,\forall,\exists$:
?
- **$\neg$:** Negation, "not", inverts the truth value of a proposition.
- **$\land$:** Conjunction, "and", true if both propositions are true.
- **$\lor$:** Disjunction, "or", true if at least one of the propositions is true.
- **$\Rightarrow$:** Implication, "if ... then",
- **$\Leftrightarrow$:** Biconditional, "if and only if", true if both propositions have the same truth value.
- **$\forall$:** Universal quantifier, "for all", indicates that a property applies to all elements in a given set.
- **$\exists$:** Existential quantifier, "there exists at least one", indicates that there is at least one element in a set for which a property holds.
<!--SR:!2026-03-20,318,344--> 

**What does it mean to contrapose an implication?**
?
- To contrapose an implication means to reverse and negate both sides of the implication. If we have an implication "if P, then Q" (noted as $P\Rightarrow Q$), its contrapositive is "if not Q, then not P" (noted as $\neg Q\Rightarrow \neg P$). Logically, an implication and its contrapositive are equivalent; if one is true, then the other is also true.
<!--SR:!2026-02-13,283,330-->

**What are an antecedent and a consequent?**
?
- The antecedent is the first part of a conditional statement, also known as the "if"-part. It is the condition that leads to the result.
- The consequent is the second part of a conditional statement, also known as the "then"-part.
<!--SR:!2026-03-24,322,344-->

**How are tautologies, contradictions, and contingencies interpreted in truth tables?**
?
- A **tautology** is a compound propositional formula that is true regardless of the truth values of the individual propositions. In a truth table, a tautology will always have the value "true" in its final truth value column.
- A **contradiction** is a formula that is false regardless of the truth values of the individual propositions. In a truth table, a contradiction will always have the value "false" in the final column for truth values.
- A **contingency** is a compound proposition that can be either true or false, depending on the truth values of the individual propositions. In a truth table, a contingency will have a mix of "true" and "false" in the final truth value column.
<!--SR:!2026-02-21,291,334-->

#flashcards/DiscreteMath/ProofMethods 

In proofs, particularly in existential proofs and computational complexity, a ==**witness**== is an explicit example or piece of evidence that verifies the truth of a mathematical or logical statement.
<!--SR:!2026-03-30,329,347-->

How do you do proof by inference?
?
To do a proof by inference, you need to show that a statement leads to a tautology and thus is true.
<!--SR:!2026-02-18,289,347-->

**How do you do indirect proofs/proof by contradiction (Reduction ad Absurdum)**
?
- You aim to show that the negation of a statement is false, which means that the statement itself must be true.
<!--SR:!2026-03-16,315,351-->

**According to Jakob, what is a good approach to proving something that is so obviously true that it is hard to imagine a proof?**
?
- To construct a proof by contradiction. It should be easy to show why the opposite is not true.
<!--SR:!2026-01-16,256,338-->

## Set theory

#flashcards/DiscreteMath/SetTheory 


**What algebraic properties does standard set operations have?**
?
- Mutative:
	- $A\cap B = B\cap A$
	- $A\cup B = B \cup A$
- Associative:
	- $A\cap (B\cap C) = (A\cap B) \cap C$
	- $A\cup (B\cup C) = (A\cup B) \cup C$
- Distributive:
	- $A \cap (B \cup C)  = (A \cap B) \cup (A \cap C)$
	- $A \cup (B \cap C)  = (A \cup B) \cap (A \cup C)$
<!--SR:!2025-12-20,207,282-->

Explain De Morgan’s laws:
?
- De Morgan’s laws describe the complement of unions and intersections of sets:
	1. The complement of the union of two sets:
		$(A \cup B)^c = A^c \cap B^c$
	2. The complement of the intersection of two sets:
	    $(A \cap B)^c = A^c \cup B^c$
<!--SR:!2025-10-22,184,312-->

**What is the characteristic function?**
?
The characteristic function (also called the indicator function) of a set $A$ is a function that indicates membership in $A$. It is defined as:$$\chi_{A}(x)=\begin{cases} 1, & \text{if } x \in A \\ 0, & \text{if } x \notin A \end{cases}$$
<!--SR:!2026-04-01,330,351-->

What is the universal set?
?
The universal set, often denoted by $U$, in set theory is the set that contains all the elements relevant to a given discussion or problem. It serves as a comprehensive reference for all possible elements in the particular context and is used to define complementary sets and other set operations.
<!--SR:!2026-02-26,296,340-->

What is the cardinality of a set $A$, also written as $|A|$?
?
- If $A$ is a finite set, i.e., it contains $n$ elements where $n\in\mathbb{N}$, then $n$ is called the cardinality of $A$, which is written as $|A|=n$.
- If $A$ is infinite, it is sometimes written as $|A|=\infty$.
<!--SR:!2026-03-13,311,342-->
    

What is the power set of a set $A$, also written as $\mathcal{P}(A)$ or $2^A$?
?
The power set is the set consisting of all possible subsets of $A$.
- For example, if $A={1, 2, 3}$, then $\mathcal{P}(A)=\{\emptyset, \{\{1\}, \{2\}, \{3\}, \{1, 2\}, \{2, 3\}, \{1, 3\}, \{1, 2, 3\}\}$
- The notation $2^A$ implies that there are $2^n$ elements in the power set: $|\mathcal{P}(A)|=2^{|A|}$.
<!--SR:!2026-04-05,334,352-->

What is a multiset?
?
- A multiset is a set that, unlike ordinary sets, allows repetitions of elements.
<!--SR:!2026-03-31,329,352-->

## Functions

#flashcards/DiscreteMath/Functions 

What are different ways to interpret functions?
?
- **Mappings:** A function can be seen as a mapping where each element in the domain (input) is paired with exactly one element in the codomain (output).
- **Transformation:** Functions can be interpreted as transformations that change or move elements from one space to another.
- **A specific type of relation:** Functions are special relations where each input is related to exactly one output.
- **Input-output:** A function can also be viewed as a process that takes an input and produces an output based on a given rule or formula.
<!--SR:!2025-07-09,120,308-->

What is the formal definition of a function?
?
A function is a relation between two sets that assigns exactly one element from the second set (codomain) to each element in the first set (domain).
<!--SR:!2026-02-02,266,338-->

**What characterizes total functions?** :: A total function from set $A$ to set $B$ is a relation where each element in $A$ is related to exactly one element in $B$. Mathematically, this means that for all $a \in A$, there exists a unique $b \in B$ such that $f(a) = b$. A partial function from $A$ to $B$ is also a relation, but it does not need to define a value for every element in $A$; that is, there may be some elements in $A$ for which the function is not defined.
<!--SR:!2025-08-21,142,314-->

**What characterizes injective functions?**:: A function is injective if each element in the codomain has at most one element from the domain mapping to it.
<!--SR:!2025-06-10,75,294-->

**What characterizes surjective functions?** :: A function is surjective if each element in the codomain has at least one element from the domain mapping to it.
<!--SR:!2025-08-20,129,318-->

**What characterizes bijective functions?** :: A function is bijective if it is both total, injective, and surjective, meaning there is a perfect pairwise correspondence between the domain and the codomain.
<!--SR:!2026-02-08,278,334-->

What is an inverse function, and when is a function invertible?
?
An inverse function is a function that "undoes" the effect of the original function. A function is invertible if it is injective (so that each value in the codomain has only one corresponding value in the domain) and if there exists a function that, when composed with the original function, gives the identity function for all elements in the domain.
<!--SR:!2025-09-09,153,314-->

Can you define the identity function?
?
The identity function, often denoted as $I$ or $1$, is a function where the value of $I(x)$ is always equal to $x$. For each set $A$, the identity function maps each element to itself:
$$I_{A}:A\rightarrow A\space where \space I_A(x)=x,\space \forall x\in A$$
<!--SR:!2025-08-20,146,313-->

What are composite Functions?
?
A composite function is the result of combining two functions such that the output of one function becomes the input of the other.
- Notation: $(f \circ g)(x) = f(g(x))$.
- Order matters: $(f \circ g) \neq (g \circ f)$ in general.
- **Properties**:
	 - If $f: B \to C$ and $g: A \to B$, then $f \circ g: A \to C$.
	 - Associativity: $(f \circ g) \circ h = f \circ (g \circ h)$.
	 - Identity Function: For any function $f$, $f \circ \text{id} = \text{id} \circ f = f$.
<!--SR:!2026-01-16,255,338-->

What is partial functions?
?
A partial function $f:X\hookrightarrow Y$ from $X$ to $Y$ is a function $f:X'\rightarrow Y$ for some $X'\subseteq X$, i.e. it is a function defined only for some elements of its domain.
- **Key Properties**:
	- The domain of a partial function is a subset of the expected input set.
	- Examples: Division $f(x) = \frac{1}{x}$, undefined at $x = 0$.
- **Notation for Extension**:
	- To extend a partial function $f : X \to Y$, a new partial function $g : X \to Y$ is defined that maps $a \in X$ to $b \in Y$, while otherwise behaving as $f$. This is written as:  $g = f [a \mapsto b]$ with the definition:    $$g(x) = f [a \mapsto b](x) =
  \begin{cases}
  b & \text{if } x = a, \\
  f(x) & \text{otherwise}.
  \end{cases}$$
	- **Extending Multiple Values**:
		- To extend a function with multiple mappings simultaneously, brackets can be collapsed. Extensions are read left-to-right.  Example: $$f [a \mapsto b, c \mapsto d] \equiv f [a \mapsto b][c \mapsto d].$$
<!--SR:!2025-09-04,148,308-->


What are function spaces?
?
A function space is a collection of functions between two fixed sets.
<!--SR:!2026-03-14,312,353-->


**How do we denote a function $f$, that takes arguments from $A$ and $B$ and returns to $C$?**
?
One way to denote this is as $f: A\times B \rightarrow C$, where the function $f$ takes a pair $(a,b)$ in the Cartesian product $A\times B$ and returns an element from $C$.
<!--SR:!2025-09-12,156,308--> 

## Binary Relations

#flashcards/DiscreteMath/BinaryRelations 

What are ordered pairs and how do they relate to the Cartesian product?
?
An ordered pair is a collection of two elements where the order is significant, typically denoted as $(a,b)$. It is fundamental in the definition of the Cartesian product, as the Cartesian product of two sets $A$ and $B$, denoted $A \times B$, is the set of all possible ordered pairs formed by taking one element from $A$ and one element from $B$.
<!--SR:!2026-02-07,270,338-->

Explain what the cardinality of a product set is:
?
If $|A| = m$ and $|B| = n$, then the cardinality of their product set is:$$|A×B|=m⋅n=|A|⋅|B|$$
<!--SR:!2025-12-02,233,338-->

Explain what a partition/quotient set is:
?
A partition of a set is a division of the set into non-overlapping subsets, such that each element of the set belongs to exactly one subset.
<!--SR:!2025-11-20,221,334-->

Explain how a vector in $\mathbb{R}^2$ relates to the Cartesian product of the real numbers:
?
A vector in $\mathbb{R}^2$ can be represented as an ordered pair $(x,y)$, where $(x,y) \in \mathbb{R}^2$. This pair corresponds to an element in the Cartesian product $\mathbb{R} \times \mathbb{R}$, indicating that the vector is a combination of two scalars, representing its components along two dimensions in a coordinate system.
<!--SR:!2026-05-16,368,358-->

What is a relation in a mathematical context, and how is it denoted and understood?
?
A (binary) relation is a set of ordered pairs, typically defined between two sets $A$ and $B$. It expresses a kind of relationship between the elements in these sets. The notation for a relation $R$ is often $a\space R\space b$, where $a$ is from the set $A$ and $b$ is from the set $B$.
<!--SR:!2025-12-01,232,338-->

What are the four methods for representing relations?
?
- As a logical predicate $P(a,b)$, indicating whether a pair $(a,b)$ satisfies a certain condition.
- As a subset of the product set $A \times B$, where each ordered pair in the relation is an element of the product set.
- As a Boolean matrix, where the matrix elements indicate whether there is a relation between the elements (1 for yes, 0 for no).
- As a directed graph (digraph), especially when $A = B$, where the nodes represent elements in the set, and the edges represent relations between them.
<!--SR:!2026-02-01,264,338-->

Explain what the domain and range of a relation are:
?
- The **domain** of a relation is the set of all first elements in the ordered pairs, i.e., all $a$ in $A$ that appear in the relation.
- The **range**, also known as the image or codomain, is the set of all second elements in the ordered pairs, i.e., all $b$ in $B$ that can be related to from $A$ via the relation.
- These are denoted as $\text{Dom}(R)$ and $\text{Ran}(R)$.
<!--SR:!2026-04-29,351,355-->

What do reflexive, irreflexive, symmetric, asymmetric, antisymmetric, and transitive properties mean for relations?
?
- A **reflexive** relation is a relation where every element is related to itself.
- An **irreflexive** relation is a relation where no element is related to itself.
- A **symmetric** relation is a relation where if an element $a$ is related to an element $b$, then $b$ is also related to $a$.
- An **asymmetric** relation is a relation where if $a$ is related to $b$, then $b$ is not related to $a$.
- An **antisymmetric** relation is a relation where if $a$ and $b$ are related, and $b$ and $a$ are also related, then $a$ and $b$ must be the same element.
- A **transitive** relation is a relation where if $a$ is related to $b$, and $b$ is related to $c$, then $a$ is also related to $c$.
<!--SR:!2026-02-11,274,338-->

How can matrix representation be used to illustrate properties of relations?
- **Reflexivity**: ==The main diagonal will contain 1's if $R$ is reflexive.==
- **Symmetry**: ==The matrix will be symmetric around the main diagonal if $R$ is symmetric.==
- **Antisymmetry**: ==If $aRb$ and $bRa$ implies $a = b$, then for every 1 outside the main diagonal, there will be a matching 0 in the transposed position if $R$ is antisymmetric.==
<!--SR:!2026-01-08,247,334!2026-03-24,322,354!2025-11-19,220,338-->

What is equivalence relations?
?
An equivalence relation is a relation that is reflexive, symmetric, and transitive. These properties allow the relation to group elements into sets known as equivalence classes, where each element in a class is equivalent to the other elements in the same class.
<!--SR:!2025-11-25,203,321-->

How does the concept of partitions of a set relate to the equivalence classes created by an equivalence relation on the same set?
?
When we have an equivalence relation on a set, this relation divides the set into non-overlapping subsets, where each element in a subset is equivalent to the other elements in the same subset. These subsets are called equivalence classes, and the collection of these equivalence classes forms a partition of the original set. The equivalence relation ensures that each element in the set belongs to exactly one equivalence class, fulfilling the definition of a partition.
<!--SR:!2026-02-13,276,338-->

What is the closure of a relation?
?
The closure of a relation on a set is the smallest relation that both contains the original relation and has a desired property, such as reflexivity, symmetry, or transitivity. This process of adding pairs to the original relation to achieve a closure is also known as "closing" the relation under the specified property.
<!--SR:!2026-02-06,269,338-->

How do you perform closures for the different properties?
- Reflexive closure: ==Add all elements related to themselves to the relation:$$R\cup\{(a,a)∣a∈A\}$$==
- Symmetric closure:==Add the inverse relation$$R \cup R^{-1}$$==
- Transitive closure:==The union of all powers of $R$.  $$R^{\infty}$$==
<!--SR:!2025-10-10,191,334!2025-10-17,187,318!2026-04-08,337,355-->



What does $R^n$ represent in the context of binary relations?
?
$R^n$ represents the **$n$-th power** of a binary relation $R$, defined recursively as:
- $R^1 = R$
- $R^{n} = R^{n-1} \circ R\space  for\space n \geq 2,$ where $\circ$ denotes relation composition.
This means $(a, b) \in R^n$ if there exists a sequence of elements $x_1, x_2, \dots, x_{n-1}$ such that:$$
((a, x_1) \in R, \quad (x_1, x_2) \in R, \quad \dots, \quad (x_{n-1}, b) \in R$$
<!--SR:!2025-12-31,239,337-->

How can $R^n$ be interpreted when displayed in graph form and boolean matrix form?
?
- In **graph** form, $R^n$ contains all pairs where there is a path of length exactly $n$ following the graph of $R$.
- if $R$ is represented on **boolean matrix** form, $R^{n}$ acquaints to taking the $n$-th power of $M_R$ with respect to boolean matrix multiplication.
<!--SR:!2026-01-28,260,336-->

What is an the inverse of a binary relation $R\subseteq A\times B$?
?
the **inverse relation** $R^{-1}$ is defined as: $R^{-1} = \{ (b, a) \mid (a, b) \in R \}$
<!--SR:!2025-11-14,192,315-->


**What is relation compositions?**
?
Composition of relations involves combining two relations, $R$ and $S$, to form a new relation $T$, where if an element $a$ is related to $b$ through $R$ and $b$ is related to $c$ through $S$, then $a$ will be related to $c$ through $T$.
<!--SR:!2025-11-27,228,338-->

This is often expressed using a circle for function compositions:
$$(f\circ g)(x)=f(g(x))$$
## Inference Rules

#flashcards/DiscreteMath/InferenceRules 

**What is the meaning of the following notation in the context of inference rules?**
- **Turnstile ($\vdash$)**: ==Separates context/environment from the statement.==
- **Arrow ($\Rightarrow$)**: ==Denotes "evaluates to" or "transforms to" (notation is context-dependent)==.
<!--SR:!2025-12-20,228,324!2025-08-21,82,369-->


**What are inference rules**?
?
Inference rules define logical relationships between premises and conclusions, often represented as:$$
\frac{Q_1 \; Q_2 \; ... \; Q_n}{P}
	$$
- **Premises**: $Q_1, Q_2, ..., Q_n$ (conditions that must hold).
- **Conclusion**: $P$ (what can be inferred from the premises).
<!--SR:!2025-07-21,116,309-->


How can inference rules be read...
- **Top-to-bottom**: =="If $Q_1, Q_2, ..., Q_n$ hold, then $P$ holds." ==
- **Bottom-to-top**: =="To prove $P$, it suffices to prove $Q_1, Q_2, ..., Q_n$."==
<!--SR:!2026-04-18,345,349!2026-04-13,340,349-->


Rules without premises are ==**axioms**== and always hold.
<!--SR:!2026-03-16,312,349-->