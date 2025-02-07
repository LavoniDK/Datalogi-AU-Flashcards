___
#flashcards/ComArk/Uge2 

## C Programming


**What is a value in C programming?**::A representation of data stored in an object that can be manipulated via expressions.
<!--SR:!2025-02-08,3,255-->

**What does the address-of operator (`&`) do?**::Retrieves the memory address of a variable's object.
<!--SR:!2025-02-08,3,262-->

**What does the indirection operator (`*`) do?**::Dereferences a pointer, accessing the object it points to.
<!--SR:!2025-02-08,4,279-->

**What is the difference between `int *p` and `*p` in C?**::`int *p` declares a pointer, while `*p` dereferences it.
<!--SR:!2025-02-08,4,276-->

**How do you declare a pointer in C?**::`type *ptr;` declares a pointer to a variable of type `type`
<!--SR:!2025-02-08,4,279-->

**What does `*ptr` do in C?**::Dereferences the pointer, accessing the value it points to.
<!--SR:!2025-02-08,4,277-->

**What is pointer arithmetic?**::Operations like `ptr + 1`, which move the pointer to the next memory block of the type, they are performed in terms of the size of the data type the pointer points to.
<!--SR:!2025-02-08,4,279-->

**What is a NULL pointer?**::A pointer that does not point to a valid object (e.g., `NULL` or `(void*)0`).
<!--SR:!2025-02-08,4,275-->

**What is a dangling pointer?**::A pointer that refers to memory that has been freed or gone out of scope.
<!--SR:!2025-02-19,12,278-->

**What is automatic storage?**::Local variables allocated on the stack and destroyed at block exit.
<!--SR:!2025-02-14,7,256-->

**An object is a region of storage that holds ==values==, and its ==type== determines its valid operations and memory layout.**
<!--SR:!2025-02-08,4,275!2025-02-08,4,270-->

**The heap is used for ==dynamically allocated== memory, managed via `malloc()` and `free()`.**
<!--SR:!2025-02-08,4,272-->

**An enum in C starts with a default value of ==0== and increments by ==1== unless explicitly assigned.**
<!--SR:!2025-02-08,4,276!2025-02-08,4,278-->

**What is an lvalue in C?**::An expression that refers to a memory location and can appear on the left-hand side (LHS) of an assignment.
<!--SR:!2025-02-11,4,282-->

**What is an rvalue in C?**::An expression that does not have a memory location and can only appear on the right-hand side (RHS) of an assignment.
<!--SR:!2025-02-11,4,286-->

**What is a void pointer in C?**::A generic pointer type that can point to any data type.
<!--SR:!2025-02-11,4,282-->

**Why must a void pointer be cast before use?**::Because it does not have a predefined type, so arithmetic operations are not allowed directly.
<!--SR:!2025-02-11,4,286-->

**What should always be checked after calling `malloc()`?**::If the returned pointer is `NULL` to verify successful allocation.
<!--SR:!2025-02-11,4,286-->