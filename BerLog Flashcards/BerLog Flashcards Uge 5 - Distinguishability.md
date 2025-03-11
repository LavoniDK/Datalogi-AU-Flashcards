___
#flashcards/BerLog/5_Distinguishability 

## Distinguishability and DFA Minimization
 
What does it mean for two words to be **distinguished** by another word $z$?::Two words $x$ and $y$ are **distinguished** by $z$ if $xz \in L$ and $yz \notin L$, or vice versa.
<!--SR:!2025-03-14,3,259-->

What does it mean for two words to be **indistinguishable** with respect to a language $L$?::Two words $x$ and $y$ are **indistinguishable** if for all words $z$, $xz \in L \Leftrightarrow yz \in L$.
<!--SR:!2025-03-14,3,259-->

What does the equivalence relation $\equiv_L$ represent?::It represents **indistinguishability** with respect to $L$, meaning two words behave the same way when extended with any suffix.
<!--SR:!2025-03-14,3,259-->

What does Myhill-Nerode theorem say about regular languages?::A language $L$ is **regular** if and only if $\equiv_L$ partitions $\Sigma^*$ into **finitely many equivalence classes**.
<!--SR:!2025-03-15,4,280-->

What is the key idea behind DFA minimization?::Merge states that are **indistinguishable**, since they accept the same language.
<!--SR:!2025-03-14,3,258-->

How does distinguishability help in proving that a language is **not regular**?
?
1. Find an **infinite set** of words that are **pairwise distinguishable** in $L$.
2. By Theorem 2.21(b), any DFA recognizing $L$ must have **at least as many states** as the number of distinguishable words.
3. If this number exceeds **any finite bound**, then no finite-state DFA can exist for $L$, proving it is **not regular**.
<!--SR:!2025-03-14,3,250-->

Why is the language of **palindromes** not regular?
?
- Consider $Pal = \{w \mid w = w^r\}$.
- Any two distinct words $x, y$ in $\{a, b\}^*$ are **pairwise distinguishable** in $Pal$.
- By Theorem 2.21(b), this means an **infinite number of states** would be required in any DFA recognizing $Pal$.
- Since a DFA must have **finitely many** states, no such DFA can exist for $Pal$, proving it is **not regular**.
<!--SR:!2025-03-15,4,270-->

The equivalence relation $\equiv_L$ **==partitions $\Sigma^*$ into equivalence classes based on indistinguishability==**.
<!--SR:!2025-03-15,4,278-->  

Theorem 2.21(b) says that if we find **==$n$ pairwise distinguishable words in $L$==**, then **any DFA recognizing $L$ must have at least $n$ states**.
<!--SR:!2025-03-15,4,280-->  

A **language is not regular** if we can show that **==it requires an infinite number of distinguishable states==**.
<!--SR:!2025-03-14,3,259-->  

The **language of palindromes** is **not regular** because **==every pair of distinct words is distinguishable, requiring infinitely many states==**.
<!--SR:!2025-03-15,4,278-->  

## Pumping Lemma and Closure Properties

The **Pigeonhole Principle** ensures that in a DFA, a word with **==as many or more symbols than states==** must contain **==a repeated state==**.
<!--SR:!2025-03-14,3,258!2025-03-15,4,280-->  

If $L_{1}$ and $L_{2}$ are regular, what operations also remain regular?
?
- $L_{1}^{*}, L_{1}L_{2}$ and $L_{1}\cup L_{2}$ (definition of regular expressions and languages)
- $L_{1}'$
- $L_{1}\cap L_{2}$
- $L_{1}\setminus L_{2}$
- $L^{R}$
<!--SR:!2025-03-15,4,270-->


If $X\subseteq_{fin} \Sigma^{*}$ is a finite language, what can be said about its regularity?::every finite language is regular
<!--SR:!2025-03-15,4,270-->

The problem *"Given DFA $M$ and word $w$ is $w\in \mathcal{L}(M)$?"* is a ==decision problem, (a question that given some finite inputs requires a yes/no answer)==
<!--SR:!2025-03-15,4,280-->

If something is undecidable, what does that imply about its computational sufficiency?::It is **not a fully sufficient model of computation**.
<!--SR:!2025-03-15,4,278-->

Why are closure properties important in language theory?::They allow us to build more complex languages from simpler ones, while still ensuring that the resulting language maintains certain desirable properties, like regularity
<!--SR:!2025-03-15,4,270-->

What does the **Pumping Lemma** state about regular languages?::If a language is regular, if there is an sufficiently long word, it can be split into three parts $z = uvw$ where $v$ can be **pumped** (repeated any number of times) while still remaining in the language.
<!--SR:!2025-03-14,3,258-->

What does the **contraposition** of the Pumping Lemma state?::If for **every** $k > 0$ we can find a word in $L$ that **fails the pumping conditions**, then $L$ is **not regular**.
<!--SR:!2025-03-14,3,259-->

Why is the Pumping Lemma only relevant for **infinite languages**?::Because it only provides constraints on words that exceed a certain length, which **finite languages never do**.
<!--SR:!2025-03-12,1,238-->

What is the key requirement to prove that a language is **non-regular** using the Pumping Lemma?::Find a word in the language **longer than $k$** that **cannot be pumped** while remaining in the language.
<!--SR:!2025-03-15,4,270-->

Why does the **Pumping Lemma** not contradict the fact that all finite languages are regular?
?
- The **universal quantifier** in the Pumping Lemma applies **only to words in $L$ of length at least $k$**.
- If $L$ is finite, there may be **no such words**, meaning the implication **$false \Rightarrow false$** holds, which is **true**.
- Therefore, the Pumping Lemma **does not apply to finite languages**, but this does not contradict their regularity.
<!--SR:!2025-03-15,4,279-->