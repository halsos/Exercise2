# Mutex and Channel basics

### What is an atomic operation?
> An atomic operation is in concurrent programming operations that run independent from processes. As example, when the processor perform add or sub operation there are values loaded from or stored to memory. The processor cannot perform another write/read before the atomic operation is finished.

### What is a semaphore?
> A semmaphore is a variable used as a conditional to access a certain piece of data. Example: if bool A is a semaphore to Q, then when A is true then Q is accessable. When A is not true then Q is not accessible.

### What is a mutex?
> Mutual exclusive: Where multiple threads can access a resource (a memory location) a mutex-function makes sure that only one thread is allowed to access the resource at a time.

### What is the difference between a mutex and a binary semaphore?
> Binary semaphore: Different processes can wait() and Signal() a semaphore. Mutexes give ownership to a thread of a resoure. Only this thread can lock and unlock the resource as long as it has the ownership.

### What is a critical section?
> The part of a program that accesses shared resources. Only in a critical section can a process disrupt another process. Race conditions can be avoided by making sure that two processes are not in a critical section at the same time.

### What is the difference between race conditions and data races?
 > A race condition is when the timing or ordering of a program affects the correctness of the result. A data race is when there are two memory accesses within the a program and both target the same address location.

### List some advantages of using message passing over lock-based synchronization primitives.
> Shared objects are not easily accessed by multiple threads at a time. Message passing will lead to algorithms that are wait-free and lock-free. Avoid the shared-object problem of multiple processor cores duplicate the value in its cache. A system built of Message passing semantics is inherently more scalable. Since message passing implies that messages are sent asynchronously, the sender is not required to block until the receiver acts on the message.

### List some advantages of using lock-based synchronization primitives over message passing.
> The algoritms for lock-based synchronization primitives tend to be simpler than for message passing.
A message passing system that requires resources to be locked will eventually degenerate into a shared object systems.
If algorithms are wait-free, you will see improved performance and reduced memory footprint as there is much less object allocation in the form of new messages.
