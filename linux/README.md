# Linux / OS Fundamentals

This section contains a summary of key Linux and OS concepts, commands, and tools relevant for software development and technical interviews.  
It focuses on processes, threads, memory, caching, namespaces, containers, I/O, networking, and performance tools.

---

## Table of Contents
1. [Processes vs Threads](#processes-vs-threads)
2. [Virtual Memory & Paging](#virtual-memory--paging)
3. [File Descriptors](#file-descriptors)
4. [Syscalls](#syscalls)
5. [Scheduling](#scheduling)
6. [I/O Multiplexing](#io-multiplexing)
7. [Performance Tools](#performance-tools)
8. [Namespaces & Containers](#namespaces--containers)
9. [Page & CPU Caches](#page--cpu-caches)
10. [Process / System Commands](#process--system-commands)
11. [Files / I/O / Disks](#files--io--disks)
12. [Networking](#networking)
13. [Build / Debug Tools](#build--debug-tools)

---

## Processes vs Threads
- **Process:** isolated execution with its own address space, file table, resources. IPC needed to communicate. Expensive context switches. Crash does not kill others.  
- **Thread:** lightweight unit inside a process, shares memory and file descriptors. Cheaper context switches. Crash kills whole process.  

---

## Virtual Memory & Paging
- Virtual memory provides each process a large, contiguous address space.  
- Memory is split into pages (4 KB typical, huge pages 2 MB / 1 GB).  
- Virtual → physical translation via **page tables**.  
- **TLB** caches recent translations. Page faults trigger loading from disk.  
- Only active pages remain in RAM; inactive pages swapped out.  

---

## File Descriptors
- Integer handles representing open resources (files, sockets, pipes, devices).  
- Stored in per-process file table pointing to kernel objects.  
- Standard: `0 = stdin`, `1 = stdout`, `2 = stderr`.  
- Shared between threads, inherited across `fork()`.

---

## Syscalls
- Controlled transition from user space → kernel space.  
- Examples: `read`, `write`, `open`, `close`, `fork`, `exec`, `mmap`, `socket`.  
- Expensive due to context switch and privilege change.  

---

## Scheduling
- Kernel decides which thread runs where and for how long.  
- Linux uses **CFS (Completely Fair Scheduler)**.  
- Threads have priorities & **vruntime**; smallest picked next.  
- Preemption allows high-priority tasks to interrupt low-priority ones.  
- NUMA-aware scheduling & CPU affinity.

---

## I/O Multiplexing
- **select / poll / epoll**: wait for I/O readiness.  
- `select` → fixed limit, linear scan.  
- `poll` → no fd limit, linear scan.  
- `epoll` → O(1), event-driven, edge/level-triggered.  

---

## Performance Tools
- `strace` → syscall tracing  
- `ltrace` → library call tracing  
- `perf` → CPU profiling, cache misses, branches  
- `htop` → interactive process/thread monitoring  

---

## Namespaces & Containers
- Namespaces isolate resources: PID, NET, MOUNT, IPC, UTS, USER, TIME.  
- **cgroups** limit CPU, memory, I/O, PIDs, network.  
- `clone()` → new process in new namespaces  
- `unshare()` → move process to new namespaces  
- `setns()` → join existing namespace  
- Docker/Containerd workflow: clone → UID/GID mapping → mounts/network → exec program  

---

## Page & CPU Caches
- **Page cache:** file data in RAM → reduce disk I/O  
- **CPU cache:** L1/L2/L3 levels, cache lines (~64 bytes), false sharing is harmful  
- **TLB:** caches virtual→physical mapping, huge pages reduce misses  

---

## Process / System Commands
- `ps`, `top`, `htop`, `uptime`, `watch`, `time`, `kill`, `pkill`, `taskset`, `strace`, `perf`, `vmstat`, `iostat`, `free`, `dmesg`  

---

## Files / I/O / Disks
- `mount / umount`, `df`, `du`, `stat`, `lsof`, `fuser`, `sync`, `file`, `ldd`  

---

## Networking
- `ss`, `ip`, `tc`, `ping`, `traceroute`, `nc`, `curl`, `wget`, `tcpdump`  

---

## Build / Debug Tools
- `nm`, `objdump`, `readelf`, `strings`, `addr2line`, `gdb`  

---


