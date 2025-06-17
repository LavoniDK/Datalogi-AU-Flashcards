___
#flashcards/ComArk/8_Virtual-Memory

## Introductiont to Operating Systems

Why are operating systems not considered intermediaries between hardware and applications?
?
Both OS and applications run directly on hardware. The OS differs by having special hardware support like privileged execution modes and access to system registers.
<!--SR:!2025-07-09,23,250-->

What are some examples of system registers used by an OS?
?
Examples include the flags register, exception vector (for handling exceptions), and page table root (for address translation).
<!--SR:!2025-07-14,28,230-->

## Virtual Memory

What is address translation in virtual memory?
?
It’s a technique where processes use virtual addresses, which are translated by hardware into physical addresses using a mapping function.
<!--SR:!2025-08-15,60,250-->

Why is address translation important in multi-process systems?
?
It isolates process memory spaces, preventing interference and simplifying memory management and protection.
<!--SR:!2025-07-07,21,250-->

How is address translation typically implemented in hardware?
?
Using page tables, often in a hierarchical structure, where virtual addresses are split into page groups and offsets for efficient lookup.
<!--SR:!2025-08-08,53,250-->

What is the copy-on-write optimization?
?
It shares pages between processes for reading. If a process writes to a shared page, it gets a private copy (on fault), preserving the original for others.
<!--SR:!2025-07-05,19,250-->

Why is copy-on-write efficient for process creation?
?
It avoids duplicating memory unnecessarily by sharing read-only data until a write actually occurs.
<!--SR:!2025-07-19,33,270-->

## Protection and System Calls

What is a system call in an operating system?
?
A system call is the interface through which a user-level process requests services from the OS kernel, such as file I/O or memory allocation.
<!--SR:!2025-06-22,6,210-->

What happens when a system call is made?
?
The process executes a special instruction (e.g., `syscall`), the CPU switches to kernel mode, the kernel validates the request, executes it, and returns the result.
<!--SR:!2025-07-19,33,243-->

Why are system calls important for protection?
?
They provide a controlled entry point into the kernel, allowing enforcement of security policies and preventing unauthorized hardware access.
<!--SR:!2025-07-04,18,263-->

What is the syscall_64.tbl file in Linux?
?
It’s a table that defines the available system calls for the x86-64 architecture in the Linux kernel.
<!--SR:!2025-06-24,8,223-->

What are common OS protection mechanisms?
?
Memory protection, privilege levels, file system ACLs, and CPU-level protections like timer interrupts and privileged instruction restrictions.
<!--SR:!2025-06-25,9,223-->

How do privilege levels support protection?
?
By separating user mode (restricted) from kernel mode (full access), preventing untrusted code from performing sensitive operations.
<!--SR:!2025-07-04,18,243-->

What is the relationship between system calls and protection?
?
System calls act as the gatekeepers to protected resources, ensuring that access only occurs through validated, controlled requests.
<!--SR:!2025-06-28,12,230-->
