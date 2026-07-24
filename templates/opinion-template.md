---
name: Personal Opinions Template
version: 1.0.0
parser_directives:
  required_fields: [topic, consensus, contrarian_view]
  format: markdown
  nesting_level: H4
---

# 💡 Personal Opinions & Perspectives Template

> **Parser Instruction**: This template extracts contrarian opinions and technical beliefs. AI agents should use the "Creative Framing" voice iterations to tailor posts for different target audience segments.

---

## 🏷️ [Opinion Topic]

### 🔍 The Core Stance

#### Topic
`[e.g., Microservices vs. Modular Monoliths for SME software]`

#### Current Industry Opinion (The Consensus)
`[What is the mainstream belief? E.g., "To build scale, you must break everything into microservices from day one so separate teams can own independent services."]`

#### My Opinion (The Contrarian View)
`[What do you actually believe? E.g., "For 95% of businesses—especially SMEs in Egypt—microservices are an expensive disaster that slows down feature delivery and introduces severe network latency."]`

---

### 🛡️ Arguments & Grounding

#### Why (Logical Reasoning)
`[Explain the rationale. E.g., "Microservices introduce a distributed network barrier. In a monolith, a transaction rollback handles database inconsistencies instantly. In microservices, you need complex patterns like Saga or two-phase commits to ensure data integrity."]`

#### Evidence (Data / Facts)
`[e.g., Studies or public company examples (like Prime Video moving back to monoliths) proving costs decreased.]`

#### Experience (Personal Proof)
`[e.g., "When designing the POS/ERP platforms, keeping inventory and sales modules in a single modular monolith database allowed us to run instant atomic updates rather than managing API handshakes."]`

#### Counter Arguments
* **Counter Argument**: `[e.g., "But what if the database becomes a bottleneck?"]`
* **Your Response**: `[e.g., "Use proper indexing, cache reads with Redis, and scale vertically first. A single MySQL instance can handle millions of requests a day if designed right."]`

---

### 📖 Anecdotes & Pitfalls

#### Mistakes (What happens if people don't follow this opinion?)
`[e.g., "A startup built 12 microservices for an ERP MVP, spent $4,000/month on AWS bills, and spent 3 months debugging why customer profiles weren't syncing with checkout cards."]`

#### Real-world Examples
`[e.g., Compare two projects: Project A (clean modular monolith) vs Project B (bloated distributed setup).]`

#### Stories
`[e.g., "That time a colleague suggested we spin up a new service just to handle email notifications, and we ended up with a simple Laravel Queue Job that took 5 minutes to write instead."]`

#### Future Prediction
`[e.g., "The industry will swing back. We will see a major renaissance of monolithic frameworks (like Rails, Laravel, and Go templates) as cloud hosting costs rise and teams shrink."]`

---

## 🎨 Creative Framing (Voice Iterations)

### 🔥 The Hot Take Version (Spicy, provocative)
> *"If your startup has less than 20 developers and you're using microservices, you aren't engineering. You're just paying an AWS tax to sound smart."*

### 👔 The Professional Version (Structured, corporate, objective)
> *"While microservices offer organizational decoupling for enterprise teams, they introduce significant network overhead. For early-stage and SME products, a well-structured modular monolith provides superior velocity and simpler transaction management."*

### 👶 The Beginner Version (Simple, educational)
> *"Don't worry about breaking your app into separate servers. Keep all your code in one project, structure it cleanly, and make sure your database queries are fast. That's more than enough to handle your first 10,000 customers."*

### 👴 The Senior Version (Philosophical, trade-off oriented)
> *"Architecture isn't about choosing the 'coolest' stack; it's about minimizing the cost of change. A monolith lets you refactor interfaces in seconds. Microservices force you to modify network contracts across separate codebases. Choose accordingly."*

---

## 📢 Content Distribution Formats

### ✍️ LinkedIn Post Draft
`[Draft a hook-to-CTA post utilizing the core opinion. Focus on a narrative flow.]`

### 🎥 YouTube Script Outline
* **Hook**: `[Hook]`
* **The Myth**: `[Industry consensus explanation]`
* **The Reality**: `[Your counterpoint]`
* **The Code/Proof**: `[Examples]`
* **Outro/CTA**: `[CTA]`

### 📨 Newsletter Blueprint
* **Subject line**: `[Subject]`
* **Deep-dive**: `[Detailed essay layout with subheadings]`

---

### ❓ FAQ: Questions People Might Ask
* **Q**: *Doesn't a monolith make it harder for multiple developers to work together?*
  * **A**: *No. A Modular Monolith uses distinct directory structures (domains/modules). Git conflicts are minimal if domain boundaries are clear.*
