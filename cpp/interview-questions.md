# C++ Interview Questions

A collection of typical C++ interview questions with concise answers.

---

### 1. What is Encapsulation?  
Bundling data and methods inside a class and restricting direct access using access specifiers (`private`, `protected`, `public`).  

### 2. What is Abstraction?  
Exposing only what the user needs and hiding implementation details, typically via interfaces or abstract classes.  

### 3. What is Inheritance?  
A class derives from another class, inheriting its data and behavior, enabling code reuse and polymorphism.  

### 4. What is Polymorphism?  
Treat objects of different derived types through a base class interface. Runtime behavior varies via virtual functions.  

### 5. What is a Virtual Function?  
A member function that supports **dynamic dispatch** — call resolved at runtime based on the actual object type.  

### 6. What is an Interface in C++?  
A class containing only pure virtual functions and no data members; defines a contract.  

### 7. What is a Constructor?  
Special member function called automatically when an object is created; used to initialize the object.  

### 8. What is a Destructor?  
Special member function called automatically when an object is destroyed; used to release resources.  

### 9. What is RAII?  
**Resource Acquisition Is Initialization:** resources are tied to object lifetime — allocate in constructor, release in destructor.  

### 10. Difference between `struct` and `class`  
Identical except default access:  
- `struct` → public  
- `class` → private  

### 11. What is const correctness?  
Mark objects, functions, and parameters as `const` when they should not modify state, enabling safer code and optimization.  

### 12. What is a Reference?  
Alias to another object; must be initialized and cannot be reseated.  

### 13. What is a Pointer?  
Holds the address of an object; can be reassigned or null.  

### 14. What is the Rule of 5?  
If a class manages resources, explicitly define:  
- Destructor  
- Copy constructor  
- Copy assignment  
- Move constructor  
- Move assignment  

### 15. What is Undefined Behavior?  
Behavior not defined by the C++ standard; program may crash, misbehave, or appear to work.  

### 16. What is a vtable?  
Compiler-generated table of function pointers for dynamic dispatch of virtual functions. Each polymorphic object contains a hidden pointer to its class vtable.  

### 17. What is NUMA?  
**Non-Uniform Memory Access:** each CPU socket has local memory; accessing remote memory is slower, affecting latency and scalability.  

### 18. What is Kernel bypass?  
Applications access hardware (NICs) directly, avoiding the kernel networking stack to reduce latency/CPU overhead (DPDK, RDMA, netmap).  

### 19. What is Zero-copy (0-copy)?  
Transfer data without copying between memory buffers; reduces CPU usage and latency.  

### 20. What is Lock-free?  
At least one thread always makes progress in finite steps, avoiding mutexes; relies on atomic operations like CAS.  

### 21. What is a Socket?  
Endpoint for bidirectional communication between processes (network or local); abstracts transport details.  

### 22. What is False sharing?  
Independent variables in the same cache line cause unnecessary cache invalidations and performance issues.  

### 23. What is a Mutex?  
Provides mutual exclusion; only one thread accesses a shared resource at a time.  

### 24. What is Atomic?  
Lock-free, thread-safe operations on single variables; requires correct memory ordering.  
```cpp
std::atomic<int> counter{0};
counter.fetch_add(1, std::memory_order_relaxed);

### 25. What is Perfect Forwarding?
Preserves value category (lvalue/rvalue) and const-qualification when passing arguments through templates.
template<typename T>
void f(T&& x) { g(std::forward<T>(x)); }

### 26. What is Move Semantics?
Transfers resources from temporary or expiring objects instead of copying, improving performance and enabling efficient ownership transfer.

### 27. What is the difference between deep copy and shallow copy?
- Shallow copy: copies pointers or references, not the actual resources → shared ownership
- Deep copy: duplicates the entire object and its resources → independent ownership

### 28. What is a Lambda in C++?
Anonymous function object; can capture variables from the enclosing scope. Used for short, inline functions.
auto add = [](int a, int b){ return a + b; };

### 29. What is a Smart Pointer?
Object that manages dynamic memory automatically, preventing leaks.
- unique_ptr → sole ownership
- shared_ptr → shared ownership with reference counting
- weak_ptr → non-owning reference to shared_ptr

### 30. What is the difference between std::vector and std::list?
- std::vector → contiguous memory, fast random access, slow insert/delete in middle
- std::list → doubly-linked, fast insert/delete anywhere, slow random access

### 31. What is the difference between const, constexpr, and consteval?
- const → value cannot change after initialization
- constexpr → can be evaluated at compile-time; may also be runtime
- consteval → must be evaluated at compile-time

### 32. What is the Rule of Three / Five / Zero?
- Rule of Three: if you define destructor, copy constructor, copy assignment → define all three
- Rule of Five: includes move constructor and move assignment for resource-managing classes
- Rule of Zero: use RAII types and smart pointers; avoid custom resource management

### 33. What is SFINAE?
Substitution Failure Is Not An Error — template instantiation failure doesn’t trigger compilation error immediately; allows conditional compilation.

### 34. What is the difference between std::mutex and std::shared_mutex?
- std::mutex → exclusive lock for one thread at a time
- std::shared_mutex → allows multiple readers or one writer



