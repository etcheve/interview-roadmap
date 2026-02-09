### The Art of Multiprocessor Programming

**Summary:**  
The book explains how to design correct and scalable concurrent algorithms using atomic primitives, memory models, and non-blocking techniques. It emphasizes correctness properties like linearizability and progress guarantees, while exposing the fundamental limits of synchronization.

---

**1) Concurrency is about correctness first, performance second**  
- Parallel programs are non-deterministic; most bugs are about ordering, not logic  
- Goal: define correctness before optimizing

---

**2) Shared memory & atomicity**  
- Threads communicate via shared memory; reads/writes can interleave  
- Atomic operations are the foundation  
- Hardware primitives:
  - CAS (compare-and-swap)  
  - LL/SC (load-linked/store-conditional)

---

**3) Consistency models matter**  
- Sequential consistency is intuitive but slow  
- Modern CPUs reorder aggressively  
- Programmers must use:
  - Memory fences  
  - Atomics with ordering

---

**4) Locks are simple but expensive**  
- Classic locks: Mutex, Spinlock, Reader-writer lock  
- Problems: Contention, Deadlock, Priority inversion, Convoying

---

**5) Lock-free and wait-free algorithms**  
- **Lock-free:** some thread always makes progress  
- **Wait-free:** every thread makes progress in bounded steps  
- Benefits: Avoid deadlocks, better scalability, resilience to thread suspension  
- Costs: Hard to design, subtle bugs, memory reclamation complexity

---

**6) Consensus and impossibility results**  
- Consensus number of an object determines its power  
- Examples:
  - Atomic read/write → consensus number 1  
  - CAS → consensus number ∞  
- Explains why CAS is fundamental

---

**7) Non-blocking data structures**  
- Builds: lock-free stacks, queues, concurrent sets, skip lists  
- Focus: Linearizability, progress guarantees, correct memory ordering

---

**8) Memory reclamation is hard**  
- Big problem: when can memory be safely freed?  
- Techniques:
  - Hazard pointers  
  - Epoch-based reclamation  
  - Reference counting (problematic)  
- Key insight: GC simplifies concurrency but impacts performance

---

**9) Testing concurrent code is brutal**  
- Bugs are rare and timing-dependent  
- Stress testing > unit testing  
- Formal reasoning matters  
- Tools: Model checking, linearizability proofs

---

**Core Philosophy**  
- Concurrency is precise, not “hard”  
- Locks are a convenience, not a solution  
- Correctness requires mathematical thinking  
- Performance comes after correctness

