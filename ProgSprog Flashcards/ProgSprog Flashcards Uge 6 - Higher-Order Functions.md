____
#flashcards/ProgSprog/6_Higher-Order-Functions 

What is a higher-order function (HOF)?::A higher-order function is a function that takes another function as an argument or returns a function as a result.
<!--SR:!2025-06-16,64,314-->

What does it mean for a language to support functions as first-class values?::A language supports functions as first-class values if functions can be assigned to variables, passed as arguments, and returned from other functions.
<!--SR:!2025-06-09,57,314-->

How does MiniScala v5 support first-class functions?::MiniScala v5 unifies function and variable names into **identifiers** ($Id$) and extends environments to store function closures as values.
<!--SR:!2025-06-18,23,270-->

What is a closure in MiniScala v5?::A closure is a tuple $(Id, Exp, Env, \mathcal{P}(Decl))$ that includes a function's parameter, body, the environment at declaration, and the set of declarations in its scope.
<!--SR:!2025-10-02,128,290-->

What is currying?
?
Currying is the transformation of a function with multiple arguments into a sequence of functions, each taking a single argument.
Example:
  - Standard: `(a: Int, b: Int, c: Int) => a + b + c`
  - Curried: `(a: Int) => (b: Int) => (c: Int) => a + b + c`
<!--SR:!2025-09-08,111,294-->
