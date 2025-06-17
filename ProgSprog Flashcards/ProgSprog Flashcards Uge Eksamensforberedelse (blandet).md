___
#flashcards/ProgSprog/Eksamensforberedelse_Blandet

How do environments look when functions are first-class values? What about before?
?
- When functions are first-class values, in MiniScala v5, environments must store function closures, as a values alongside other data types such as variables.
- Before functions were first-class, when they were first-order, in MiniScala v4, environments only needed to store mappings from variables to values, and we introduced a separate environment for functions, a _function environment_.
<!--SR:!2025-06-05,5,248-->

Outline the development stages of MiniScala. Which features was added in the different versions?
?
- v1: Arithmetic expressions
- v2: Variables, environments and block expressions
- v3: Booleans and tuples, logic and comparisons, branching and case-matching, dynamic and static type checking, type annotations
- v4: First-order functions
- v5: Higher-order functions, lambdas
- v6: Mutable state (via. the store) and imperative features (side effecting expressions, while-loops, mutable variables and assignment, null values (empty tuple))
- v7: Classes and objects, class-environments
- v8: Classes as types and subtyping
- Week 13-14, we added a compiler and abstract machine, but not a direct part of MiniScala.
<!--SR:!2025-06-05,5,249-->

How are lambda functions handled in the operational semantics?
?
Lambda functions are evaluated to **closures**, which pair the function's code with the current environment. This allows correct variable resolution during later function calls, especially for free variables captured from the defining scope.
<!--SR:!2025-06-05,5,248-->

Where is dynamic type checking defined? How does it differ from static type checking?
?
Dynamic type checking is integrated into the **operational semantics** — e.g., as side conditions in evaluation rules that ensure runtime values match annotated types. In contrast, static type checking is defined separately in the **type system**, independent of runtime execution (dynamic semantics).
<!--SR:!2025-06-05,5,249-->

What is the behavioral difference between assigning an object or a higher-order function (HOF) to a value (immutable, in distinction to variables)?
?
- Assigning an object binds a **reference (location in the store)**, so aliasing can cause mutations to be shared. Assigning a HOF binds a **closure value** directly in the environment (immutable by default), so copies are independent.
- If they instead were assigned to a variable (mutable), the behaviour would be close the same, since the closure now would be mutable and live in the store, but aliassing would still not be allowed since any assignment to the same variable, would require looking up the variable in the store, not just returning its location in the store, .
<!--SR:!2025-06-05,5,248-->

**Why does the type rule for annotated function calls require a subtype argument, while function subtyping requires a supertype (i.e., contravariant arguments)?**
?
- **Function subtyping** describes when _one function type_ can safely be used in place of another. It ensures that we can substitute one function for another without causing type errors. This is why it requires **contravariant parameter types** — a function that accepts more general inputs (supertypes) is more flexible and safer to substitute.
- **Annotated function calls**, on the other hand, fix the function and check the argument against its annotated type. In this case, we’re not substituting functions — only supplying an argument. Therefore, we require that the argument is a **subtype** of the annotated parameter type, as per the weak substitutability principle.
<!--SR:!2025-06-05,5,248-->

Why must arrays be invariant in their type to ensure soundness?
?
- Arrays are **mutable**, so allowing **covariance** (e.g., `Student[] <: Person[]`) enables **unsafe writes** — e.g., inserting a `Person` into an array that expects `Student`s.  
- Allowing **contravariance** (e.g., `Person[] <: Student[]`) enables **unsafe reads** — expecting a `Student` but getting a general `Person`.  
- Therefore, **invariance** is required to ensure both safe reads and writes.
<!--SR:!2025-06-05,5,249-->


Why is `Option[T]` in Scala a type-safe alternative to `null` in Java?
?
- `null` is an **untyped absence** that can be assigned to any reference type in Java, often leading to **runtime errors** (e.g., `NullPointerException`).
- `Option[T]` is a **type-safe, explicit** representation of optionality in Scala:
	- `Some(value)` represents presence.
	- `None` represents absence.
- This enforces handling of missing values **at compile time**, avoiding hidden nulls, e.g. using pattern matching, `.getOrElse(value)`, etc.
<!--SR:!2025-06-14,11,270-->


**What is the rebinding technique in MiniScala, and when is it used?**
?
- **Rebinding** is the technique of **inserting a binding for a name into the environment that a closure captures**, enabling **self-recursion**. **Mutual recursion** requires building an environment where **all definitions in the current block are rebound together**.
	- For **function closures**, a closure captures the environment at its **definition site**. If the function is recursive, rebinding injects the function’s own name into that environment, so the function can call itself.
	- For **classes**, rebinding injects the class into the **class environment** it captures, allowing the class to refer to itself (e.g., for instantiating objects of its own type in methods or fields).
<!--SR:!2025-06-13,10,270-->

How is direct and mutual recursion resolved of function closures resolved at different stages of the MiniScala development?
?
- **MiniScala v4**: Rebinding enables direct recursion (documented), rebinding entire environment simultanously by additionaly storing all declaration inside current block in the closure also allows mutual recursion (undocumented)
- **MiniScala v5**: In week 6, again mutual recursion is enabled the same way, but this is undocumented. In week 7 we introduce mutual recursion without rebinding, by using recursively defined environments, implemented using a higher-order function approach, exploiting the fact that defs (in the meta-language) can be recursive and lazily evaluated.
- **MiniScala v6**: With mutation we can make a simpler and more efficient implementation of recursively defined environments by making them mutable. We first building the closures without recursive environments and then overwrite the `env` field in each closure, pointing to the new environment. (undocumented)
<!--SR:!2025-06-10,7,250-->


How are class declarations scoped in MiniScala?
?
Class declarations are **statically scoped**, meaning the meaning of a class name is determined by its lexical position. To avoid conflicts, class type identity includes the **source code position**.
<!--SR:!2025-06-05,5,249-->


What is the purpose of the class type environment?
?
The class type environment:
$$\gamma \in ClassTypeEnv = Id \hookrightarrow Position \times Type \times TypeEnv
$$
Stores information about class types and is used by the type checker.
<!--SR:!2025-06-05,5,248-->


What is dynamic dispatch?
?
**Dynamic dispatch** (also called late binding) means method calls are resolved at **runtime** based on the object's runtime type. Overridden methods in subclasses replace superclass methods.
<!--SR:!2025-06-05,5,249-->



How does Scala handle method overriding?
?
Scala requires the `override` keyword to make overriding **explicit** and avoid accidental override or shadowing.
<!--SR:!2025-06-07,7,269-->


What is the subtyping rule for functions?
?
Function subtyping is:
- **Contravariant** in parameter type
- **Covariant** in return type
$$\frac{\tau_{1}' <: \tau_{1} \quad \tau_{2} <: \tau_{2}'}{\tau_{1} \rightarrow \tau_{2} <: \tau_{1}' \rightarrow \tau_{2}'}
$$
<!--SR:!2025-06-11,8,268-->


Why is function subtyping contravariant in parameter?
?
- To allow a function to accept **more general inputs** and remain type-safe. A function that expects **less specific input** (i.e., a **supertype**) can handle **more cases** than one that expects a specific subtype. If $\tau_1' <: \tau_1$, then any input of type $\tau_1$ is valid for a function expecting $\tau_1'$.
<!--SR:!2025-06-05,5,248-->

What is Liskov’s Substitution Principle?
?
If `S <: T`, then `T` can be replaced by `S` in any program **without affecting correctness** — often weakened to mean "without causing type errors".
<!--SR:!2025-06-05,5,249-->


What is the role of `Nothing` in Scala?
?
`Nothing` is the **bottom type**, a subtype of all types. It's used for expressions that do not return normally (e.g., `throw` ).
<!--SR:!2025-06-11,8,250-->


What is the Scala type hierarchy?
?
```
            Any
           /   \
     AnyVal   AnyRef
       |         |
     Int, ...   String, ...
                  |
                Null
                  |
               Nothing
```
<!--SR:!2025-06-08,5,230-->


What is the readers and writers principle?
?
Use:
- **Covariant types** for **read-only** data: `Reader[+T]`
- **Contravariant types** for **write-only** data: `Writer[-T]`
<!--SR:!2025-06-05,5,248-->


What is the difference between variance annotations and bounds?
?
- **Variance annotations (`+A`, `-A`)** apply at definition (declaration-site). Controls **subtyping relationship** of parameterized types. Propagates to all usages. Think “*How does `F[T]` behave for subtyping?*”
- **Bounds (`T <: A`, `T >: A`)** apply at usage (use-site). Constrains **what types** are allowed for `T`. Only affects one definition. Think: “*Which `T` values are allowed here?*”
<!--SR:!2025-06-05,5,248--> 


Why are **dynamic type checks** in MiniScala v8 performed **inside the class environment**?
?
Because with the introduction of subtyping and substitutability, our type hierarchy also depends class definitions, as we treat them as types. Meaning the dynamic execution of class declarations also must be taken in to account to allow for substitution with subtyping in the type checker.
<!--SR:!2025-06-05,5,248--> 


What is a fixed point of a function $f$?
?
A value $x$ such that $f(x) = x$.
<!--SR:!2025-06-07,7,268-->


What is a fixed-point combinator?
?
A higher-order function `fix` such that `fix(f)` is a fixed point of `f`, i.e., `fix(f) = f(fix(f))`. Applying the combinator produces a function that behaves like recursive version of $f$.
<!--SR:!2025-06-10,7,250-->


What is the difference between Call-by-Value and Call-by-Name?
?
- Call-by-value:
	- The **argument expression is evaluated first**, then the resulting value is passed to the function.
	- The argument is **only evaluated once**, regardless of how many times it's used inside the function.
	- Most modern languages (like Scala by default, Java, Python) use this strategy.
- Call-by-name
	- The **argument expression is not evaluated immediately**, but **each time it's used inside the function**, it is **re-evaluated**.
	- Useful for controlling **evaluation order**, or **avoiding unnecessary computation** (e.g., short-circuiting, laziness).
	- In Scala, you write it with a `=>` in the parameter type.
<!--SR:!2025-06-05,5,249-->

How does the definition of $type(\tau, \gamma)$ look at MiniScala v8?
?
- $type(\textcolor{blue}{\text{Int}}, γ) = Int$
- $type(\textcolor{blue}{\text{Boolean}}, γ) = Bool$
- $type(\textcolor{blue}{\text{Unit}}, γ) = Unit$
- $type(\textcolor{blue}{\text{(}}t_{1}, t_{2}\textcolor{blue}{\text{)}}, γ) = (type(t_{1}, γ), type(t_{2}, γ))$
- $type(t_{1} \textcolor{blue}{\text{=>}} t_{2}, γ) = type(t_{1}, γ) → type(t_{2}, γ)$
- $type(C, γ) = γ(C)$
<!--SR:!2025-06-05,5,248-->


How is the set $\mathsf{Type}$ defined in MiniScala v8?
?
These rules define the structure of valid types used in type checking, annotation interpretation, and class declarations. The set $\mathsf{Type}$ is inductively defined as follows:
- $\mathsf{Int} \in \mathsf{Type}$
- $\mathsf{Bool} \in \mathsf{Type}$
- $\mathsf{Unit} \in \mathsf{Type}$
- If $C$ is a class name, then $C \in \mathsf{Type}$ (interpreted via $\gamma(C)$ as a $\mathsf{StaticClassType}$)
- If $\tau_1, \tau_2 \in \mathsf{Type}$, then:
	- $(\tau_1, \tau_2) \in \mathsf{Type}$
	- $\tau_1 \rightarrow \tau_2 \in \mathsf{Type}$
- If $\tau \in \mathsf{Type}$, then:
	- $\mathsf{Mut}(\tau) \in \mathsf{Type}$
<!--SR:!2025-06-10,7,250-->

What is the difference between the set $\mathsf{Type}$ and the function $\mathsf{type}(\tau, \gamma)$ in MiniScala v8?
?
- $\mathsf{Type}$ is the **set of all valid types**, defined inductively (e.g., $\mathsf{Int}$, $\tau_1 \rightarrow \tau_2$, $\mathsf{Mut}(\tau)$, etc.).
- $\mathsf{type}(\tau, \gamma)$ is a **function that maps a syntactic type annotation** $\tau$ (like `C`, `t1 => t2`, etc.) into a semantic type in $\mathsf{Type}$, using the class type environment $\gamma$.
<!--SR:!2025-06-05,5,248-->

Why is it necessary to introduce $Mut(\tau)$ in MiniScala v6?
?
Using $Mut(\tau)$ is crucial for tracking **aliasing and side-effects** in the operational semantics.
<!--SR:!2025-06-08,5,228-->

What purpose does the $type$ function serve in the type checker?
?
It’s interpreting a **syntactic type annotation** into its **semantic type**, i.e. translating from the object language MiniScala, to the meta-language.
<!--SR:!2025-06-05,5,249-->

What is default behavior of overwriting in `Java` and `Scala`?
?
- **Java:** All methods are virtual by default, `@Override` is optional, `final` prevents overriding; `@Override` helps catch mistakes.
- **Scala:** Must explicitly write `override`. Helps avoid both accidental and missing overrides.
<!--SR:!2025-06-09,6,248-->


Is Generics and Parametric Polymorphism the same thing?::Yes
<!--SR:!2025-06-15,12,288-->


What is the correct answer? Convince yourself why this is true.
?
![[PR E Q.png]]
<!--SR:!2025-06-08,5,249-->


What does `sealed` do in Scala?
?
A `sealed` class or trait restricts subclassing to the **same file**, enabling the **compiler to check for exhaustiveness** in pattern matching.
- Typically used to define **algebraic data types**.
- Prevents extension outside its file for safety and exhaustiveness checking.
```scala
sealed trait Expr
case class Num(n: Int) extends Expr
case class Add(l: Expr, r: Expr) extends Expr

def eval(e: Expr): Int = e match {
  case Num(n)    => n
  case Add(l,r)  => eval(l) + eval(r)
}
```
> [!tip]
> You can omit the default `case _ =>` when all cases are covered thanks to `sealed`.
<!--SR:!2025-06-10,7,269-->

What does a `case class` provide in Scala?
?
A `case class` is a regular class with **built-in features**:
- **Pattern matching support**
- Automatically generated `equals`, `hashCode`, `toString`
- Public `val` fields
- An `apply` constructor — no need to write `new`
```scala
case class Point(x: Int, y: Int)

val p = Point(1, 2)          // No `new`
val Point(x, y) = p          // Pattern match
```
> [!info]
> Case classes are **immutable by default** and are ideal for defining data structures like ASTs.
<!--SR:!2025-06-08,5,249-->


How do `foldLeft` and `foldRight` differ?
?
```scala
def foldRight[A, B](xs: List[A], z: B, f: (A, B) => B): B = xs match {
  case Nil() => z
  case Cons(y, ys) => f(y, foldRight(ys, z, f))
}
```
- **Right-associative**: applies `f` from the end of the list toward the front.
- Not tail-recursive — builds up deferred operations (`f(y, ...)`).
- Equivalent to: `f(x1, f(x2, ... f(xn, z)...))`
```scala
def foldLeft[A, B](xs: List[A], z: B, f: (B, A) => B): B = xs match {
  case Nil() => z
  case Cons(y, ys) => foldLeft(ys, f(z, y), f)
}
```
- **Left-associative**: applies `f` from the start of the list to the end.
- Tail-recursive — more efficient for large lists.
- Equivalent to: `f(f(f(z, x1), x2), ..., xn)`
<!--SR:!2025-06-08,5,249-->

What is `StaticClassType` used for in MiniScala v8?
?
It is the type checker’s representation of class types, holding the source position, constructor type, and member types. It enables type checking of objects and method access.
<!--SR:!2025-06-06,3,252-->


What is `DynamicClassType` used for in MiniScala v8?
?
It is the runtime representation of a class’s identity, used inside `DynamicClassInstance`. It stores the source position to identify the class during method dispatch.
<!--SR:!2025-06-06,3,252-->


Why is `srcpos` (source position) used in class types in MiniScala?
?
To uniquely identify class declarations in a statically scoped language where class names may be shadowed. This allows correct typing and method resolution even if classes have the same name.
<!--SR:!2025-06-06,3,252-->

How is the `type` function applied on class names?
?
$type(C, γ) = γ(C)$ replaces class names by the corresponding class types, so the type checker resolves occurrences of `ClassNameType` to `StaticClassType` instances, much like the interpreter replaces occurrences of `ClassNameType` by `DynamicClassType` .
<!--SR:!2025-06-06,3,252--> 

What does `StaticClassType` contain?
?
```scala
case class StaticClassType(
  srcpos: Position,           // where the class was defined in the source code
  paramtype: Type,            // type of the constructor argument
  membertypes: TypeEnv        // member fields and method types
) extends Type
```
<!--SR:!2025-06-06,3,252-->


What is the difference between use-site variance and declaration-site variance in Scala?
?
- **Declaration-site variance** is specified when defining a generic class or trait:
    - `+A` means **covariant**: safe for reading (e.g., `List[+A]`)
    - `-A` means **contravariant**: safe for writing (e.g., `Function1[-A, +B]`)
    - No annotation = **invariant**
- **Use-site variance** is specified at the point of use using **wildcards**:
    - `_ <: A` means "any subtype of A" (covariant position)
    - `_ >: A` means "any supertype of A" (contravariant position)
<!--SR:!2025-06-06,3,252-->

**When should you use induction over derivations instead of structural induction?**
?
Use **induction over derivations** when proving properties about **operational semantics**, because evaluation does **not always follow the full structure** of the expression.
E.g., in `if true then e1 else e2`, only `e1` is evaluated — derivation-based induction allows reasoning just about that.
<!--SR:!2025-06-06,3,252-->