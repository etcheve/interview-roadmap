### [When a Microsecond Is an Eternity](https://www.youtube.com/watch?v=NH1Tta7purM)

**Summary:** Excellent HFT video that acts like a checklist for performance pitfalls and optimizations.  

**Key Points:**
- Super useful website to inspect assembly: [Godbolt](https://godbolt.org/)
- Branch / path prediction matters
- Reuse objects wherever possible
- Avoid system calls entirely in hot paths
- Google Benchmark for measuring performance
- Hash tables: chaining vs open addressing
- `inline` is only a hint — it does not guarantee faster code
- Warm up hot paths and keep them hot
- Profile-guided optimization (PGO) may produce uneven performance; measure carefully
- **Measurements are critical**: `gprof`, `callgrind` (instruction-level simulator)
- `likely` / `unlikely` are not silver bullets — design code correctly first

**Added Comments / Key Takeaways:**
- Microsecond-level performance is about **avoiding surprises**
- Branch mispredictions, cache misses, memory allocation, and syscalls dominate costs
- Don’t optimize by guessing — **measure, inspect assembly, and verify**
- The fastest code is usually the **simplest code** that stays on the hot path and avoids touching the kernel or unnecessary memory

