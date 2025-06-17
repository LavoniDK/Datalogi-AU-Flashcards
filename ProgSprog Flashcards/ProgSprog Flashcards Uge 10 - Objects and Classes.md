___
#flashcards/ProgSprog/10_Objects-and-Classes

## Object Syntax and Semantics


==Object== construction in MiniScala uses the ==`new`== keyword and dot syntax for ==field access==.
<!--SR:!2025-08-01,59,314!2025-06-04,15,294!2025-06-28,30,272-->

Why is field writing not allowed in this implementation of MiniScala?::To simplify implementation and promote good programming practices, instead setter methods should be used.
<!--SR:!2025-06-12,12,234-->

How can we achieve field mutation without direct field writing?::By adding setter methods to the class.
<!--SR:!2025-07-08,38,294-->

## Class Environment and Evaluation

What structure maps class names to their constructors in MiniScala?::`ClassEnv`, mapping class names to constructor tuples.
<!--SR:!2025-06-27,29,275-->

What does each constructor in `ClassEnv` contain?::A parameter name, constructor body, and the environment and class environment at declaration.
<!--SR:!2025-06-04,9,214-->

What is the new form of evaluation rules with objects in MiniScala?
?$$Env, ClassEnv, Sto \vdash Exp ⇒ Val, Sto$$ and $$Env, ClassEnv, Sto \vdash Decl ⇒ Env, ClassEnv, Sto$$

How is an object represented in the store in MiniScala?::As a value type that maps field/method names to values, like an environment.
<!--SR:!2025-06-12,17,254-->

==Objects== are stored as ==locations== in the store, not directly as values.
<!--SR:!2025-06-05,16,290!2025-07-10,44,290-->

## Operational Semantics of Object Creation

What is $\rho_{3}\downarrow F$ in the evaluation rule for object creation?::The environment restricted to the declared field and method names.
<!--SR:!2025-06-17,20,254-->

What does it mean that MiniScala passes objects by reference?::The function or method receives a reference (location) to the object, not a copy.
<!--SR:!2025-06-15,20,250-->

What is aliasing in object-oriented semantics?::Multiple variables referencing the same object in the store.
<!--SR:!2025-07-03,33,275-->

## Objects vs. Closures

How can closures be mimicked with objects?::A closure is an object with a single method.
<!--SR:!2025-07-12,42,295-->

How are closures internally represented in Java or Scala?::As objects with one method.
<!--SR:!2025-06-28,25,275-->

What is the purpose of the `this` keyword?::To refer to the current object instance from within a method. (In case an object is given the same reference name as some variable in it's body)
<!--SR:!2025-06-26,26,274-->

What does the `null` keyword represent?::An absence of value or uninitialized reference.
<!--SR:!2025-07-19,46,292-->

Why is `null` potentially dangerous in programming?::It can lead to runtime errors like null-pointer exceptions.
<!--SR:!2025-07-03,33,274-->

What is Scala's alternative to `null`?::`Option[T]`, a type-safe way to represent optional values.
<!--SR:!2025-06-21,18,234-->

## Comparing Objects

What does `x eq y` mean in Scala?::It checks if `x` and `y` refer to the same object (reference equality).
<!--SR:!2025-06-26,23,255-->

What does `x.equals(y)` do in Scala and Java?::It compares `x` and `y` by value (can be overridden).
<!--SR:!2025-06-13,17,255-->

What does `x == y` do in Scala?::Checks for null first, then compares using `.equals()`, which compares by value.
<!--SR:!2025-06-04,6,212-->

Why is `x == y` in Scala safer than Java's `x.equals(y)`?::It avoids null-pointer exceptions by checking for null before calling `.equals()`.
<!--SR:!2025-07-01,31,272-->