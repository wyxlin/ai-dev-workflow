# AI Dev Workflow

A structured workflow and protocol for reliable AI-driven software development.

This project defines a stateless, multi-agent development system that makes AI-assisted coding more controllable, auditable, and reproducible.

---

## 🚀 Why This Exists

AI coding is powerful, but unstable.

Common problems:
- Context drift (AI forgets what was actually implemented)
- Hidden assumptions (logic exists in chat, not in code)
- Inconsistent reviews (different models give different judgments)
- Lack of reproducibility

This workflow solves these by enforcing:

- Stateless execution
- Structured communication
- Independent review
- Explicit system state tracking

---

## 🧠 Core Concepts

### 1. Stateless Execution
AI must NOT rely on chat history.

All decisions must be based on:
- Code (repo)
- Documents (PRD, SCHEMA, etc.)
- Snapshot / Progress files

---

### 2. Multi-Agent Collaboration
The system separates responsibilities:

- Developer AI → implements code
- Reviewer AI → independently audits code
- Human → final decision maker

Reviewer must run in a separate context/window.

---

### 3. Snapshot-Based Recovery
Each module produces a system snapshot:

SNAPSHOT.md

This allows:
- Context reset
- Multi-window continuation
- Reliable state recovery

---

### 4. Strict Review Gate
Every change must pass structured review:

PASS → continue  
MINOR_FIX → fix locally  
BLOCKING_ISSUE → redesign + re-review  

---

## 📂 Project Structure

docs/ 
├── product/ 
│   └── PRD.md

├── domain/
│   └── RUBRIC.md

├── architecture/
│   ├── ARCHITECTURE.md
│   └── SCHEMA.md

├── ai/
│   └── PROMPTS.md

├── workflow/
│   ├── AI_WORKFLOW.md
│   ├── DEV_WORKFLOW.md
│   ├── REVIEW_WORKFLOW.md
│   └── PROTOCOL.md

---

## ⚙️ How It Works

### Step 1 — Define System
Create:
- PRD (what to build)
- RUBRIC (rules)
- ARCHITECTURE (structure)
- SCHEMA (data model)

---

### Step 2 — Plan Modules
Define execution order in:

MODULE_PLAN.md

---

### Step 3 — Developer Execution
Developer AI:

- Loads context (documents)
- Outputs SCHEMA snapshot
- Implements ONE module
- Updates progress
- Generates snapshot

---

### Step 4 — Independent Review
Reviewer AI:

- Runs in a new window
- Reads code + documents
- Outputs structured findings + verdict

---

### Step 5 — Resolution
Based on verdict:

- PASS → next module
- MINOR_FIX → fix locally
- BLOCKING → redesign + re-review

---

## 🔒 Key Rules

- Never trust chat memory
- Always trust documents + code
- Always generate SNAPSHOT
- Always update PROJECT_PROGRESS
- Reviewer must be independent

---

## 📌 When to Reset Context

Start a new window when:

- A module is completed
- Context becomes long (>60%)
- Multiple review iterations occurred

---

## 🧩 What Makes This Different

This is NOT a prompt collection.

This is a control system for AI development:

- Defines behavior
- Enforces consistency
- Prevents drift
- Enables reproducibility

---

## 🧪 Who This Is For

- Engineers using AI for coding
- Teams experimenting with multi-agent workflows
- Builders who want deterministic AI behavior

---

## 🛠️ Status

Experimental but practical.

Designed to be:
- Minimal
- Strict
- Extensible

---

## 📎 License

MIT (recommended)
