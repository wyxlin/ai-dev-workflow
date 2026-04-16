# AI Collaboration Protocol v4

## 1. Developer → Reviewer Input Format

Review Input:
- Module:
- Scope:
- Non-Scope:
- Files Changed:
- Diff:
- Key Logic Summary:
- Related Docs:

---

## 2. Reviewer Output Format (MANDATORY)

Findings:

[Severity: Critical / Major / Minor / Note]
- File:
- Issue:
- Reason:

---

Scope Status:
- In Scope / Out of Scope

Drift Detected:
- Yes / No

---

Verdict:
- PASS
- MINOR_FIX
- BLOCKING_ISSUE

---

## 3. Verdict Action Rules

PASS:
- Proceed to next module

MINOR_FIX:
- Developer MUST fix in current window
- No full re-review required
- MUST update PROJECT_PROGRESS.md

BLOCKING_ISSUE:
- Developer MUST:
  1. Stop current implementation
  2. Return to Step 1 (re-design)
- Full re-review REQUIRED after fix

---

## 4. SNAPSHOT Format

- Implemented Features
- Open Bugs
- Current State
- Current Module
- Next Action

---

## 5. PROJECT_PROGRESS Format

- Current Module
- Status
- Completed Work
- Known Issues
- Context Status
- Next Step

---

## 6. SCHEMA SNAPSHOT

- Entities
- Key Fields
- Constraints

---

## 7. Communication Rules

- MUST use structured output
- No free-form responses
- No missing fields
