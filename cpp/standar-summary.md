# C++ Standards Summary

A quick reference of major C++ standards and their key features.

---

### C++98 / C++03
- Core language: classes, inheritance, templates, exceptions, namespaces, STL  
- RAII and deterministic destructors  
- Manual memory management dominant  
- No threading model, no move semantics, no lambdas  

---

### C++11
- Move semantics and rvalue references  
- Smart pointers: `unique_ptr`, `shared_ptr`, `weak_ptr`  
- Thread library, mutexes, atomics, memory model  
- Lambdas  
- `auto`, `nullptr`, `constexpr`  
- Range-based `for` loops  
- `std::chrono`  
- Variadic templates  
- Deprecated: `auto_ptr`  

---

### C++14
- Generic lambdas  
- Relaxed `constexpr` rules  
- `std::make_unique`  

---

### C++17
- Structured bindings  
- `if constexpr`  
- `std::optional`, `std::variant`, `std::any`  
- `std::string_view`  
- Parallel algorithms  
- `std::filesystem`  
- Removed `auto_ptr`  

---

### C++20
- Concepts for template constraints  
- Ranges library  
- Coroutines  
- Modules  
- `std::span`  
- `std::format`  
- Widespread `constexpr` support  

---

### C++23
- `std::expected`  
- Better ranges and views  
- More `constexpr` in the standard library  
- Multidimensional `operator[]`  
- Library cleanups and performance improvements  

