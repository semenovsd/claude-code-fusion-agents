# Architecture Documentation

Detailed architecture documentation for the Hybrid Subagents System.

## System Overview

The Hybrid Subagents System is a unified AI agent orchestration system that combines best practices from three leading subagent repositories:

- **lst97**: Optimal balance, MCP integration, real metrics
- **VoltAgent**: Wide coverage, production-ready, detailed checklists
- **zhsama**: Structured workflows, quality gates, full cycle

## Core Architecture

### Orchestration Layer

```
┌─────────────────────────────────────────┐
│      Smart Orchestrator                 │
│  (Master Coordinator)                    │
└──────────────┬──────────────────────────┘
               │
       ┌───────┴───────┐
       │               │
┌──────▼──────┐  ┌─────▼──────┐
│ Complexity  │  │ Workflow   │
│  Analyzer   │  │  Selector  │
└─────────────┘  └────────────┘
       │               │
       └───────┬───────┘
               │
       ┌───────▼───────┐
       │ Agent Team    │
       │   Builder     │
       └───────┬───────┘
               │
       ┌───────▼───────┐
       │ Quality Gate  │
       │   Manager     │
       └───────────────┘
```

### Agent Categories

#### 1. Orchestration Agents
- **Smart Orchestrator**: Master coordinator
- **Task Complexity Analyzer**: Complexity assessment
- **Workflow Selector**: Workflow pattern selection
- **Agent Team Builder**: Team assembly
- **Quality Gate Manager**: Gate management

#### 2. Planning Agents
- **Requirements Analyzer**: Requirement analysis
- **Task Planner**: Task breakdown
- **Business Analyst**: Business requirements (enterprise)

#### 3. Development Agents
- **Backend Architect**: Backend architecture design
- **Frontend Architect**: Frontend architecture design
- **Backend Developer**: Backend implementation
- **Frontend Developer**: Frontend implementation
- **Fullstack Developer**: Fullstack implementation

#### 4. Quality Agents
- **Code Reviewer**: Code review
- **Test Automator**: Test automation
- **Security Auditor**: Security audit (enterprise)

#### 5. Validation Agents
- **Spec Validator**: Specification validation
- **Spec Reviewer**: Specification review (enterprise)

## Workflow Architecture

### Simple Workflow

```
User Request
    │
    ▼
Smart Orchestrator
    │
    ▼
Complexity Analyzer (Score: 2)
    │
    ▼
Workflow Selector (Simple)
    │
    ▼
Agent Team Builder (1 agent)
    │
    ▼
Direct Agent Call
    │
    ▼
Result
```

### Medium Workflow

```
User Request
    │
    ▼
Smart Orchestrator
    │
    ▼
Complexity Analyzer (Score: 6)
    │
    ▼
Workflow Selector (Medium)
    │
    ▼
Agent Team Builder (2-3 agents)
    │
    ├─► Task Planner
    │       │
    │       ▼
    │   Execution Plan
    │
    ├─► Specialist Agent(s)
    │       │
    │       ▼
    │   Implementation
    │
    └─► Code Reviewer
            │
            ▼
        Review Gate (80%)
            │
            ▼
        Result
```

### Complex Workflow

```
User Request
    │
    ▼
Smart Orchestrator
    │
    ▼
Complexity Analyzer (Score: 9)
    │
    ▼
Workflow Selector (Complex)
    │
    ▼
Agent Team Builder (5-7 agents)
    │
    ├─► Phase 1: Planning
    │   ├─► Requirements Analyzer
    │   ├─► Backend Architect
    │   └─► Frontend Architect
    │           │
    │           ▼
    │   Planning Gate (95%)
    │
    ├─► Phase 2: Development
    │   ├─► Backend Developer
    │   ├─► Frontend Developer
    │   └─► Test Automator
    │           │
    │           ▼
    │   Development Gate (85%)
    │
    └─► Phase 3: Validation
        ├─► Code Reviewer
        └─► Spec Validator
                │
                ▼
        Validation Gate (95%)
                │
                ▼
        Result
```

### Enterprise Workflow

```
User Request
    │
    ▼
Smart Orchestrator
    │
    ▼
Complexity Analyzer (Score: 10)
    │
    ▼
Workflow Selector (Enterprise)
    │
    ▼
Agent Team Builder (7+ agents)
    │
    ├─► Iteration 1: Planning
    │   ├─► Requirements Analyzer
    │   ├─► Business Analyst
    │   ├─► Backend Architect
    │   └─► Frontend Architect
    │           │
    │           ▼
    │   Planning Gate (95%)
    │
    ├─► Iteration 2: Development
    │   ├─► Backend Developer
    │   ├─► Frontend Developer
    │   └─► Test Automator
    │           │
    │           ▼
    │   Development Gate (85%)
    │
    ├─► Iteration 3: Optimization
    │   ├─► Security Auditor
    │   └─► Performance Engineer
    │           │
    │           ▼
    │   Optimization Gate (90%)
    │
    └─► Iteration 4: Validation
        ├─► Code Reviewer
        ├─► Spec Reviewer
        └─► Spec Validator
                │
                ▼
        Validation Gate (95%)
                │
                ▼
        Result
```

## Complexity Analysis

### Scoring Factors

1. **Scope** (1-3 points)
   - Single element: 1
   - Module: 2
   - System: 3

2. **Dependencies** (0-2 points)
   - None: 0
   - Internal: 1
   - External: 2

3. **Architecture Impact** (0-3 points)
   - None: 0
   - Minor: 1
   - Major: 2
   - New: 3

4. **Testing Requirements** (0-2 points)
   - Minimal: 0
   - Unit: 1
   - Comprehensive: 2

5. **Integration Complexity** (0-2 points)
   - None: 0
   - Simple: 1
   - Complex: 2

**Total**: 1-12 → Mapped to 1-10 scale

### Complexity Levels

- **1-3**: Simple (direct call)
- **4-6**: Medium (planning + execution + review)
- **7-9**: Complex (full pipeline with gates)
- **10**: Enterprise (multi-phase iterative)

## Quality Gates

### Gate Types

1. **Planning Validation** (Complex+)
   - Threshold: 95%
   - Criteria: Requirements completeness, architecture feasibility

2. **Development Validation** (Complex+)
   - Threshold: 85%
   - Criteria: Code quality, test coverage, performance

3. **Production Readiness** (Complex+)
   - Threshold: 95%
   - Criteria: Code review, tests passing, documentation

4. **Security & Performance** (Enterprise)
   - Threshold: 90%
   - Criteria: Security audit, performance optimization

## Integration Points

### MCP Integration

- **context7**: Framework/library documentation
- **sequential-thinking**: Complex reasoning

### Agent Communication

Agents communicate through:
- Structured JSON protocols
- Shared documentation files
- Context passing

## Performance Optimization

### Token Optimization

- Simple tasks: Direct calls (5K-20K tokens)
- Medium tasks: Minimal planning (30K-80K tokens)
- Complex tasks: Optimized phases (100K-300K tokens)
- Enterprise tasks: Iterative refinement (300K-1M+ tokens)

### Time Optimization

- Parallel execution where possible
- Early validation to catch issues
- Incremental delivery
- Smart caching

## Best Practices

1. **Right Tool for Right Job**: Match workflow to complexity
2. **Token Efficiency**: Minimize tokens without compromising quality
3. **Quality When Needed**: Gates for complex+ tasks only
4. **Iterative Refinement**: Allow iterations for enterprise tasks
5. **Performance Tracking**: Monitor metrics continuously

## Next Steps

- Review [SETUP.md](SETUP.md) for setup instructions
- Check [USAGE.md](USAGE.md) for usage guide
- See [BEST_PRACTICES.md](BEST_PRACTICES.md) for best practices
