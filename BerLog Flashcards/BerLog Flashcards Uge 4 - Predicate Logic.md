___

#flashcards/BerLog/4_Predicate-Logic 


What is a logical predicate?::A function that returns a truth value when applied to specific values, expressing a property or relationship involving variables.
<!--SR:!2025-12-08,180,310-->

The building blocks of predicate logic, is denoted as the Vocabulary, how is the sets of elements in the vocabulary defined?
?
Vocabulary ($\Sigma=(C,F,P,V)$):
- $C$: Set of constants (representing fixed objects). Each has no arity. Examples: $\{0, 1, a, b, alice, bob\}$. Constants represent specific, named objects.
- $F$: Set of function symbols (denoting total functions on objects). Each function symbol has an *arity*. Examples: $\{add/2, multiply/2, successor/1, motherOf/1\}$. $add/2$ signifies *add* is a 2-ary function.
- $P$: Set of predicate symbols (denoting relations between objects). Each predicate symbol also has an *arity*.
- $V$: Set of variables (representing arbitrary objects). Infinite, denumerable. Typically: $\{x, y, z, x_1, y_1, z_{1}, ...\}$. Variables represent unknown or unspecified objects and are used with quantifiers.
<!--SR:!2025-10-15,148,301-->


Give a formal grammar, that defines terms::$T ::= V\; | \; C \;| \; F(T_1, ..., T_n)$
<!--SR:!2025-07-18,73,295-->

How are Formulas constructed?::From Terms, and Boolean operators and quantifiers.
<!--SR:!2025-08-11,63,276-->

What is a bound variable?::A variable $x$ in $\varphi$ is bound if it occurs within the scope of $\forall x$ or $\exists x$.
<!--SR:!2025-07-16,49,270-->

What is a closed formula (sentence)?::A formula with no free variables. Its truth value is independent of any variable assignment.
<!--SR:!2025-06-25,28,290-->

Explain why capture avoidance is important:Consider $(\exists y. x < y)[y+1/x]$ :: If we directly substitute, we get $\exists y. y+1 < y$, which is not what was intended!, therefore Rename the inner $y$ first: $(\exists z. x < z)[y+1/x]$ becomes $\exists z. y+1 < z$.
<!--SR:!2025-12-31,205,310-->

What is $\varphi[t/x]$?::substituting *all* free occurrences of variable $x$ in formula $\varphi$ with the term $t$.
<!--SR:!2025-06-26,29,290-->

How can Universal Introduction ($∀i$) be used?::To prove $\forall x. \varphi$, show that $\varphi$ holds for an *arbitrary* x.
<!--SR:!2025-11-30,174,310-->

What are the restrictions when using Universal Introduction ($∀i$)::$x_0$ *must not* appear free in the premises or conclusion outside the box
<!--SR:!2025-09-07,88,250-->

How can Universal Elimination ($∀e$) be used?::From $\forall x.\varphi$, you can infer $\varphi[t/x]$ for any term $t$.
<!--SR:!2025-09-27,133,296-->

How can Existential Introduction ($∃i$) be used?::From $\varphi[t/x]$, you can infer $\exists x. \varphi$ for any term $t$.
<!--SR:!2025-07-22,43,255-->

What does the definition of truth depend on in predicate logic?::How we define our overarching model and variable assignments.
<!--SR:!2025-11-10,154,301-->

What does a model consist of in semantic entailment?
?
- Model ($\mathcal{M}$)*, where each symbol is assigned meaning:
	-  $A$: A non-empty set, called the *universe of discourse*. This is the set of all possible objects.
	-  $c_M$: For each constant $c \in C$, an element $c_M \in A$. Interpretation of the constant.
	-  $f_M$: For each function symbol $f \in F$ (arity $n$), a function $f_M : A^n \rightarrow A$. Interprets a n-ary function.
	* $p_M$: For each predicate symbol $p \in P$ (arity $n$), a relation $p_M \subseteq A^n$. Tells us when the relations hold between items from A.
- Lookup Table ($\ell$): A partial function $\ell : V \rightarrow A$ assigning elements of the universe $A$ to variables. This assignment is also called a *valuation*.
<!--SR:!2025-07-27,82,276-->

When does two terms evaluate to the same element under some model and valuation?(formally)::$\mathcal{M}, \ell \vDash t_1 = t_2$ if ${[\![t_1]\!]_l = [\![t_2]\!]_l}$
<!--SR:!2025-07-15,36,210-->

List results that characterizes the fundamental properties of predicate logic::Soundness, Completeness, Undecidability, Expressivity.
<!--SR:!2025-09-07,118,296-->

What is the meaning of Undecidability in predicate logic?::There is no algorithm that, given a formula $\varphi$, can always determine whether $\vDash \varphi$ (or $\vdash \varphi$).
<!--SR:!2025-10-04,139,296-->

What is the meaning of Compactness in predicate logic?::If every finite subset of a set of formulas $\Gamma$ is satisfiable, then the entire set $\Gamma$ is satisfiable
<!--SR:!2025-06-23,26,281-->

Certain concepts, like ==transitive closure/reachability==, cannot be expressed in standard first-order predicate logic.
<!--SR:!2025-06-21,69,316-->