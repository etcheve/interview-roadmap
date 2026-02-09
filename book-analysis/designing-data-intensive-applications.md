### Designing Data-Intensive Applications

**1) Data systems are about tradeoffs**  
There is no “best” database. Every system makes explicit tradeoffs between:  
- Consistency  
- Availability  
- Latency  
- Throughput  
- Durability  
- Operational complexity  

---

**2) Core goals: Reliability, Scalability, Maintainability**  
- **Reliability:** system continues to work correctly under faults  
- **Scalability:** performance remains acceptable as load grows  
- **Maintainability:** system can be evolved and operated over time  

---

**3) Data models matter**  
Different data models optimize for different access patterns:  
- **Relational (SQL):** strong consistency, joins, schemas  
- **Document:** flexible schema, locality  
- **Key-value:** simplicity, scalability  
- **Graph:** relationships as first-class citizens  

---

**4) Storage & retrieval internals**  
How databases actually work:  
- B-trees vs LSM-trees  
- Indexes and compaction  
- Write amplification  
- Read vs write optimization  

---

**5) Encoding & evolution**  
Data lives longer than code:  
- Schemas must evolve  
- Backward & forward compatibility  
- Encoding formats:
  - JSON (human-friendly)  
  - Avro / Protobuf (efficient, schema-based)  

---

**6) Replication**  
Replication improves:  
- Availability  
- Read scalability  
- Fault tolerance  

But introduces:  
- Replication lag  
- Conflicts  
- Consistency challenges  

---

**7) Partitioning (Sharding)**  
Required for scale:  
- Horizontal partitioning by key  
- Rebalancing cost  
- Hot keys  
- Cross-partition queries are hard  

---

**8) Transactions & consistency**  
Transactions in distributed systems become harder:  
- Isolation levels  
- Distributed transactions  
- Two-phase commit (2PC)  
- Global transactions don’t scale well  

---

**9) Consistency models**  
Strong consistency is expensive. Models include:  
- Linearizability  
- Eventual consistency  
- Causal consistency  
- Read-your-writes  

CAP theorem explained properly (not just a slogan)  

---

**10) Fault tolerance**  
Failures are normal. Covers:  
- Crash faults  
- Network partitions  
- Partial failures  
- Timeouts & retries  
- Idempotency  

---

**11) Stream processing & batch processing**  
Two processing styles:  
- **Batch:** large, offline jobs (MapReduce)  
- **Stream:** continuous processing (Kafka, Flink)  

---

**Additional Key Insights:**  
- Distributed systems fail in non-obvious ways  
- Latency matters more than throughput in user-facing systems  
- Simplicity beats cleverness  
- Observability and operability matter as much as correctness  

