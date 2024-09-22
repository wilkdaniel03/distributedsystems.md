# Processes

Multiple processes are commonly used in distributed computing because they allow performant communication.
Processes are often created from multiple threads.

Operating system creates virtual CPU for different processes and keeps track of them by process table.
These are completely separated - they **cannot** affect each other.

Threads are lightweigtht alternative to processes. They only store minimum amount of information about CPU context - no separation involved.

IPC(inter-process communication) is common way of communication between different processes but it requires huge amount of context switching.
Using threads allow us to avoid context switching because threads use shared memory, but we have to take care of separation ourselves.
Another way is using hybrid threads - scheduling threads through scheduler in kernel space.
