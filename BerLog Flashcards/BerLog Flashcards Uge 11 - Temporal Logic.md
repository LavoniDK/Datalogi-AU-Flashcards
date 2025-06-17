___
#flashcards/BerLog/11-Temporal-Logic 

## Temporal Logic Overview

What is Temporal Logic used for in model checking?::It is used as a completely automated tool for model checking that handles concurrency but is limited to finite systems and can suffer from scalability issues.
<!--SR:!2025-06-25,12,247-->

Why are Deterministic Finite Automata (DFA) insufficient for reasoning about liveness properties?::Because liveness properties require reasoning about infinite behaviors, and DFAs work only with finite words. We need to consider infinite words ($\Sigma^\omega$) and $\omega$-regular expressions.
<!--SR:!2025-07-06,23,250-->

## LTL Syntax and Operators

What do the temporal operators $\mathbf{G}, \mathbf{F}, \mathbf{U}$ stand for in LTL?::They stand for **Globally** (always), **Eventually** (in the future), and **Until** respectively.
<!--SR:!2025-06-20,13,245-->

What are the main components of LTL formula syntax?:: $\varphi ::= p \mid \neg \varphi \mid \varphi \land \varphi \mid \varphi \lor \varphi \mid \mathbf{X} \varphi \mid \mathbf{F} \varphi \mid \mathbf{G} \varphi \mid \varphi ,\mathbf{U}, \psi \mid \varphi ,\mathbf{W}, \psi$
<!--SR:!2025-06-15,2,246-->

What does the operator $\mathbf{X} \varphi$ mean in LTL?::It means $\varphi$ holds in the next state (neXt).
<!--SR:!2025-06-18,5,230-->

What does $\varphi \,\mathbf{W}\, \psi$ mean in LTL?::It means $\varphi$ holds until $\psi$ holds (if at all). This is called **Weak Until**.
<!--SR:!2025-07-05,22,250-->

## Kripke Structures 

What is a Kripke structure?::A transition system $\mathcal{M} = (\mathcal{A}, S, \rightarrow, L)$ combining states, transitions, and labelings for atomic propositions.
<!--SR:!2025-06-15,2,225-->

What does the labeling function $L : S \rightarrow 2^{\mathcal{A}}$ define in a Kripke structure?::It defines which atomic propositions are true in each state.
<!--SR:!2025-06-26,19,267-->

How is a path $\pi$ defined in a Kripke structure?::An infinite sequence of states $\pi_0, \pi_1, \dots$ such that for all $i$, $(\pi_i \rightarrow \pi_{i+1})$.
<!--SR:!2025-06-26,13,245-->

What is the meaning of $\pi^i$?::It denotes the suffix of path $\pi$ starting at index $i$: $\pi_i, \pi_{i+1}, \dots$
<!--SR:!2025-06-26,13,230-->

## Semantics of LTL 

When does a path $\pi$ satisfy an atomic proposition $p$?::$\pi \models p \iff p \in L(\pi_0)$
<!--SR:!2025-06-18,5,225-->

When does $\pi$ satisfy $\mathbf{G} \varphi$?::$\pi \models \mathbf{G} \varphi \iff \forall i, \pi^i \models \varphi$
<!--SR:!2025-07-11,34,285-->

When does $\pi$ satisfy $\mathbf{F} \varphi$?::$\pi \models \mathbf{F} \varphi \iff \exists i, \pi^i \models \varphi$
<!--SR:!2025-06-21,8,265-->

When does $\pi$ satisfy $\varphi \,\mathbf{U}\, \psi$?::$\pi \models \varphi \,\mathbf{U}\, \psi \iff \exists i: \pi^i \models \psi$ and $\forall j < i: \pi^j \models \varphi$
<!--SR:!2025-06-18,5,225-->

When does $\pi$ satisfy $\mathbf{X} \varphi$?::$\pi \models \mathbf{X} \varphi \iff \pi^1 \models \varphi$
<!--SR:!2025-06-14,7,230-->

## Model Checking 

What is the LTL model checking problem?::Given a transition system $\mathcal{M}$ and an LTL property $\varphi$, check whether $\mathcal{M} \models \varphi$, i.e., all infinite paths from the initial state satisfy $\varphi$.
<!--SR:!2025-06-26,13,230-->