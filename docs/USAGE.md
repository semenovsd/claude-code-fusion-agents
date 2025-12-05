# Usage Guide

Complete guide for using the Hybrid Subagents System.

## Basic Usage

### Using Smart Dev Command

The `/smart-dev` command automatically analyzes task complexity and selects optimal workflow:

```
/smart-dev <task description>
```

### Examples

#### Simple Task
```
/smart-dev Fix typo in login form validation message
```
- **Complexity**: 2 (Simple)
- **Workflow**: Direct call
- **Agent**: frontend-developer
- **Result**: Quick fix, minimal tokens

#### Medium Task
```
/smart-dev Add user profile picture upload feature
```
- **Complexity**: 6 (Medium)
- **Workflow**: Planning → Execution → Review
- **Agents**: task-planner, backend-developer, frontend-developer, code-reviewer
- **Result**: Complete feature with tests

#### Complex Task
```
/smart-dev Implement microservices architecture for user management
```
- **Complexity**: 9 (Complex)
- **Workflow**: Full pipeline with gates
- **Agents**: Full team (5-7 agents)
- **Result**: Complete implementation with quality gates

#### Enterprise Task
```
/smart-dev Build new e-commerce platform
```
- **Complexity**: 10 (Enterprise)
- **Workflow**: Multi-phase iterative
- **Agents**: Full team + specialists (7+ agents)
- **Result**: Enterprise-grade solution

## Manual Agent Selection

If you need to use specific agents manually:

### Planning Agents

```markdown
Use requirements-analyzer to analyze requirements for user authentication system
```

```markdown
Use task-planner to create task breakdown for user profile feature
```

### Development Agents

```markdown
Use backend-architect to design microservices architecture for user management
```

```markdown
Use backend-developer to implement user authentication API
```

```markdown
Use frontend-developer to create user profile component
```

### Quality Agents

```markdown
Use code-reviewer to review user authentication implementation
```

```markdown
Use test-automator to write tests for user service
```

```markdown
Use security-auditor to audit user authentication security
```

## Workflow Patterns

### Simple Workflow

For simple tasks, use direct agent calls:

```markdown
Use backend-developer to fix bug in user service
```

### Medium Workflow

For medium tasks, follow planning → execution → review:

1. **Planning**: Use task-planner
2. **Execution**: Use specialist agents
3. **Review**: Use code-reviewer

### Complex Workflow

For complex tasks, use full pipeline:

1. **Planning Phase**:
   - requirements-analyzer
   - backend-architect / frontend-architect
   - Quality Gate 1

2. **Development Phase**:
   - backend-developer / frontend-developer
   - test-automator
   - Quality Gate 2

3. **Validation Phase**:
   - code-reviewer
   - spec-validator
   - Quality Gate 3

### Enterprise Workflow

For enterprise tasks, use multi-phase iterative:

1. **Iteration 1 - Planning**:
   - requirements-analyzer
   - business-analyst
   - architects
   - Quality Gate 1

2. **Iteration 2 - Development**:
   - developers
   - test-automator
   - Quality Gate 2

3. **Iteration 3 - Optimization**:
   - security-auditor
   - performance-engineer
   - Quality Gate 3

4. **Iteration 4 - Validation**:
   - code-reviewer
   - spec-reviewer
   - spec-validator
   - Quality Gate 4

## Best Practices

### 1. Let the System Decide

Don't manually select workflows. Let Smart Orchestrator analyze and choose:

✅ **Good**: `/smart-dev Add user profile feature`
❌ **Bad**: Manually calling all agents for simple task

### 2. Trust Complexity Analysis

The system accurately assesses complexity. Trust its judgment:

✅ **Good**: Accept complexity score and workflow selection
❌ **Bad**: Override complexity for simple tasks

### 3. Use Quality Gates

Quality gates ensure quality without over-engineering:

✅ **Good**: Let gates run for complex tasks
❌ **Bad**: Skip gates for complex tasks

### 4. Monitor Metrics

Track tokens, time, and quality scores:

- Simple tasks: 5K-20K tokens, 1-5 minutes
- Medium tasks: 30K-80K tokens, 5-15 minutes
- Complex tasks: 100K-300K tokens, 15-45 minutes
- Enterprise tasks: 300K-1M+ tokens, 45+ minutes

### 5. Iterate When Needed

Enterprise tasks allow iterative refinement:

- If gate fails, fix issues and re-run
- Don't skip iterations
- Learn from gate feedback

## Common Patterns

### Backend Development

```markdown
/smart-dev Implement REST API for user management with PostgreSQL
```

### Frontend Development

```markdown
/smart-dev Create user profile page with React and TypeScript
```

### Full-Stack Development

```markdown
/smart-dev Build user authentication system with JWT
```

### Refactoring

```markdown
/smart-dev Refactor user service to use microservices architecture
```

### Bug Fixes

```markdown
/smart-dev Fix memory leak in user service
```

## Troubleshooting

### Task Too Simple

If system selects complex workflow for simple task:
- Check task description clarity
- Verify complexity analysis output
- Consider manual agent selection

### Task Too Complex

If system selects simple workflow for complex task:
- Break down into smaller tasks
- Use multiple `/smart-dev` calls
- Consider manual workflow selection

### Quality Gate Fails

If quality gate fails:
- Review gate feedback
- Fix identified issues
- Re-run gate
- Don't skip gates

## Advanced Usage

### Custom Workflows

Create custom workflows by combining agents:

```markdown
1. Use requirements-analyzer to analyze requirements
2. Use backend-architect to design architecture
3. Use backend-developer to implement
4. Use test-automator to write tests
5. Use code-reviewer to review
```

### Parallel Execution

Some agents can run in parallel:

- Planning: requirements-analyzer + architects
- Development: backend-developer + frontend-developer
- Validation: code-reviewer + spec-validator (sequential)

### Context Sharing

Agents share context through documentation:

- Requirements doc → Architects → Developers
- Architecture doc → Developers → Testers
- Implementation → Reviewers → Validators

## Next Steps

- Review [ARCHITECTURE.md](ARCHITECTURE.md) for architecture details
- Check [BEST_PRACTICES.md](BEST_PRACTICES.md) for best practices
- See [SETUP.md](SETUP.md) for setup instructions
