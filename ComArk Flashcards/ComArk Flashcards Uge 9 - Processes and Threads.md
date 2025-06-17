___
#flashcards/ComArk/9_Processes-and-Threads

What is the key difference between a process and a thread?
?
Processes are independent execution units with separate memory. Threads are units of execution within a process that share the same virtual memory space.
<!--SR:!2025-07-13,27,247-->

Why is thread communication easier than process communication?
?
Threads share the same memory space, allowing direct access to shared data, while processes are isolated and require interprocess communication mechanisms.
<!--SR:!2025-07-08,22,227-->

How does the OS manage multiple threads on a single-core CPU?
?
By rapidly switching between threads using context switches, giving the illusion of parallelism.
<!--SR:!2025-07-07,47,290-->

What is the purpose of the `fork()` system call in POSIX?
?
It creates a new process. In the parent, it returns the child's PID; in the child, it returns 0, allowing both to distinguish their roles.
<!--SR:!2025-07-19,33,247-->

What is POSIX and what relevance does it have for processes and threads?
?
**POSIX** is a standardized operating system interface that ensures portability by defining APIs for process control, threading, and system calls across UNIX-like systems.
<!--SR:!2025-07-16,30,246-->


What is a Thread Control Block (TCB)?
?
A TCB stores thread-specific information like ID, state, stack pointer, program counter, priority, and register value, allowing the OS to manage and resume threads.
<!--SR:!2025-06-30,14,210-->

What is a timer interrupt and why is it used?
?
A periodic hardware interrupt that forces context switching, ensuring all processes get CPU time and preventing monopolization.
<!--SR:!2025-06-19,19,267-->

What are the three states a thread can be in?
?
Runnable, running, or waiting.
<!--SR:!2025-07-15,29,247-->

What is priority scheduling?
?
A scheme where higher-priority threads run before lower-priority ones. Priorities can be fixed or dynamically adjusted.
<!--SR:!2025-08-09,54,250-->

What is a disadvantage of fixed priority scheduling?
?
Low-priority threads may suffer starvation if higher-priority ones never yield the CPU.
<!--SR:!2025-06-23,7,230-->

How does decay function scheduling address starvation?
?
It gradually reduces the priority of running threads and increases that of waiting threads, balancing fairness over time.
<!--SR:!2025-06-22,6,207-->

What is proportional-share scheduling?
?
Each process gets CPU time based on an assigned share, with examples including lottery and fair share scheduling.
<!--SR:!2025-06-19,24,250-->

How does lottery scheduling work?
?
Each thread gets a number of tickets according to a fixed priority; at each time slice, one ticket is drawn randomly to choose which thread runs.
<!--SR:!2025-07-12,26,230-->

What is round-robin scheduling?
?
Each thread gets a fixed time slice in rotation. Simple and fair, but doesn't account for priority or workload differences.
<!--SR:!2025-07-01,31,270-->

What is virtual runtime in Linux's CFS?
?
An abstract value representing how much CPU time a thread has received, adjusted by its weight, used to fairly distribute CPU time.
<!--SR:!2025-07-14,28,230-->

What are common concerns in scheduling on multicore systems?
?
Cache coherence, load balancing, and thread affinity (ensuring threads run on cores where their data is cached).
<!--SR:!2025-07-17,31,247-->

What is the main disadvantage of round-robin scheduling?
?
If the time slice is too short or there are too many threads, performance suffers due to frequent context switches.
<!--SR:!2025-07-11,25,227-->

Why does Linux's CFS prefer threads with a lower virtual runtime?
?
Because a lower vruntime indicates the thread has used less CPU time (adjusted by weight), maintaining fairness in scheduling.
<!--SR:!2025-07-21,35,230-->

What is the trade-off in load balancing on multicore systems?
?
Balancing thread load across cores may conflict with cache affinity, potentially harming performance.
<!--SR:!2025-07-05,19,210-->

What happens when a thread frequently switches cores?
?
It may lose cache locality, resulting in slower performance due to cache misses.
<!--SR:!2025-07-16,46,290-->

What is cache affinity in multicore scheduling?
?
Cache affinity is a scheduling strategy that aims to keep a thread running on the same core it previously used, so it can reuse data still in that core’s cache, thereby improving performance.
<!--SR:!2025-08-03,48,267-->
