___
#flashcards/BerLog/Uge1

## Formal Languages

What is the null string ($\Lambda$)?::The null string is an empty string with a length of 0.
<!--SR:!2025-02-01,4,270-->

What does $\Sigma^*$ represent?::$\Sigma^*$ is the set of all strings over the alphabet $\Sigma$, including the null string $\Lambda$.
<!--SR:!2025-01-31,3,252-->

What is a finite language?::A finite language is a subset of $\Sigma^*$ containing a finite number of strings.
<!--SR:!2025-02-01,3,252-->

Define an alphabet ($\Sigma$) and strings.
?
An alphabet is a finite set of symbols, such as $\{a, b\}$ or $\{0, 1\}$. Strings are finite sequences of symbols from the alphabet.
<!--SR:!2025-02-01,4,272-->

Explain string concatenation (with two strings).
?
Concatenation combines strings $x$ and $y$, denoted $x\cdot y$.
<!--SR:!2025-02-01,4,271-->

What are the properties of string concatenation?
?
  - $\Lambda \cdot x = x \cdot \Lambda = x$
  - $\|x\cdot y\| = \|x\| + \|y\|$
  - Associativity: $(x \cdot y)\cdot z = x \cdot (y\cdot z)$
<!--SR:!2025-02-01,3,252-->

What is a prefix of a string?::A prefix is an initial segment of a string up to some position.
<!--SR:!2025-02-02,4,280-->

What is a suffix of a string?::A suffix is a final segment of a string starting from some position.
<!--SR:!2025-02-02,4,280-->

What is a substring of a string $s$?::A substring is any contiguous sequence of characters within $s$.
<!--SR:!2025-02-02,4,278-->

What is the special property of the null string ($\Lambda$) regarding substrings?::The null string ($\Lambda$) is a prefix, suffix, and substring of any string.
<!--SR:!2025-02-02,4,279-->

A language is a **==set of strings over an alphabet of symbols==**.
<!--SR:!2025-01-31,3,250-->

The **length of a string**, $\|x\|$, represents the **==number of symbols in $x$==**.
<!--SR:!2025-02-01,4,270-->

**String operations** include concatenation, where $x \in L_1$ and $y \in L_2$ form **==the string $x\cdot y$==**.
<!--SR:!2025-01-31,3,251-->

The **Kleene star** $L^*$ is defined as::the union of all possible concatenations of strings in $L$, including $\Lambda$). Formally, $L^* = \bigcup_{k \geq 0} L^k$.
<!--SR:!2025-01-31,3,252-->

What is the difference between generative and property-based definitions of languages?
?
- Generative definitions describe how to generate strings in the language.
	- Example: $L_1 = \{ab, bab\}^* \cup \{b\}\{ba\}^*\{ab\}^*$.
- Property-based definitions specify a property that all strings in the language must satisfy.
	- Example: $L_2 = \{x \in \{a, b\}^* \mid n_a(x) > n_b(x)\}$.
<!--SR:!2025-02-01,4,272-->

What is string reversal?::String reversal is the process of reversing the order of symbols in a word. Example: $(ab)^R = ba$.

What are the properties of string reversal?
?
  - $\Lambda^R = \Lambda$
  - $(au)^R = u^R a$
  - Distributive: $(uv)^R = v^R u^R$
  - Self-inverse: $(u^R)^R = u$

What is string repetition?::String repetition is the process of repeating a string multiple times. Example: $(ab)^2 = abab$.

What are the properties of string repetition?
?
  - $u^0 = \Lambda$
  - $u^{n+1} = u(u^n)$
  - $u^m u^n = u^{m+n}$
  - $(u^m)^n = u^{mn}$

What are the properties of occurrence count?
?
  - $n_{\sigma}(\Lambda) = 0$
  - $n_{\sigma}(au) = 1 + n_{\sigma}(u)$ if $\sigma = a$
  - $n_{\sigma}(au) = n_{\sigma}(u)$ if $\sigma \neq a$

What is the complement of a language?::The complement of a language $L$ is $L' = \Sigma^* - L = \{u \mid u \in \Sigma^*, u \notin L\}$.

What is language concatenation?::Language concatenation is the combination of two languages, $L_1 L_2 = \{xy \mid x \in L_1, y \in L_2\}$.

What is the reverse of a language?::The reverse of a language $L$ is $L^R = \{u^R \mid u \in L\}$.

What is language exponentiation?
?
Exponentiation of a language is repeated concatenation, defined as:
  - $L^0 = \{\Lambda\}$
  - $L^k = L L^{k-1}$

What is the positive closure of a language?::The positive closure of a language $L^+$ is $L^+ = \bigcup_{k \geq 1} L^k$, omitting the empty string.

What are the properties of the Kleene star?
?
  - $L^+ = L L^*$
  - $L^* = \{\Lambda\} \cup L^+$
  - If $\Lambda \in L$, then $L^* = L^+$
  - $\emptyset^+ = \emptyset$
  - $\emptyset^* = \{\Lambda\}$

## Recursive definitions

What are the two key components of a recursive definition?
?
1. **Basis statement** that specifies one or more initial elements in the set.
2. **Recursive rules** that define how to construct new elements using elements already in the set.
<!--SR:!2025-02-01,4,272-->

How is closure property of $\mathbb{N}$ described in its recursive definition?::Through the successor operation. $\mathbb{N}$ is closed under the successor operation.
<!--SR:!2025-02-01,4,271-->

Define the natural numbers $\mathbb{N}$ recursively.
?
1. $0 \in \mathbb{N}$ (basis).
2. If $n \in \mathbb{N}$, then $n+1 \in \mathbb{N}$ (successor operation).
3. $\mathbb{N}$ is the smallest set satisfying (1) and (2).
<!--SR:!2025-02-01,4,274-->

Define the subset of multiples of 7 recursively.
?
1. $0 \in A$ (basis).
2. If $n \in A$, then $n+7 \in A$.
<!--SR:!2025-01-31,3,252-->

How is the set of all strings $\Sigma^*$ over $\{a, b\}$ defined recursively?
?
1. $\Lambda \in \Sigma^*$ (basis, empty string).
2. If $x \in \Sigma^*$, then $x\cdot a \in \Sigma^*$ and $x\cdot b \in \Sigma^*$.
<!--SR:!2025-02-01,3,250-->

## Structural Induction

What is strong induction?::A variation of induction where you assume the property is true for all values less than or equal to the current value during the inductive step.
<!--SR:!2025-02-01,4,272-->

Structural induction is ==a generalization of induction, used to prove properties about recursively defined structures==
<!--SR:!2025-02-01,3,259-->

## Regular Expression and Languages

What is a regular language?::A regular language is a language that can be recognized by a finite automaton and can be described using regular expressions.

What are the three main operations used in regular expressions?
?
The three main operations in regular expressions are:
  - **Union** ($L_1 \cup L_2$): Combines two languages. 
  - **Concatenation** ($L_1 L_2$): Joins strings from two languages.
  - **Kleene star** ($L^*$): Allows repetition of strings from a language.


What is the recursive definition of regular languages?
?
The recursive definition of regular languages states:
  - **Base cases**: $\emptyset$, $\{\Lambda\}$, and $\{a\}$ (for every $a \in \Sigma$) are regular languages.
  - **Inductive step**: If $\mathcal{L}_1, \mathcal{L}_2$ are regular languages, then:
    - $\mathcal{L}_1 \cup \mathcal{L}_2$ (union) is regular.
    - $\mathcal{L}_1 \mathcal{L}_2$ (concatenation) is regular.
    - $\mathcal{L}_1^*$ (Kleene star) is regular.


What is the basis of regular expressions?
?
The basis of regular expressions consists of:
  - $\emptyset$ (empty set)
  - $\Lambda$ (empty string)
  - $a$ for each $a \in \Sigma$ (single-character expressions).

How are set operations represented in regular expressions?
?
Set operations in regular expressions are represented as:
  - **Union**: $\cup$ is replaced with `+` (e.g., $a \cup b$ → `a + b`).
  - **Concatenation**: Implied by adjacency (e.g., `ab` means `a` followed by `b`).
  - **Kleene star**: Represented as `*` (e.g., $(a + b)^*$).


What does it mean for two regular expressions to be equivalent?
?
Two regular expressions are equivalent if they define the same language: $$E_1 = E_2 \Leftrightarrow \mathcal{L}(E_1) = \mathcal{L}(E_2)$$

## Deterministic Finite Automata

What is a Deterministic Finite Automaton (DFA)?::A DFA is a theoretical model of computation that recognizes regular languages by processing input symbols one at a time and determining acceptance or rejection based on a finite set of states.

What are the key characteristics of a DFA?
?
  - **Input/Output Behavior**: Reads symbols one at a time and accepts or rejects the input.  
  - **Simplicity**: Uses a finite number of states and limited memory.  
  - **Operation**: Starts in an initial state, transitions based on input, and accepts if it reaches an accepting state.

How is a DFA formally defined?
?
A DFA is defined as a 5-tuple $M = (Q, \Sigma, q_0, A, \delta)$, where:  
  - $Q$: Finite set of states.  
  - $\Sigma$: Input alphabet.  
  - $q_0 \in Q$: Initial state.  
  - $A \subseteq Q$: Accepting states.  
  - $\delta: Q \times \Sigma \to Q$: Transition function.

What is the extended transition function in a DFA?
?
The extended transition function $\delta^*$ is recursively defined as:  
  1. $\delta^*(q, \Lambda) = q$  
  2. $\delta^*(q, aw) = \delta^*(\delta(q, a), w)$  

What is the intuition behind the extended transition function $\delta^*$ in a DFA?
?
The extended transition function $\delta^*$ defines how a DFA processes an entire string recursively.  
  - It starts in the initial state and processes the input symbol by symbol.
  - For an empty string $\Lambda$, the DFA stays in the same state.
  - For a non-empty string $aw$, it first processes $a$, transitioning to a new state, and then recursively processes the rest of $w$.
  - This allows $\delta^*$ to determine the final state reached after consuming an entire input string.  

What is the acceptance condition of a DFA?::A string $w \in \Sigma^*$ is accepted if $\delta^*(q_0, w) \in A$.

What is an incomplete DFA?::An incomplete DFA is one where the transition function $\delta$ is **partial**, meaning some transitions are undefined.

How can an incomplete DFA be completed?::An incomplete DFA can be completed by adding an explicit **error state** (trap state) that absorbs all undefined transitions.

What operations on languages can be implemented using DFAs?::DFAs can be constructed to accept the **union, intersection, difference, or complement** of two regular languages.

How can a DFA be constructed for the union, intersection, or difference of two languages?
?
A composite DFA can be constructed by combining the states of two DFAs:  
  - **Union**: Accepts if at least one DFA accepts.  
  - **Intersection**: Accepts if both DFAs accept.  
  - **Difference**: Accepts if the first DFA accepts and the second does not.

What is the state explosion problem in composite automata?::The number of states in a composite DFA can be as large as $|Q_1| \times |Q_2|$, though many are often unnecessary.

How can composite automata be optimized?::Unreachable or redundant states can be removed, and minimization techniques can reduce the number of states to the smallest possible DFA.

