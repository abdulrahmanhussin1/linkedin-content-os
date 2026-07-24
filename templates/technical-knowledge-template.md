---
name: Technical Knowledge Template
version: 1.0.0
parser_directives:
  required_fields: [definition, benefits, drawbacks]
  format: markdown
  nesting_level: H3
---

# 📚 Technical Knowledge Documentation Template

> **Parser Instruction**: This template catalogs backend engineering concepts, architectures, and design patterns. AI agents should parse the code blocks (Laravel, Go, SQL) and the Decision Matrix to generate high-signal educational content.

---

## 🏷️ [Technical Topic Name]

### 📖 Definition
`[Provide a clear, simple, yet technically accurate definition of the concept. Avoid hand-wavy descriptions. E.g., CQRS (Command Query Responsibility Segregation) is an architectural pattern that separates read and update operations for a data store.]`

---

### 🚦 Decision Matrix

#### When to Use
* `[Scenario 1: e.g., When the application's read volume is significantly higher than its write volume.]`
* `[Scenario 2: e.g., When business rules for writes are complex, but reads only require simple denormalized views.]`

#### When NOT to Use
* `[Scenario 1: e.g., Simple CRUD applications where data schemas are identical for both reading and writing.]`
* `[Scenario 2: e.g., When real-time read consistency immediately following a write is a strict requirement (unless using synchronous replication).]`

---

### ⚖️ Trade-offs

#### Benefits
* `[Benefit 1: e.g., Independent scaling of read and write resources.]`
* `[Benefit 2: e.g., Optimized data schemas for reads (flat, denormalized) and writes (normalized, domain-driven).]`

#### Drawbacks
* `[Drawback 1: e.g., Increased code complexity and maintenance overhead.]`
* `[Drawback 2: e.g., Eventual consistency challenges (read lag).]`

---

### 💻 Code & Implementation Examples

#### 1. Laravel Example
```php
// Show a clean Laravel implementation of the concept (e.g., Command handling or separate DB connections)
```

#### 2. Go Example
```go
// Show the Go equivalent demonstrating concurrency, struct design, or interface implementation
```

#### 3. Database Example
```sql
-- Show schema structures, migration snippets, index strategies, or SQL queries representing the concept
```

---

### 🔍 Architectural Attributes

* **Performance**: `[How does this impact query latency, CPU, and memory utilization? E.g., offloads index scans off write tables.]`
* **Security**: `[What security implications does this pattern present? E.g., read-only users can be locked down to the read database replica.]`
* **Scalability**: `[How does it scale vertically and horizontally? E.g., multiple read replicas can be added dynamically.]`
* **Clean Code**: `[How does this help keep codebases DRY, SOLID, and decoupled?]`
* **Architecture Impact**: `[How does this affect modular boundaries, domain decoupling, or monolith-to-microservice migration pathways?]`

---

### 🤝 Best Practices & Common Pitfalls

#### Best Practices
* `[Best Practice 1: e.g., Always use transaction boundaries inside commands.]`
* `[Best Practice 2: e.g., Keep queries completely free of write side logic.]`

#### Common Mistakes
* `[Mistake 1: e.g., Trying to reuse the write entity model in read views, defeating the segregation pattern.]`
* `[Mistake 2: e.g., Prematurely implementing separate databases for reads/writes instead of starting with separate code paths on a single DB.]`

---

### 🗣️ Interview Prep: Questions & Answers
* **Q**: `[e.g., How do you handle eventual consistency in a CQRS system?]`
  * **A**: `[e.g., By using event handlers that update the read database asynchronously, combined with UI optimistic updates or polling.]`
* **Q**: `[Question 2]`
  * **A**: `[Answer 2]`

---

### 📚 References & Resources
* `[Link to authoritative documentation, academic papers, books, or articles]`

---

### 💡 Personal Opinion & Hot Take
`[Write your perspective on this technology or pattern. E.g., "Most developers use CQRS because they think they have a scaling issue, when in reality they just have bad database indexes. Don't add two databases until your single database is actually crying."]`

---

## 🎨 Reusable Content Ideas

### 📝 Post Ideas (LinkedIn & Threads)
1. **The "Frustrated Developer" Hook**:
   > *"Stop splitting your databases just because you read a blog post about microservices. Here is why separate database schemas on a single MySQL instance is actually all you need..."*
2. **The Code Comparison**:
   > *"Laravel Service classes are great. But Command classes are better. Let's compare how they handle business transactions side-by-side..."*
