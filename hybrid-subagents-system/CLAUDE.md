# CLAUDE.md - Hybrid Subagents System

This project uses the **Hybrid Subagents System** for AI agent orchestration.

## Agent Dispatch Protocol

For complex, multi-domain tasks requiring specialized expertise, this project uses the Adaptive Orchestrator system.

### When to Use Agent Orchestration

Use agent orchestration when encountering tasks that involve:
- Multiple technology domains
- Complex architectural decisions
- Cross-functional requirements
- System-wide changes
- New projects or major subsystems

### Workflow Levels

#### Simple Tasks
- Single file modifications
- Simple refactoring
- Bug fixes
- Documentation updates

**Routing:** Direct execution, no orchestration

#### Medium Tasks
- New features in existing modules
- Module refactoring
- Integration between components
- Requires planning but not architecture

**Routing:** Focused team coordination (2-4 agents)

#### Complex Tasks
- New projects or major subsystems
- Architectural changes
- Multi-domain requirements
- Requires comprehensive planning
- Needs full QA pipeline

**Routing:** Full pipeline with quality gates (5-10+ agents)

## Project Overview

[Describe your project here]

## Technology Stack

[List your technology stack]

## Development Commands

```bash
# Setup
npm install

# Development
npm run dev

# Testing
npm test

# Build
npm run build

# Deploy
npm run deploy
```

## Architecture Overview

[Describe your architecture]

## Configuration

[Important configuration details]

## Testing

[Testing approach and coverage targets]

## Deployment

[Deployment procedures]

## Monitoring

[Monitoring and observability setup]

## Agent Usage Examples

### Simple Task
```
"Fix typo in UserService.ts line 42"
→ Routes to simple workflow
→ Direct execution
```

### Medium Task
```
"Add user profile editing feature"
→ Routes to standard workflow
→ Team: backend-architect, frontend-developer, test-automator
```

### Complex Task
```
"Build e-commerce platform from scratch"
→ Routes to full pipeline
→ Phases: Planning → Development → Validation
→ Quality gates: All passed
```

## Quality Standards

- Code quality: >85%
- Test coverage: >80%
- Security: Zero critical vulnerabilities
- Performance: p95 < 200ms

## Best Practices

- Follow project conventions
- Write comprehensive tests
- Document changes
- Review code thoroughly
- Maintain security standards
