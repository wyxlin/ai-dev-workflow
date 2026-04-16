# Developer Workflow v4

## Step 0: Load Context
Read:
- AI_WORKFLOW.md
- MODULE_PLAN.md
- PROJECT_PROGRESS.md
- PRD / RUBRIC / ARCHITECTURE / SCHEMA

## Step 0.5: SCHEMA SNAPSHOT (MANDATORY)
Output:
- Entities
- Key fields
- Constraints

## Step 1: Select Module
Define:
- Goal
- Scope
- Non-scope
- Dependent docs

## Step 2: Parallelization Check
Determine if multi-agent execution is possible

## Step 3: Implement
Rules:
- Only implement current module
- Do NOT expand scope
- Do NOT modify design documents

Output:
- Code changes
- Explanation (what / why / risks)

## Step 4: Update Progress (MANDATORY)
Update PROJECT_PROGRESS.md:
- Module status
- Known issues
- Context status

## Step 5: Prepare Review Input
Follow PROTOCOL.md format

## Step 6: SNAPSHOT + Context Cleanup (ENHANCED)

Before generating SNAPSHOT.md:

1. Persistence Check:
- All logic MUST be written to code files
- No critical logic may exist only in chat

2. Redundancy Cleanup:
- Remove outdated reasoning
- Ensure system state is fully represented in code + docs

3. Generate SNAPSHOT.md:
- Implemented features
- Open bugs
- Current state
- Next action
