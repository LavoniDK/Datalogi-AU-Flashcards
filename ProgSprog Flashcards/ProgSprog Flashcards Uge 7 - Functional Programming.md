____
#flashcards/ProgSprog/7_Functional-Programming 

What is a pure function?::A pure function always returns the same output for the same input and has no side effects, meaning it does not modify state or interact with external systems.
<!--SR:!2025-03-15,4,270-->

What is lazy evaluation?::Lazy evaluation delays computation until the result is needed, optimizing performance and enabling the creation of infinite data structures.
<!--SR:!2025-03-14,3,250-->

What is call-by-name evaluation?::Call-by-name delays the evaluation of an argument until it is actually used in the function body, instead of evaluating it before passing it to the function.
<!--SR:!2025-03-12,1,230-->

What is a thunk in call-by-name evaluation?::A thunk is a zero-argument lambda function that wraps an expression, delaying its evaluation until needed.
<!--SR:!2025-03-15,4,270-->

What is parametric polymorphism?::Parametric polymorphism (generics) allows functions and data structures to operate on different types without specifying them in advance, using type parameters.
<!--SR:!2025-03-14,3,250-->

What is an immutable accumulator in iteration?::An immutable accumulator is a technique where, instead of modifying a variable in a loop, the accumulator is passed as an argument to a recursive function, preserving immutability.
<!--SR:!2025-03-15,4,270-->

What is `fold left` in functional programming?::`Fold left` (also called `reduceLeft`, `foldl`, or `fold`) is a higher-order function that processes a collection by applying a binary operation from left to right, accumulating results.
<!--SR:!2025-03-14,3,250-->