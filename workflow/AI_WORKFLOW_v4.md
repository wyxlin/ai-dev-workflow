# AI Workflow (Main Document v4)

## 1. Objective
Enforce structured control over AI-driven development to ensure:
- No scope drift
- Traceability
- Reviewability
- Support for multi-AI collaboration
- Recoverability (via snapshots)
- Long-term stability

## 2. Documentation System
docs/
- product/PRD.md (what to build)
- domain/RUBRIC.md (business rules + engineering standards)
- architecture/ARCHITECTURE.md (system structure)
- architecture/SCHEMA.md (data model)
- ai/PROMPTS.md (AI behavior)
- workflow/ (this process)

## 3. Document Priority
PRD > RUBRIC > ARCHITECTURE > SCHEMA > PROMPTS > CODE

Rules:
- Lower layers MUST NOT modify higher layers
- Conflicts MUST be escalated to design-level decisions

## 4. Roles
- Human: decisions and approvals
- Developer AI: implement, update, handoff
- Reviewer AI: independent audit

## 5. Collaboration Principles
- Stateless execution (each run relies ONLY on current code + documents, not chat history)
- Reviewer MUST run in a new window (preferably a different model)
- All communication MUST follow PROTOCOL.md

## 6. Context Management
Start a new window when:
- Module is completed
- Context becomes too long
- After multiple review rounds

Forced interruption:
- Token usage > 60%
- Repeated error loop >= 2

## 7. SNAPSHOT Lifecycle Rules
- SNAPSHOT.md MUST overwrite previous content (no append)
- Only ONE valid snapshot at any time
- PROJECT_PROGRESS.md MUST record:
  - Snapshot reference (commit ID or timestamp)

Purpose:
- Ensure single source of truth
- Prevent stale state usage by Reviewer

## 8. Core Principles
Small modules + strict constraints + doc alignment + review gate + snapshot-based recovery
