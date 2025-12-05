---
name: simple-workflow
description: Direct execution workflow for simple tasks. No orchestration overhead, single agent execution.
complexity_level: 1
estimated_tokens: 500-2000
estimated_time: 2-5 minutes
---

# Simple Workflow

**Purpose**: Handle simple tasks with direct execution, no orchestration overhead.

**Complexity Level**: 1 (Simple Tasks)

**When to Use:**
- Single file modifications
- Simple refactoring (<100 lines)
- Bug fixes in isolated code
- Documentation updates
- Configuration changes

## Workflow Process

```
User Request
    ↓
Task Complexity Analyzer
    ↓
[Simple Task Detected]
    ↓
Direct to Specialist Agent
    ↓
Result
```

## Execution Steps

### Step 1: Task Analysis (Automatic)
- Complexity analyzer identifies simple task
- Routes directly to appropriate specialist

### Step 2: Direct Execution
- Specialist agent executes task
- No coordination needed
- Minimal context required

### Step 3: Result Delivery
- Task completed
- Changes documented
- Result returned to user

## Agent Selection

**Common Specialists:**
- `typescript-pro` - TypeScript/JavaScript changes
- `python-pro` - Python changes
- `golang-pro` - Go changes
- `backend-developer` - Backend changes
- `frontend-developer` - Frontend changes
- `documentation-expert` - Documentation updates

## Example Execution

**Request:** "Fix typo in UserService.ts line 42"

**Execution:**
1. Complexity analyzer: Simple task detected
2. Route to: `typescript-pro`
3. Execute: Fix typo
4. Result: Typo fixed, file updated

**Time:** 2 minutes
**Tokens:** 800 tokens

## Output Format

```markdown
## Task Execution

**Task:** [Task description]
**Agent:** [Specialist name]
**Status:** ✅ Complete
**Time:** [X] minutes
**Tokens:** [X] tokens

**Changes:**
- [File]: [Change description]

**Result:** [Brief summary]
```

## Optimization

- **No orchestration overhead**
- **Minimal token usage**
- **Fast execution**
- **Direct specialist access**
