___
#flashcards/BerLog/1_Formal-Language-Theory

## Formal Languages

What is the null string ($\Lambda$)?::The null string is an empty string with a length of 0.
<!--SR:!2025-04-21,63,310-->

What does $\Sigma^*$ represent?::$\Sigma^*$ is the set of all strings over the alphabet $\Sigma$, including the null string $\Lambda$.
<!--SR:!2025-03-31,47,292-->

What is a finite language?::A finite language is a subset of $\Sigma^*$ containing a finite number of strings.
<!--SR:!2025-05-13,73,272-->

Define an alphabet ($\Sigma$) and strings.
?
An alphabet is a finite set of symbols, such as $\{a, b\}$ or $\{0, 1\}$. Strings are finite sequences of symbols from the alphabet.
<!--SR:!2025-04-17,59,312-->

What are the properties of string concatenation?
?
  - $\Lambda \cdot x = x \cdot \Lambda = x$
  - $|x\cdot y| = |x| + |y|$
  - Associativity: $(x \cdot y)\cdot z = x \cdot (y\cdot z)$
<!--SR:!2025-04-18,48,252-->

How do we distinguish between an alphabet consisting of Roman letters and an alphabet where symbols are English words?
?
- **Letter-based alphabet**: $\Sigma = \{a, b, ..., z\}$
	 - Symbols are single characters (letters).
	 - Strings are sequences of letters (e.g., `"hello"` as `h, e, l, l, o`).
	 - Useful for studying spelling and syntax at the character level.
- **Word-based alphabet**: $\Sigma = \{\text{"hello"}, \text{"world"}, ...\}$
	 - Symbols are entire words.
	 - Strings are sequences of words (e.g., `"hello world"` as `hello, world`).
	 - Useful for modeling languages at the lexical level (e.g., NLP, phrase structures).
- **Key distinction:** The atomic units in the alphabet change from individual characters to whole words, affecting how formal languages and automata process strings.
<!--SR:!2025-05-08,74,335-->

What is a prefix of a string?::A prefix is an initial segment of a string up to some position.
<!--SR:!2025-05-05,74,320-->

What is a suffix of a string?::A suffix is a final segment of a string starting from some position.
<!--SR:!2025-04-29,70,320-->

What is a substring of a string $s$?::A substring is any contiguous sequence of characters within $s$.
<!--SR:!2025-04-28,69,318-->

What is the special property of the null string ($\Lambda$) regarding substrings?::The null string ($\Lambda$) is a prefix, suffix, and substring of any string.
<!--SR:!2025-04-27,68,319-->

A language is a **==set of strings over an alphabet of symbols==**.
<!--SR:!2025-03-20,38,290-->

**String operations** include concatenation, where $x \in L_1$ and $y \in L_2$ form **==the string $x\cdot y$==**.
<!--SR:!2025-03-25,42,291-->

The **Kleene star** $L^*$ is defined as::The union of all possible concatenations of strings in $L$, including $\Lambda$. Formally, $L^* = \bigcup_{k \geq 0} L^k$.
<!--SR:!2025-03-17,33,272-->

What is the difference between generative and property-based definitions of languages?
?
- Generative definitions describe how to generate strings in the language.
	- Example: $L_1 = \{ab, bab\}^* \cup \{b\}\{ba\}^*\{ab\}^*$.
- Property-based definitions specify a property that all strings in the language must satisfy.
	- Example: $L_2 = \{x \in \{a, b\}^* \mid n_a(x) > n_b(x)\}$.
<!--SR:!2025-04-18,60,312-->


What are the properties of string reversal?
?
  - $\Lambda^R = \Lambda$
  - $(au)^R = u^R a$
  - Reverse-distributive: $(uv)^R = v^R u^R$
  - Self-inverse: $(u^R)^R = u$
<!--SR:!2025-03-15,31,295-->

What are the properties of string repetition?
?
  - $u^0 = \Lambda$
  - $u^{n+1} = u(u^n)$
  - $u^m u^n = u^{m+n}$
  - $(u^m)^n = u^{mn}$
<!--SR:!2025-04-05,46,295-->

What are the properties/recursive definition of the occurrence count operation?
?
  - $n_{\sigma}(\Lambda) = 0$
  - $n_{\sigma}(au) = 1 + n_{\sigma}(u)$ if $\sigma = a$
  - $n_{\sigma}(au) = n_{\sigma}(u)$ if $\sigma \neq a$
<!--SR:!2025-04-07,49,315-->

What is the complement of a language?::The complement of a language $L$ is $L' = \Sigma^* - L = \{u \mid u \in \Sigma^*, u \notin L\}$.
<!--SR:!2025-04-04,46,315-->

What is language concatenation? :: Language concatenation is the combination of two languages. It includes all combinations of concatenating one element from each language together. $L_1 L_2 = \{xy \mid x \in L_1, y \in L_2\}$.
<!--SR:!2025-04-30,69,324-->

What is the reverse of a language?::The reverse of a language $L$ is $L^R = \{u^R \mid u \in L\}$.
<!--SR:!2025-05-10,74,332-->

What is language exponentiation?
?
Exponentiation of a language is repeated concatenation, defined as:
  - $L^0 = \{\Lambda\}$
  - $L^k = L L^{k-1}$
<!--SR:!2025-04-17,52,305-->

What is the positive closure of a language?::The positive closure (Kleene Star) of a language $L^+$ is $L^+ = \bigcup_{k \geq 1} L^k$, omitting the empty string.
<!--SR:!2025-04-18,53,304-->

What are the properties of the Kleene star?
?
- $L^{+}=LL^{*}$
- $L^{*}=\{\Lambda\}\cup L^{+}$
- if $\Lambda \in L$ then $L^{*}=LL^{*}=L^{+}$
- $\emptyset^{+}=\emptyset$
- $\emptyset^{*}=\emptyset^{0}=\{\Lambda\}$
<!--SR:!2025-05-17,67,275-->

## Recursive definitions

What are the two key components of a recursive definition?
?
1. **Basis statement** that specifies one or more initial elements in the set.
2. **Recursive rules** that define how to construct new elements using elements already in the set.
<!--SR:!2025-04-13,57,312-->

How is the closure property of $\mathbb{N}$ described in its recursive definition?::Through the successor operation. $\mathbb{N}$ is closed under the successor operation.
<!--SR:!2025-04-15,57,311-->

Define the natural numbers $\mathbb{N}$ recursively.
?
1. $0 \in \mathbb{N}$ (basis).
2. If $n \in \mathbb{N}$, then $n+1 \in \mathbb{N}$ (successor operation).
3. $\mathbb{N}$ is the smallest set satisfying (1) and (2).
<!--SR:!2025-04-22,64,314-->


How is the set of all strings $\Sigma^*$ over $\{a, b\}$ defined recursively?
?
1. $\Lambda \in \Sigma^*$ (basis, empty string).
2. If $x \in \Sigma^*$, then $x\cdot a \in \Sigma^*$ and $x\cdot b \in \Sigma^*$.
<!--SR:!2025-03-18,33,270-->

## Structural Induction

What is strong induction?::A variation of induction where you assume the property is true for all values less than or equal to the current value during the inductive step.
<!--SR:!2025-04-23,65,312-->

Structural induction is ==a generalization of induction, used to prove properties about recursively defined structures==
<!--SR:!2025-07-03,114,299-->

## Regular Expression and Languages

What is a regular language?::A regular language is a language that can be recognized by a finite automaton and can be described using regular expressions.
<!--SR:!2025-03-30,41,312-->

What are the three main operations used in regular expressions?
?
The three main operations in regular expressions are:
  - **Union** ($L_1 \cup L_2$): Combines two languages.
  - **Concatenation** ($L_1 L_2$): Joins strings from two languages.
  - **Kleene star** ($L^*$): Allows repetition of strings from a language.
<!--SR:!2025-05-12,76,332-->


What is the recursive definition of regular languages?
?
The recursive definition of regular languages states:
  - **Base cases**: $\emptyset$, $\{\Lambda\}$, and $\{a\}$ (for every $a \in \Sigma$) are regular languages.
  - **Inductive step**: If $\mathcal{L}_1, \mathcal{L}_2$ are regular languages, then:
    - $\mathcal{L}_1 \cup \mathcal{L}_2$ (union) is regular.
    - $\mathcal{L}_1 \mathcal{L}_2$ (concatenation) is regular.
    - $\mathcal{L}_1^*$ (Kleene star) is regular.
<!--SR:!2025-03-28,39,304--><

What does it mean for two regular expressions to be equivalent?
?
Two regular expressions are equivalent if they define the same language: $$E_1 = E_2 \Leftrightarrow \mathcal{L}(E_1) = \mathcal{L}(E_2)$$
<!--SR:!2025-04-06,48,312-->

## Deterministic Finite Automata

What is a Deterministic Finite Automaton (DFA)?::A DFA is a theoretical model of computation that recognizes regular languages by processing input symbols one at a time and determining acceptance or rejection based on a finite set of states.
<!--SR:!2025-05-02,71,325-->


How is a DFA formally defined?
?
A DFA is defined as a 5-tuple $M = (Q, \Sigma, q_0, A, \delta)$, where:
  - $Q$: Finite set of states.
  - $\Sigma$: Input alphabet.
  - $q_0 \in Q$: Initial state.
  - $A \subseteq Q$: Accepting states.
  - $\delta: Q \times \Sigma \to Q$: Transition function.
<!--SR:!2025-05-08,74,334-->

What is the extended transition function in a DFA?
?
The extended transition function $\delta^*$ is recursively defined as:
  1. $\delta^*(q, \Lambda) = q$
  2. $\delta^*(q, aw) = \delta^*(\delta(q, a), w)$
<!--SR:!2025-03-27,38,292-->

What is the intuition behind the extended transition function $\delta^*$ in a DFA?
?
The extended transition function $\delta^*$ defines how a DFA processes an entire string recursively.
  - It starts in the initial state and processes the input symbol by symbol.
  - For an empty string $\Lambda$, the DFA stays in the same state.
  - For a non-empty string $aw$, it first processes $a$, transitioning to a new state, and then recursively processes the rest of $w$.
  - This allows $\delta^*$ to determine the final state reached after consuming an entire input string.
<!--SR:!2025-05-12,77,335-->

What is the acceptance condition of a DFA?::A string $w \in \Sigma^*$ is accepted if $\delta^*(q_0, w) \in A$.
<!--SR:!2025-03-18,31,284-->

What is an incomplete DFA?::An incomplete DFA is one where the transition function $\delta$ is **partial**, meaning some transitions are undefined.
<!--SR:!2025-03-13,28,284-->

How can an incomplete DFA be completed?::An incomplete DFA can be completed by adding an explicit **error state** (trap state) that absorbs all undefined transitions.
<!--SR:!2025-05-07,73,332-->


