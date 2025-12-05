---
name: smart-dev
description: Intelligent development command that automatically analyzes task complexity and selects optimal workflow. For simple tasks uses direct agent calls, for complex tasks uses full multi-phase pipeline with quality gates.
---

# Smart Dev Command

**Usage**: `/smart-dev <task description>`

**Description**: Intelligently analyzes task complexity and selects optimal workflow. Automatically minimizes token usage for simple tasks while providing full power for complex ones.

## How It Works

1. **Task Analysis**: Analyzes task complexity (1-10 scale)
2. **Workflow Selection**: Selects optimal workflow (simple/medium/complex/enterprise)
3. **Agent Team Assembly**: Forms minimal effective team
4. **Execution**: Executes workflow with appropriate gates
5. **Result**: Returns complete solution

## Examples

### Simple Task
```
/smart-dev Fix typo in login form validation message

→ Complexity: 2 (Simple)
→ Workflow: Direct call
→ Agent: frontend-developer
→ Result: Fixed typo
→ Tokens: 8K
→ Time: 2 minutes
```

### Medium Task
```
/smart-dev Add user profile picture upload feature

→ Complexity: 6 (Medium)
→ Workflow: Planning → Execution → Review
→ Agents: task-planner, backend-developer, frontend-developer, code-reviewer
→ Result: Complete feature with tests
→ Tokens: 65K
→ Time: 12 minutes
```

### Complex Task
```
/smart-dev Implement microservices architecture for user management

→ Complexity: 9 (Complex)
→ Workflow: Full pipeline with gates
→ Agents: requirements-analyzer, backend-architect, backend-developer,
          test-automator, code-reviewer, spec-validator
→ Result: Complete microservices implementation
→ Tokens: 250K
→ Time: 35 minutes
```

### Enterprise Task
```
/smart-dev Build new e-commerce platform

→ Complexity: 10 (Enterprise)
→ Workflow: Multi-phase iterative
→ Agents: Full team (11 agents)
→ Result: Enterprise-grade platform
→ Tokens: 800K
→ Time: 60 minutes
```

## Benefits

- ✅ **Automatic Optimization**: Right workflow for each task
- ✅ **Token Efficiency**: Minimizes tokens for simple tasks
- ✅ **Quality Assurance**: Full quality gates for complex tasks
- ✅ **No Over-Engineering**: Simple tasks stay simple
- ✅ **No Under-Engineering**: Complex tasks get full power
