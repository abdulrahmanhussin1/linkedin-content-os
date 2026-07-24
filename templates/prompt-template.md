---
name: Agent Prompt Template
version: 1.0.0
target_llm: Claude/ChatGPT/Manus
description: Reusable template to structure system instructions and agent tasks.
---

# 🤖 Agent Prompt: [Agent Name / Role]

> **Purpose**: [Brief 1-2 sentence description of what this prompt instructs the agent to do]

---

## 🎭 Role & Context
* **Persona**: [e.g., Senior Database Administrator / Expert LinkedIn Content Writer]
* **Target Tone**: [e.g., Pragmatic, technical, objective, dry humor]
* **Core Skillsets**:
  * [Skill 1]
  * [Skill 2]

---

## 🎯 Objectives & Tasks
Provide a numbered list of instructions the agent must perform:
1. **Analyze Input**: [e.g., Read the raw story from `knowledge/stories/`]
2. **Retrieve Context**: [e.g., Cross-reference technical guidelines in `knowledge/technical/`]
3. **Generate Output**: [e.g., Format the result as standard Markdown in `posts/02-drafts/`]

---

## 🛡️ Rules & Constraints
Clear boundaries the agent **must not** cross:
* **Constraint 1**: [e.g., Do NOT invent experience. Only use facts in `who-am-i.md`]
* **Constraint 2**: [e.g., Never use buzzwords like "delve", "testament", or "revolutionary"]
* **Constraint 3**: [e.g., Output markdown only—no conversational introductory or concluding text]

---

## 📥 Input Requirements
* **Context Files Needed**: [e.g., `prompts/writing-style.md`, `knowledge/profile/who-am-i.md`]
* **Expected Input Format**: [e.g., Raw project brief or transcript file]

---

## 📤 Output Structure
Detailed breakdown of the expected response structure:
```markdown
# Title
[Core Content]

## Reusable Stories
[Narrative]

## Key Takeaway
[One liner]
```

---

## 📝 Few-Shot Examples

### Example 1: Input
```text
[Raw input example]
```
### Example 1: Output
```markdown
[Expected output example]
```
