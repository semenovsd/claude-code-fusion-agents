# Usage Guide

## Getting Started

### 1. Installation

Copy the hybrid system to your Claude Code agents directory:

```bash
# Example (adjust path for your system)
cp -r hybrid-subagents-system ~/.cursor/agents/
```

### 2. Configuration

Ensure MCP servers are configured in your Claude Code settings:

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@context7/cli"]
    },
    "sequential-thinking": {
      "command": "npx",
      "args": ["-y", "@sequential-thinking/cli"]
    }
  }
}
```

### 3. First Use

The system automatically routes tasks. Simply describe your task:

```
User: "Add user authentication to my app"
```

The system will:
1. Analyze task complexity
2. Route to appropriate workflow
3. Execute with optimal team
4. Return results

## Task Complexity Examples

### Simple Tasks

**Examples:**
- "Fix typo in UserService.ts line 42"
- "Add JSDoc comment to calculateTotal function"
- "Update API endpoint URL in config"

**What Happens:**
- Routes to simple workflow
- Direct execution by specialist
- Fast completion (2-5 minutes)

### Medium Tasks

**Examples:**
- "Add user profile editing feature"
- "Refactor authentication module"
- "Integrate payment gateway"

**What Happens:**
- Routes to standard workflow
- Team of 2-4 agents
- Coordinated execution (10-25 minutes)

### Complex Tasks

**Examples:**
- "Build e-commerce platform from scratch"
- "Refactor monolith to microservices"
- "Create full-stack SaaS application"

**What Happens:**
- Routes to full pipeline
- Team of 5-10+ agents
- Three phases with quality gates (45-120 minutes)

## Workflow Selection

The system automatically selects workflow based on:

1. **Task Scope**
   - Single file → Simple
   - Multiple files → Medium/Complex
   - Entire project → Complex

2. **Planning Needs**
   - No planning → Simple
   - Basic planning → Medium
   - Comprehensive planning → Complex

3. **Architecture Changes**
   - No changes → Simple/Medium
   - Architectural changes → Complex

4. **Integration Points**
   - 0 integrations → Simple
   - 1-3 integrations → Medium
   - 4+ integrations → Complex

## Manual Override

You can manually specify workflow level:

```
User: "Add user profile editing [complex]"
```

This forces complex workflow even if task seems simpler.

## Quality Gates

### Planning Gate

**When:** After planning phase (complex tasks only)

**Checks:**
- Requirements completeness
- Architecture feasibility
- Task breakdown adequacy
- Risk mitigation coverage

**Threshold:** 95%

**If Failed:**
- Returns to planning phase
- Addresses identified gaps
- Re-validates

### Development Gate

**When:** After development phase (medium/complex tasks)

**Checks:**
- Code quality (>85%)
- Test coverage (>80%)
- Security scan passed
- Performance benchmarks met

**Threshold:** 85%

**If Failed:**
- Returns to development phase
- Fixes identified issues
- Re-validates

### Validation Gate

**When:** After validation phase (complex tasks only)

**Checks:**
- Code review passed
- All tests passing
- Documentation complete
- Deployment ready

**Threshold:** 95%

**If Failed:**
- Returns to appropriate phase
- Addresses issues
- Re-validates

## Best Practices

### 1. Clear Task Description

**Good:**
```
"Add user profile editing feature with avatar upload, 
email change, and password reset"
```

**Bad:**
```
"Fix user stuff"
```

### 2. Provide Context

**Good:**
```
"Add user profile editing to my React + Node.js app. 
Backend uses Express, frontend uses React. Database is PostgreSQL."
```

**Bad:**
```
"Add profile editing"
```

### 3. Specify Requirements

**Good:**
```
"Add user authentication with JWT tokens, password hashing with bcrypt, 
and refresh token mechanism"
```

**Bad:**
```
"Add auth"
```

### 4. Trust the System

Let the system automatically route tasks. Manual intervention rarely needed.

### 5. Review Quality Gates

Quality gate outputs provide actionable feedback. Review and address issues.

## Common Use Cases

### Use Case 1: Simple Bug Fix

```
User: "Fix null pointer exception in UserService.getUser() method"
→ Simple workflow
→ Direct to backend-developer
→ 3 minutes, 1000 tokens
```

### Use Case 2: New Feature

```
User: "Add user profile editing with avatar upload"
→ Standard workflow
→ Team: backend-architect, frontend-developer, test-automator
→ 20 minutes, 6000 tokens
```

### Use Case 3: New Project

```
User: "Build e-commerce platform with products, cart, checkout, and payments"
→ Full pipeline
→ Phases: Planning → Development → Validation
→ Quality gates: All passed
→ 90 minutes, 30000 tokens
```

## Troubleshooting

### Issue: Task Routed Incorrectly

**Solution:** Provide more context or manually specify complexity level.

### Issue: Quality Gate Failing

**Solution:** Review quality gate output, address identified issues, re-run.

### Issue: High Token Usage

**Solution:** Check if task is unnecessarily complex. Consider breaking into smaller tasks.

### Issue: Slow Execution

**Solution:** Check if parallel execution is possible. Review agent selection.

## Advanced Usage

### Custom Agent Teams

Specify custom team composition:

```
User: "Add feature X [team: backend-architect, test-automator]"
```

### Skip Quality Gates

Not recommended, but possible:

```
User: "Add feature X [skip-gates]"
```

### Force Workflow Level

Force specific workflow:

```
User: "Add feature X [workflow: complex]"
```

## Monitoring

### Token Usage

Track token usage per task:
- Simple: 500-2000 tokens
- Medium: 3000-8000 tokens
- Complex: 15000-50000+ tokens

### Execution Time

Monitor execution time:
- Simple: 2-5 minutes
- Medium: 10-25 minutes
- Complex: 45-120 minutes

### Quality Metrics

Review quality gate results:
- Planning gate: 95% threshold
- Development gate: 85% threshold
- Validation gate: 95% threshold

## Support

For issues or questions:
1. Check documentation
2. Review quality gate outputs
3. Check system logs
4. Create issue with details
