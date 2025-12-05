---
name: standard-workflow
description: Focused team coordination workflow for medium tasks. Lightweight orchestration with 2-4 agents.
complexity_level: 2
estimated_tokens: 3000-8000
estimated_time: 10-25 minutes
---

# Standard Workflow

**Purpose**: Handle medium tasks with focused team coordination, streamlined workflow.

**Complexity Level**: 2 (Medium Tasks)

**When to Use:**
- New features in existing modules
- Module refactoring
- Integration between 2-3 components
- Requires planning but not architecture
- Needs testing but not full QA pipeline

## Workflow Process

```
User Request
    ↓
Task Complexity Analyzer
    ↓
[Medium Task Detected]
    ↓
Team Formation (2-4 agents)
    ↓
Sequential/Parallel Execution
    ↓
Result
```

## Execution Steps

### Step 1: Task Analysis
- Complexity analyzer identifies medium task
- Determines required specialists

### Step 2: Team Formation
- Select 2-4 appropriate agents
- Define execution order
- Identify parallel opportunities

### Step 3: Execution
- Agents execute in sequence or parallel
- Coordination as needed
- Progress tracking

### Step 4: Result Compilation
- Combine agent outputs
- Validate completeness
- Deliver result

## Typical Team Compositions

### Backend Feature
- `backend-architect` - API design and implementation
- `test-automator` - Test creation

### Frontend Feature
- `frontend-developer` - UI implementation
- `test-automator` - Test creation

### Full-Stack Feature
- `backend-architect` - Backend implementation
- `frontend-developer` - Frontend implementation
- `test-automator` - Test creation

### Integration Task
- `backend-architect` - Backend integration
- `frontend-developer` - Frontend integration
- `test-automator` - Integration tests
- `api-documenter` - API documentation

## Example Execution

**Request:** "Add user profile editing feature"

**Execution:**
1. Complexity analyzer: Medium task detected
2. Team formation: `backend-architect`, `frontend-developer`, `test-automator`
3. Execution:
   - `backend-architect`: Design and implement API endpoints
   - `frontend-developer`: Create UI components
   - `test-automator`: Write tests
4. Result: Complete feature with tests

**Time:** 15 minutes
**Tokens:** 5000 tokens

## Output Format

```markdown
## Team Execution

**Task:** [Task description]
**Team:** [agent-1, agent-2, agent-3]
**Status:** ✅ Complete
**Time:** [X] minutes
**Tokens:** [X] tokens

**Execution Flow:**
1. **[agent-1]**: [What was done]
2. **[agent-2]**: [What was done]
3. **[agent-3]**: [What was done]

**Deliverables:**
- [List of deliverables]

**Result:** [Summary]
```

## Optimization

- **Focused team size** (2-4 agents)
- **Efficient coordination**
- **Parallel execution when possible**
- **Streamlined workflow**
