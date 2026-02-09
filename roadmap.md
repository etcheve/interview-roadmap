# Roadmap

This roadmap reflects how I organize and revisit topics when preparing for **software engineering roles in the financial sector**, with a primary focus on **C++ and systems-level development**.

The emphasis is on **correctness, performance, latency, and failure modes** — concerns that are especially relevant in finance (trading systems, market data, risk engines, and low-latency infrastructure).

The list is intentionally **non-exhaustive** and unordered by difficulty. Topics are revisited iteratively depending on the role (low-latency, backend, infrastructure, or quantitative systems).

---

## Linux / OS fundamentals
- Processes vs threads  
- Virtual memory, paging  
- File descriptors and syscalls  
- Scheduling  
- `epoll` / `select` / `poll`  
- Page cache and buffer cache  
- Namespaces and cgroups  
- NUMA basics  
- Tooling: `strace`, `ltrace`, `perf`, `htop`  

---

## Networking
- TCP vs UDP  
- Congestion control  
- Nagle algorithm, delayed ACK  
- Latency vs throughput trade-offs  
- TLS basics  
- HTTP/1.1 vs HTTP/2 vs HTTP/3  
- DNS  
- Load-balancing strategies  

---

## C++ (systems-level focus)
- C++ memory model  
- RAII and lifetime management  
- Const correctness  
- Move semantics and perfect forwarding  
- Templates and type traits  
- Threads, mutexes, atomics  
- Lock-free and wait-free basics  
- False sharing and cache-line awareness  
- NUMA-aware programming  
- Kernel bypass concepts (DPDK, `io_uring`, etc.)  

---

## Concurrency & performance
- Memory ordering and visibility  
- Synchronization primitives  
- Contention and scalability limits  
- CPU caches and cache coherence  
- Profiling and performance analysis  

---

## Databases & storage
- Indexing (B-tree, LSM)  
- Query planning and execution  
- Transactions  
- Isolation levels  
- Write-ahead logging (WAL)  
- Replication  
- Sharding and partitioning  

---

## Caching systems
- CPU cache vs page cache  
- Cache invalidation strategies  
- Write-through vs write-back  
- Consistency models  

---

## Messaging & distributed systems
- Kafka architecture  
- Partitions and consumer groups  
- Ordering guarantees  
- Exactly-once semantics  
- Backpressure and flow control  
- Rebalancing  
- Failure modes  

---

## Distributed systems theory
- CAP theorem  
- Consistency models  
- Paxos / Raft basics  
- Vector clocks  
- Idempotency  

---

## Containers & infrastructure
- Namespaces and cgroups (container perspective)  
- OverlayFS  
- Container networking  
- Orchestration basics  

---

## Observability & production
- Logging  
- Metrics  
- Tracing  
- Debugging production incidents  
- SLOs and SLAs  

---

## Security basics
- TLS  
- Certificates  
- Authentication vs authorization  
- OAuth  
- Secrets management  

---

## Engineering workflow
- Git fundamentals  
- Rebase vs merge  
- Rewriting history  
- Conflict resolution  
- `git bisect`  
- Git internals (objects, refs, packfiles)  

---

## Finance domain
- Financial instruments: futures, options, swaps  
- Greeks  
- Market microstructure  
- Order books  
- Latency constraints in trading systems  
- Risk, margin, and correctness requirements  

---

This roadmap is used as a personal reference and evolves over time as understanding deepens and interview expectations change.

