___
#flashcards/ComArk/10_Concurrency

Why can even simple multithreaded programs behave incorrectly?
?
Because appearing simple operations like `++` are not atomic—they consist of multiple CPU instructions, which can interleave between threads without proper synchronization.
<!--SR:!2025-06-23,28,271-->

What is a race condition?
?
A race condition occurs when multiple threads access shared data concurrently and the final outcome depends on the non-deterministic timing of their execution.
<!--SR:!2025-06-23,23,230-->

What is mutual exclusion and how is it achieved?
?
Mutual exclusion ensures only one thread accesses a shared resource at a time, using mechanisms like mutexes, spinlocks, or monitors.
<!--SR:!2025-06-22,33,270-->

What is deadlock?
?
Deadlock occurs when threads are waiting on each other in a cycle, preventing all of them from proceeding.
<!--SR:!2025-06-30,41,290-->

What is starvation in concurrency?
?
Starvation happens when a thread is perpetually denied access to a resource, even though it's available, due to scheduling or priority.
<!--SR:!2025-08-23,68,270-->

What are atomic transactions in concurrency?
?
Atomic transactions are sequences of operations that execute as a single unit—either all succeed or all fail—ensuring consistency.
<!--SR:!2025-07-28,42,251-->

What does a recursive mutex allow?
?
It allows a thread to lock the same mutex multiple times, requiring it to unlock it an equal number of times to release it fully.
<!--SR:!2025-08-26,71,270-->

What is the role of LDREX and STREX in ARM?
?
LDREX marks a memory address for exclusive access; STREX attempts a write and succeeds only if no other processor has modified the address in the meantime.
<!--SR:!2025-06-28,12,230-->

Why are spinlocks used and when are they effective?
?
Spinlocks avoid thread sleep by busy-waiting. They are effective for short critical sections to reduce overhead, but may be inefficient if threads frequently wait for longer periods.
<!--SR:!2025-07-31,45,251-->

What is the bounded buffer problem?
?
A concurrency problem where producers and consumers share a fixed-size buffer. Producers wait when full; consumers wait when empty.
<!--SR:!2025-07-15,29,248-->

Why use condition variables in the bounded buffer problem?
?
They let threads wait for conditions (like space availability) to be signaled before proceeding, improving efficiency.
<!--SR:!2025-07-17,31,230-->

What is the main idea behind semaphore-based solutions to bounded buffers?
?
Semaphores manage counts for available buffer space and filled slots, synchronizing producer and consumer actions.
<!--SR:!2025-07-03,17,211-->

What is the readers-writers problem?
?
A concurrency issue where multiple readers can access data simultaneously, but writers require exclusive access.
<!--SR:!2025-07-04,45,290-->

What are the four necessary conditions for deadlock?
?
Mutual exclusion, hold and wait, no preemption, and circular wait.
<!--SR:!2025-07-16,30,230-->

How does the global order strategy prevent deadlocks?
?
By imposing a strict order on resource acquisition, eliminating cycles in the wait-for graph.
<!--SR:!2025-06-24,24,228-->

What is priority inversion?
?
When a high-priority thread waits on a low-priority thread due to resource locking, while medium-priority threads delay the low-priority thread.
<!--SR:!2025-08-10,54,250-->

What causes the convoy phenomenon?
?
A popular lock under FIFO scheduling causes threads to queue and context switch excessively, reducing performance.
<!--SR:!2025-06-18,2,168-->

What does the LOCK prefix do in x86?
?
It ensures atomic execution of instructions by asserting the LOCK# signal, preventing other cores from accessing the memory simultaneously.
<!--SR:!2025-06-27,10,231-->

How does the CMPXCHG instruction support atomic operations?
?
It atomically compares a register and memory value; if equal, it swaps in a new value, using the LOCK prefix for atomicity.
<!--SR:!2025-07-30,43,250-->

What is the ABA problem in non-blocking synchronization?
?
A pointer may change to a new value and back to the old value undetected, causing errors. Solved using version tags or counters.
<!--SR:!2025-06-30,13,210-->
