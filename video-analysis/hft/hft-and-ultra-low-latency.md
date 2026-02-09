### [High Frequency Trading and Ultra Low Latency Development Techniques](https://www.youtube.com/watch?v=_0aU8S-hFQI)

**Summary:** Focused on removing variability and ensuring predictable latency in HFT systems.  

**Key Points:**
- End-to-end kernel bypass — system calls are too slow
- Avoid context switching, queuing, and data transfer between threads
- Deterministic static code flow: make as many decisions as possible at compile time
- Minimize cache misses and branch mispredictions
- Use custom-tailored data structures for specific use cases
- Fast code must be fast **all the time**, not just on average
- Avoid long chains of `if (error) return;` — create fewer, more predictable paths
- CRTP (Curiously Recurring Template Pattern) can be useful but adds complexity
- Improve branch prediction:
  - Map with static values evaluable at compile time
  - Compile-time configuration with templates instead of runtime flags
  - Rearrange statements to evaluate predictable values first
  - `constexpr` everything possible
- Cache misses are often the **highest overhead** in low-latency code
- The critical path often occurs in **1% of cases** (e.g., actual order submission)
- Lock-free and zero-copy are important (though not discussed in detail here)
- Compiler flags: `-march`, `-mtune`
- Premature optimization and micro-optimization have costs and risks

**Added Comments / Mental Model:**
- Goal is **predictable latency**, not just speed
- Kernel bypass, static control flow, and compile-time decisions reduce runtime uncertainty
- Most techniques trade **maintainability and flexibility** for determinism and speed — acceptable only in narrow hot paths
- Must **measure and isolate** hot paths — applying blindly is dangerous

