### Operating Systems – Three Easy Pieces

**1) Virtualization**  
The OS virtualizes hardware resources to give each program the illusion it owns the machine.

- **CPU virtualization**
  - Time sharing: many processes on one CPU
  - Context switches save/restore registers
  - Scheduling policies decide who runs next
- **Memory virtualization**
  - Each process has its own virtual address space
  - Address translation via page tables
  - Protection and isolation between processes
- **I/O virtualization**
  - Uniform interfaces (files, sockets, devices)
  - Asynchronous I/O and interrupts

**Key idea:** illusion of dedicated resources.

---

**2) Concurrency**  
The OS must manage multiple threads executing at the same time, safely and efficiently.

- Threads share address space; processes don’t
- Race conditions occur due to interleavings
- Critical sections must be protected
- **Synchronization primitives:**
  - Locks (mutex)
  - Condition variables
  - Semaphores
- **Common problems:**
  - Deadlock
  - Starvation
  - Priority inversion

**Key idea:** control interleavings to ensure correctness.

---

**3) Persistence**  
The OS must store data reliably despite crashes.

- **Files and directories**
  - Names → inodes → data blocks
- Disks are slow and unreliable
- **Techniques for reliability:**
  - Write-Ahead Logging (WAL)
  - Journaling
  - Copy-on-write
- **Crash consistency:** system must recover to a valid state
- **RAID:** redundancy for fault tolerance and performance

**Key idea:** make storage fast, durable, and consistent.

