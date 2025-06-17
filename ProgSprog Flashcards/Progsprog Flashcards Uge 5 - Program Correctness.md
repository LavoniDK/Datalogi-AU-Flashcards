____
#flashcards/ProgSprog/4_Program-Correctness

What is **regression testing**?::Regression testing is the process of re-running previously completed tests to ensure that **new code changes** have **not introduced bugs** or broken **existing functionality**.
<!--SR:!2025-09-10,112,295-->


What is unit testing?::Unit testing involves testing individual components (functions, classes, modules) in isolation.
<!--SR:!2025-09-21,119,290-->

What is test-driven development (TDD)?::TDD is a methodology where tests are written before implementation, guiding the design process.
<!--SR:!2025-06-11,58,315-->

What are assertions in testing?::Assertions are used inside programs to enforce invariants and verify expected conditions. Some languages allow assertions to be toggled on/off during compilation.
<!--SR:!2025-10-03,129,295-->

What is property-based testing?::Property-based testing verifies function properties against many automatically generated inputs instead of testing specific examples (e.g., QuickCheck in Haskell).
<!--SR:!2025-09-22,120,295-->

Why is proving program correctness challenging?::Proving correctness is difficult because function equivalence is often undecidable, requiring reasoning over all possible inputs and outputs.
<!--SR:!2025-07-06,61,312-->

What is equational reasoning?::Equational reasoning is a technique used in functional programming to transform and simplify programs based on mathematical laws. It is harder in imperative programming due to side effects.
<!--SR:!2025-07-14,67,275-->