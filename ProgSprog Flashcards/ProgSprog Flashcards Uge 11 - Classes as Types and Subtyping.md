___
#flashcards/ProgSprog/11_Classes-as-Types

## Classes as Types

What is the purpose of extending MiniScala syntax with class names in type annotations?::To allow variables to only reference objects that are instances of the specified class.
<!--SR:!2025-06-18,21,250-->

Why can multiple class declarations use the same name in MiniScala?::Because class declarations are statically scoped.
<!--SR:!2025-06-09,9,210-->

How are class types compared in MiniScala?::By the source code position of the class declaration, not by class name.
<!--SR:!2025-06-09,6,210-->

## Inheritance

What does a sub-class inherit from a super-class?::Fields and methods.
<!--SR:!2025-06-20,17,265-->

What is dynamic dispatch?::Run-time method selection based on the run-time type of the receiver object.
<!--SR:!2025-06-08,13,230-->

What are virtual methods?::Methods that can be overridden by sub-classes.
<!--SR:!2025-07-18,45,290-->

What is method overriding?::When a method in a sub-class has the same name and parameter types as one in the super-class.
<!--SR:!2025-06-17,20,250-->

What is method overloading?::When two methods have the same name but different parameter types.
<!--SR:!2025-07-20,47,290-->

## Subtyping

What condition defines subtyping between types A and B?::B is a subtype of A if the set of B objects is a subset of A objects. Written as `B <: A`.
<!--SR:!2025-06-22,24,250-->

What is the special property of the `Nothing` type in Scala and MiniScala?::`Nothing` is the subtype of all types and has no values.
<!--SR:!2025-06-05,16,290-->

Is `Int <: Float` in MiniScala and Scala?
?
- In MiniScala: yes
- In Scala: no — Scala uses implicit conversion instead.
<!--SR:!2025-07-01,31,270-->

What does function subtyping require for input and output types?::Contravariant input types and covariant output types.
<!--SR:!2025-06-21,23,250-->

Provide the formal rule for function subtyping.
?
$$\frac{\tau_{1}' <: \tau_{1} \quad \tau_{2} <: \tau_{2}'}{\tau_{1} \rightarrow \tau_{2} <: \tau_{1}' \rightarrow \tau_{2}'}
$$
<!--SR:!2025-06-14,11,210-->

What is the variance of array subtyping in Scala?::Invariant.
<!--SR:!2025-06-25,22,250-->

How does variance annotation affect type parameters in Scala?
?
- `+A` enables covariance (read-only)
- `-A` enables contravariance (write-only)
- No symbol means invariance
<!--SR:!2025-06-06,11,250-->

How does variance differ between immutable and mutable Scala collections?::Immutable collections like `List[+A]` are covariant, as we can read, but not write from the collection; mutable collections like `Array[A]` are invariant as we allow both reading and writing.
<!--SR:!2025-06-14,11,210-->

## Generic Classes and Function Types

What are type bounds in generics?::Constraints on type parameters such as `T <: A` (upper) or `T >: A` (lower).
<!--SR:!2025-06-20,24,250-->

Why are upper bounds more common than lower bounds in practice?::Because they are more useful and less restrictive for safe parameterization. Lower bounds don’t guarantee method availability - you're only assured the type is a supertype of something.
<!--SR:!2025-06-20,25,270-->

What is the Readers and Writers Principle?::Use covariant types for read-only (e.g., `Reader[+T]`) and contravariant for write-only (e.g., `Writer[-T]`).
<!--SR:!2025-06-09,6,230-->

Why are most common collections like `List[+A]` covariant?::Because they are designed for read operations and covariance is safe in that context.
<!--SR:!2025-06-16,13,250-->

What is the default variance in Scala generics?::Invariance.
<!--SR:!2025-06-30,30,270-->