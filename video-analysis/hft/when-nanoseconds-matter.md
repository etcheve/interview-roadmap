### [When Nanoseconds Matter](https://www.youtube.com/watch?v=sX2nF1fW7kI)

**Summary:** Good, technical presentation. I may need to rewatch it later.

**Key Points:**
- Most of the time, you don’t want node-based containers
- Mechanical harmony: hardware in sync with software
- Kernel bypass
- Dispatch fan-out to processes on the same server:
  - Solarflare / OpenOnload / TCP Direct
- Layer 2 API interfaces:
  - EF_VI
  - DPDK
- Removing layers of complexity is key (Linux kernel networking, for example)
- Locally on a server, you do not need sockets — just use shared memory

**Added Comments / Mental Model:**
- Latency is an **end-to-end property**, not just a local optimization
- Every abstraction layer (kernel networking, sockets, allocators, containers) adds **jitter and variability**
- “Mechanical harmony” = aligning software design with actual hardware behavior: NICs, caches, NUMA, PCIe, memory
- Node-based containers and pointer-heavy structures fight the cache and the prefetcher
- On a single machine, sockets are often a historical artifact — shared memory + careful synchronization is strictly better
- Kernel bypass is not only about speed; it’s about **control and predictability**

**Pairs well with:**
- Cache coherence / NUMA knowledge
- Lock-free programming
- Zero-copy designs
- Single-writer, fan-out architectures

