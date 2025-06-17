___
#flashcards/ProgSprog/12_Demand-Driven-Computation

## Streams and Lazy Evaluation

How does a stream differ from a regular list?::A stream is lazily evaluated and can be infinite, whereas a list is strictly evaluated and finite.
<!--SR:!2025-06-11,17,250-->

Why are streams used instead of lists in iterative pipelines?::To avoid creating and traversing intermediate collections unnecessarily.
<!--SR:!2025-06-13,19,250-->

What is a stream in functional programming?::A lazy list where computation is delayed using thunks and built only when needed.
<!--SR:!2025-06-22,28,270-->