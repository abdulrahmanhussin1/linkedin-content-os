---
name: Project Documentation Template
version: 1.0.0
parser_directives:
  required_fields: [role, context, status, stack]
  format: markdown
  nesting_level: H3
---

# 🚀 Software Project Documentation Template (Personal Branding Edition)

> **Parser Instruction**: This template is designed to extract deep technical details, architectural decisions, and human-centric developer stories from projects. AI agents should parse headers (`H3`) as independent data objects.

---

## 📂 [Project Name]

### 📌 Project Metadata
* **Role**: `[e.g., Solo Developer / Lead Backend Engineer]`
* **Context**: `[e.g., Personal Project / Client Work / SaaS MVP]`
* **Production Status**: `[e.g., Live / Active Development / Archive]`
* **Stack**: `[e.g., Laravel, React, MySQL, Docker, Vercel]`
* **Links**: `[Code repo, Live App]`

---

### 📖 Overview
`[Provide a high-level summary of what the system does. E.g., A multi-tenant ERP platform built to automate retail POS, warehouse movements, and treasury workflows for Egypt-based SMEs.]`

---

### ❓ The Problem & Business Context
* **The Problem**: `[What user pain or operational inefficiency triggered this project? E.g., SME owners in Egypt lost 5% of inventory yearly to spreadsheet synchronization delay.]`
* **Business Impact**: `[Why does solving this matter financially or operationally? How does it save money or generate revenue?]`

---

### 🏗️ Architecture & System Design
* **Design Philosophy**: `[e.g., Why a Modular Monolith over microservices?]`
* **Key Patterns**: `[e.g., API-first design, DTO mapping, Service layers, Action classes]`
* **Diagram/Text Representation**:
  ```text
  [Request] -> [Controller] -> [FormRequest Validation] -> [DTO] -> [Action/Service] -> [Eloquent ORM] -> [Database]
  ```

---

### 🗄️ Database & Schema Design
* **Database Choice**: `[e.g., MySQL for ACID transactions, Redis for fast queue management]`
* **Critical Tables / Relations**: `[Describe the primary schema constraints, e.g., self-referencing warehouse hierarchy table, poly-morphic sales invoices]`
* **Tenant Isolation**: `[e.g., single-database multi-tenancy using tenant_id global scopes vs. multi-database isolation]`

---

### ⚠️ Challenges & Technical Hardships
* `[Describe a major technical roadblock. E.g., handling inventory race conditions when two sales orders reserve the last product stock simultaneously.]`

---

### 🐛 Interesting Bugs & The Debugging Journey
* **The Symptoms**: `[e.g., "Queues were hanging indefinitely in staging and silently crashing under heavy payload..."]`
* **The Investigation**: `[How did you track it down? Horizon dashboard, query logging, Docker system resource inspection?]`
* **The Root Cause**: `[e.g., Circular object graph serialization inside the Job constructor.]`
* **The Fix**: `[Show the resolution (using ID references instead of complete models in jobs).]`

---

### ⚖️ Hard Decisions & Trade-offs
* **The Dilemma**: `[e.g., Deciding whether to build custom permission logic or pull in Spatie Laravel Permission package.]`
* **The Choice**: `[e.g., Built a lightweight custom RBAC logic to minimize package dependencies and optimize performance.]`
* **The Cost**: `[What was sacrificed? E.g., Spent 3 extra days developing UI controls.]`

---

### ♻️ Refactoring Stories
* **Before**: `[Show a code snippet or architecture layout that was messy, slow, or hard to read.]`
* **The Trigger**: `[What forced you to refactor? E.g., Adding a new product module broke inventory balance calculations.]`
* **After**: `[Show the clean code or structure.]`
* **The Lesson**: `[Why is the new way objectively better?]`

---

### ⚡ Optimization & Scaling
* **The Bottleneck**: `[e.g., Calculating stock reports across multiple warehouses was causing N+1 query loops.]`
* **The Intervention**: `[e.g., Replaced Eloquent relationships with eager loading and a single subquery selection using Query Builder.]`
* **The Metrics**: `[e.g., Database queries reduced from 140 to 2; page load dropped from 4s to 120ms.]`

---

### 🔒 Security Implementations
* `[e.g., Token-based API authentication with Laravel Sanctum, strict input sterilization, and granular RBAC policies protecting sensitive financial endpoints.]`

---

### 🚀 Deployment & Infrastructure
* **Hosting**: `[e.g., Deployed to Hetzner Cloud VPS managed with a Docker Compose script.]`
* **CI/CD Pipeline**: `[e.g., GitHub Action running test suites, building docker images, and deploying to Vercel/VPS.]`

---

### 🎓 Lessons & Mistakes
* **The Mistake**: `[e.g., Storing currency values as floats instead of integers (cents) in the POS module.]`
* **The Lesson**: `[e.g., Always use integers or the Decimal type when writing financial software.]`

---

### 📊 Project Metrics & Outcomes
* **Lines of Code / Files**: `[e.g., 12 custom modules, 45 REST endpoints]`
* **Database Scale**: `[e.g., 34 tables with strict FK constraints]`
* **User Metric**: `[e.g., Handles up to X operations/sec without dropping connections]`

---

### 📸 Screenshots & Media
* `[Placeholder: Path to architecture flowcharts, UI screenshots, or Performance benchmarks]`

---

### 💻 Code Examples (Social-Ready Snippets)
```php
// Code snippet showing the DTO pattern or Action class structure
```

---

## 🎨 Social Media Content Pipeline

### 📝 Reusable Stories
* *The "2 AM Debugging" Story*: `[Summarize the bug story in 3 paragraphs: Hook, Conflict, Resolution]`
* *The Founder-Developer Shift*: `[How launching a food brand changed your view on POS software validation]`

### 🛠️ Technical Post Ideas (LinkedIn / Threads)
1. **The "How We Did It" Outline**:
   > *"How I built a multi-warehouse inventory tracker in Laravel. Schema, code, and why we avoided N+1 query loops..."*
2. **The "Code Comparison" (Before vs. After)**:
   > *"Stop writing raw Eloquent queries for calculations. Use subqueries instead. Here is a real example from our ERP platform..."*

### 💭 Opinion Post Ideas (Monolith vs. Microservices, etc.)
* *"Microservices are a organizational solution, not a technical one. If you have a small team, a Modular Monolith is your superpower..."*
* *"You don't need a massive AWS bill for your MVP. A simple $5 VPS with Docker Compose will get you further than you think."*

### 👶 Beginner Lessons
* *"Always use Database Transactions when updating related tables (e.g., Sales Order and Stock count)."*

### 👴 Senior Lessons
* *"Architecture is about deferring decisions until you have enough data. Keep the code decoupled so decisions can be changed later."*

---

## 🔮 Future Improvements & Roadmap
- [ ] Add vector storage for localized product descriptions.
- [ ] Implement event-driven internal webhooks.
