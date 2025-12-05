# Best Practices

Best practices for using the Hybrid Subagents System effectively.

## General Principles

### 1. Trust the System

The Smart Orchestrator is designed to make optimal decisions. Trust its complexity analysis and workflow selection:

✅ **Good**: Let system analyze and select workflow
❌ **Bad**: Manually override complexity for simple tasks

### 2. Right Tool for Right Job

Match workflow complexity to task complexity:

✅ **Good**: Simple task → Simple workflow
✅ **Good**: Complex task → Complex workflow
❌ **Bad**: Simple task → Complex workflow (waste tokens)
❌ **Bad**: Complex task → Simple workflow (compromise quality)

### 3. Quality When Needed

Quality gates ensure quality without over-engineering:

✅ **Good**: Gates for complex+ tasks
❌ **Bad**: Gates for simple tasks (unnecessary overhead)

## Task Description Best Practices

### Be Clear and Specific

✅ **Good**: "Add user profile picture upload with validation and error handling"
❌ **Bad**: "Add picture upload"

### Include Context

✅ **Good**: "Implement REST API for user management using FastAPI and PostgreSQL"
❌ **Bad**: "Make user API"

### Specify Requirements

✅ **Good**: "Create user authentication with JWT, refresh tokens, and password reset"
❌ **Bad**: "Add login"

## Workflow Selection

### Simple Tasks (1-3)

Use for:
- Bug fixes
- Simple refactoring
- Trivial updates
- Single file changes

Don't use for:
- New features
- Architecture changes
- Multiple file changes

### Medium Tasks (4-6)

Use for:
- New features
- Module refactoring
- API integrations
- Component enhancements

Don't use for:
- New services
- Architecture changes
- System-wide changes

### Complex Tasks (7-9)

Use for:
- New services/APIs
- Major refactoring
- Architecture changes
- Full-stack features

Don't use for:
- New systems
- Enterprise features
- Large-scale migrations

### Enterprise Tasks (10)

Use for:
- New systems
- Architecture overhaul
- Large-scale migrations
- Enterprise features

## Agent Usage

### Planning Agents

**Requirements Analyzer**:
- Use for complex+ tasks
- Provides deep requirement analysis
- Creates user stories

**Task Planner**:
- Use for medium+ tasks
- Breaks down work into tasks
- Maps dependencies

**Business Analyst**:
- Use for enterprise tasks
- Analyzes business requirements
- Ensures business-IT alignment

### Development Agents

**Architects**:
- Use for complex+ tasks
- Design architecture before implementation
- Provide implementation guidance

**Developers**:
- Use for all tasks
- Implement solutions
- Follow architecture (if provided)

### Quality Agents

**Code Reviewer**:
- Use for medium+ tasks
- Reviews code quality
- Provides feedback

**Test Automator**:
- Use for medium+ tasks
- Writes comprehensive tests
- Ensures test coverage

**Security Auditor**:
- Use for enterprise tasks
- Performs security audits
- Identifies vulnerabilities

### Validation Agents

**Spec Validator**:
- Use for complex+ tasks
- Validates against requirements
- Ensures production readiness

## Quality Gates

### When Gates Apply

- **Simple tasks**: No gates
- **Medium tasks**: Basic review gate (80%)
- **Complex tasks**: Full gates (85-95%)
- **Enterprise tasks**: All gates + iterations

### Gate Failure Handling

If gate fails:
1. Review gate feedback
2. Fix identified issues
3. Re-run gate
4. Don't skip gates

### Gate Optimization

- Set appropriate thresholds
- Provide detailed feedback
- Allow iterations
- Learn from results

## Token Optimization

### Minimize Tokens

- Use simple workflow for simple tasks
- Avoid unnecessary agents
- Don't over-plan simple tasks
- Cache context between agents

### Maximize Value

- Use complex workflow for complex tasks
- Include all necessary agents
- Plan thoroughly for complex tasks
- Quality gates ensure quality

## Performance Optimization

### Parallel Execution

Some agents can run in parallel:
- Planning: requirements-analyzer + architects
- Development: backend-developer + frontend-developer
- Validation: Sequential (code-reviewer → spec-validator)

### Early Validation

- Catch issues early
- Avoid rework
- Save tokens and time

### Incremental Delivery

- Ship working increments
- Get feedback early
- Iterate based on feedback

## Common Mistakes

### Mistake 1: Over-Engineering Simple Tasks

❌ **Bad**: Using complex workflow for bug fix
✅ **Good**: Direct agent call for bug fix

### Mistake 2: Under-Engineering Complex Tasks

❌ **Bad**: Using simple workflow for new service
✅ **Good**: Full pipeline for new service

### Mistake 3: Skipping Quality Gates

❌ **Bad**: Skipping gates to save tokens
✅ **Good**: Gates ensure quality

### Mistake 4: Ignoring Gate Feedback

❌ **Bad**: Ignoring gate failures
✅ **Good**: Fix issues and re-run gates

### Mistake 5: Manual Workflow Selection

❌ **Bad**: Manually selecting workflows
✅ **Good**: Let system analyze and select

## Monitoring and Optimization

### Track Metrics

- Tokens used
- Time taken
- Quality scores
- Gate pass rates

### Optimize Based on Data

- Identify patterns
- Adjust thresholds
- Improve workflows
- Learn from results

## Next Steps

- Review [SETUP.md](SETUP.md) for setup instructions
- Check [USAGE.md](USAGE.md) for usage guide
- See [ARCHITECTURE.md](ARCHITECTURE.md) for architecture details
