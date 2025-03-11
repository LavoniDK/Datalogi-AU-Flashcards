___

#flashcards/ProgSprog/1_Introduction-and-Arithmetic-Expressions

- What is a Turing machine?::A Turing machine is a theoretical model of imperative computation that manipulates symbols on a tape according to a set of rules, used to simulate any algorithm.
<!--SR:!2025-03-16,33,273-->

- What is lambda calculus?::Lambda calculus is a formal system for expressing computation through function abstraction and application, serving as a foundation for functional programming.
<!--SR:!2025-03-30,46,290-->

- What is the Church-Turing Thesis?::The Church-Turing Thesis posits that any computation that can be performed by a physical machine can also be performed by a Turing machine.
<!--SR:!2025-06-25,106,290-->

- What is abstraction in programming?::Abstraction is the process of hiding implementation details and exposing only the essential features of a system to reduce complexity.
<!--SR:!2025-03-16,32,270-->

- What is encapsulation?::Encapsulation is a mechanism to bundle data (state) and methods (operations) together, restricting access to internal details. It enforces a **boundary** between a system’s implementation and its external interface.
<!--SR:!2025-05-18,68,273-->

- What is a Universal Turing Machine?::A Universal Turing Machine is a theoretical machine capable of simulating any other Turing machine by taking a description of the machine and its input as input.
<!--SR:!2025-06-18,99,293-->

- What is the difference between declarative and imperative languages?::Declarative languages express the logic of a computation without specifying its control flow, while imperative languages focus on how the computation is performed. Declarative programs defines *what* the desired outcome is without explicitly outlining the steps to achieve it, while Imperative programs focuses on *how* a problem should be solved, outlining the steps needed to reach the desired outcome.
<!--SR:!2025-06-30,111,293-->

- What are functional languages?::Functional languages are stateless programming languages that emphasize the use of functions, immutability, and declarative programming, such as Haskell or Lisp.
<!--SR:!2025-03-25,43,293-->

- What are object-oriented languages?::Object-oriented languages are based on the concept of objects that encapsulate data and behavior, supporting principles like inheritance, polymorphism, and encapsulation.
<!--SR:!2025-03-23,41,293-->

- What is the difference between static and dynamic typing?::Static typing checks types at compile time, while dynamic typing checks types at runtime.
<!--SR:!2025-03-28,45,290-->

- What is type inference?::Type inference is the ability of a programming language to automatically deduce the types of expressions without explicit annotations.
<!--SR:!2025-03-20,38,293-->

- What is the difference between interpreters and compilers?::Interpreters execute code line-by-line (either on an abstract machine or directly on hardware), while compilers translate code into another language, often to machine-executable format, which then is interpreted by the CPU.
<!--SR:!2025-03-19,38,293-->

- How can CPUs be viewed as interpreters?::CPUs can be viewed as interpreters implemented on hardware that execute machine code instructions directly, interpreting the binary representation of operations.
<!--SR:!2025-03-30,47,293-->

- What does it mean to bootstrap a compiler?::Bootstrapping a compiler involves writing a compiler for a programming language in the same language it compiles.
<!--SR:!2025-04-22,65,313-->

- What are the common ways programs are represented?::Programs are commonly represented as source code, abstract syntax trees (ASTs), or intermediate representations (IR).
<!--SR:!2025-05-14,74,273-->

- What is a source language?::A source language is the programming language in which code is written before being compiled or interpreted.
<!--SR:!2025-03-29,46,293-->

- What is concrete syntax?::Concrete syntax refers to the actual representation of a language's constructs as written by programmers, including symbols and structure.
<!--SR:!2025-03-26,44,293-->

- What is abstract syntax?::Abstract syntax represents the logical structure of code, stripped of syntactic details, often as an abstract syntax tree (AST).
<!--SR:!2025-03-15,23,233-->

- What are dynamic semantics?::Dynamic semantics define the runtime behavior of a program, specifying how its state changes during execution.
<!--SR:!2025-03-14,32,270-->

- What are static semantics?::Static semantics define rules that are checked at compile time, such as type correctness and variable declarations.
<!--SR:!2025-05-17,67,273-->

- What is an expression?::An expression is a combination of variables, values, operators, and functions that is evaluated to produce a result.
<!--SR:!2025-04-24,66,315-->

- What is an object language?::An object language is the language being analyzed, described, or implemented, such as MiniScala.
<!--SR:!2025-06-15,96,295-->

- What is a meta language?::A meta language is used to describe, define, or implement an object language, , often in the context of formal grammars or semantics. Examples include Scala, math, BNF-notation, or spoken language.
<!--SR:!2025-04-02,45,292-->

- What is BNF notation?::Backus-Naur Form (BNF) is a notation used to formally define the grammar of a language by specifying its syntax rules.
<!--SR:!2025-04-21,63,315-->

- What is a parse tree?::A parse tree represents the hierarchical structure of an expression according to a grammar, showing how the grammar rules are applied.
<!--SR:!2025-04-14,57,315-->

- What are terminals, non-terminals, and productions in the scope of grammars?::Terminals are the actual symbols in an expression, non-terminals are abstract categories like `Exp`, and productions are the rules defining how expressions are constructed.
<!--SR:!2025-03-12,29,275-->

- What are ambiguous expressions?::Ambiguous expressions are expressions that can be parsed in multiple legal ways according to a grammar.
<!--SR:!2025-06-30,111,295-->

- What are precedence and associativity rules?::Precedence rules determine the order in which operators are applied, and associativity rules define how operators of the same precedence are grouped.
<!--SR:!2025-03-22,39,292-->

- What is an abstract syntax tree (AST)?::An AST is a simplified version of a parse tree that abstracts away irrelevant details.
<!--SR:!2025-04-16,59,318-->

- What is parsing?::Parsing is the process of transforming a program's textual representation into an abstract syntax tree (AST).
<!--SR:!2025-04-19,62,315-->

- What are abstract classes?::Abstract classes are classes that define common properties and methods for a group of related subclasses but cannot be instantiated on their own.
<!--SR:!2025-05-31,95,295-->

- What are subclasses and superclasses?::Subclasses inherit properties and methods from their superclass, allowing for specialization and reuse of functionality.
<!--SR:!2025-04-23,65,312-->

- What are inductive data types?::Inductive data types are types that can recursively contain other values of the same type, such as trees or linked lists.
<!--SR:!2025-05-15,75,292-->

- What is the difference between atomic and composite values in inductive data types?::Atomic values are independent and self-contained, while composite values are constructed by combining atomic or other composite values.
<!--SR:!2025-03-21,39,295-->
