# Hybrid Subagents System

**Unified AI Agent Orchestration System combining the best practices from lst97, VoltAgent, and zhsama repositories.**

## Overview

This hybrid system combines:
- **Intelligent orchestration** from lst97 (claude-code-sub-agents)
- **Comprehensive categorization** from VoltAgent (awesome-claude-code-subagents)
- **Structured workflows** from zhsama (claude-sub-agent)

**Result:** A production-ready, adaptive AI agent system that automatically routes tasks to appropriate complexity levels, optimizing for both effectiveness and token efficiency.

## Key Features

### 🎯 Adaptive Complexity Routing
- **Simple tasks** → Direct execution (no orchestration overhead)
- **Medium tasks** → Focused team coordination (2-4 agents)
- **Complex tasks** → Full pipeline with quality gates (5-10+ agents)

### 🚀 Token Optimization
- Adaptive model selection (haiku/sonnet/opus)
- Prompt optimization based on complexity
- Parallel execution when possible
- Context caching and reuse

### 📊 Quality Gates
- Planning Quality Gate (95% threshold)
- Development Quality Gate (85% threshold)
- Validation Quality Gate (95% threshold)

### 🔄 Full-Stack Focus
- Complete development lifecycle support
- From requirements to deployment
- Comprehensive testing and validation

### 🧠 Intelligent Planning
- Requirements analysis
- Technical planning
- Architecture design
- Task breakdown

## Architecture

```
hybrid-subagents-system/
├── agents/
│   ├── orchestration/          # Orchestration agents
│   │   ├── adaptive-orchestrator.md
│   │   └── task-complexity-analyzer.md
│   ├── planning/               # Planning agents
│   │   ├── requirements-analyst.md
│   │   └── technical-planner.md
│   ├── development/            # Development agents
│   │   ├── backend-architect.md
│   │   └── [other specialists]
│   └── quality/                # Quality agents
│       ├── code-reviewer.md
│       ├── test-automator.md
│       └── security-auditor.md
├── workflows/                  # Workflow definitions
│   ├── simple-workflow.md
│   ├── standard-workflow.md
│   └── full-pipeline.md
├── quality-gates/             # Quality gate definitions
│   ├── planning-gate.md
│   ├── development-gate.md
│   └── validation-gate.md
└── docs/                      # Documentation
    ├── ARCHITECTURE.md
    ├── USAGE_GUIDE.md
    └── BEST_PRACTICES.md
```

## Quick Start

### 1. Installation

Copy the `hybrid-subagents-system` directory to your Claude Code agents directory:

```bash
# Example path (adjust for your system)
cp -r hybrid-subagents-system ~/.cursor/agents/
```

### 2. Configuration

Ensure MCP servers are configured:
- `context7` - For library documentation
- `sequential-thinking` - For complex reasoning

### 3. Usage

The system automatically routes tasks based on complexity:

**Simple Task Example:**
```
User: "Fix typo in UserService.ts line 42"
→ Routes to: Simple workflow
→ Executes: Direct to typescript-pro
→ Time: 2 minutes, Tokens: 800
```

**Medium Task Example:**
```
User: "Add user profile editing feature"
→ Routes to: Standard workflow
→ Team: backend-architect, frontend-developer, test-automator
→ Time: 15 minutes, Tokens: 5000
```

**Complex Task Example:**
```
User: "Build e-commerce platform from scratch"
→ Routes to: Full pipeline
→ Phases: Planning → Development → Validation
→ Quality Gates: All passed
→ Time: 100 minutes, Tokens: 35000
```

## Workflow Levels

### Level 1: Simple Workflow
- **Complexity:** Simple tasks
- **Agents:** 1 specialist
- **Tokens:** 500-2000
- **Time:** 2-5 minutes
- **Quality Gates:** None

### Level 2: Standard Workflow
- **Complexity:** Medium tasks
- **Agents:** 2-4 specialists
- **Tokens:** 3000-8000
- **Time:** 10-25 minutes
- **Quality Gates:** Development gate only

### Level 3: Full Pipeline
- **Complexity:** Complex tasks
- **Agents:** 5-10+ specialists
- **Tokens:** 15000-50000+
- **Time:** 45-120 minutes
- **Quality Gates:** All gates (Planning, Development, Validation)

## Core Agents

### Orchestration
- **adaptive-orchestrator** - Master orchestrator, routes tasks to appropriate workflows
- **task-complexity-analyzer** - Analyzes task complexity for routing

### Planning
- **requirements-analyst** - Requirements analysis and documentation
- **technical-planner** - Implementation planning and task breakdown

### Development
- **backend-architect** - Backend architecture and implementation
- **frontend-developer** - Frontend development
- **full-stack-developer** - End-to-end development

### Quality
- **code-reviewer** - Code quality review
- **test-automator** - Test creation and automation
- **security-auditor** - Security validation
- **quality-validator** - Final quality validation

## Quality Gates

### Planning Quality Gate (95%)
- Requirements completeness
- Architecture feasibility
- Task breakdown adequacy
- Risk mitigation coverage

### Development Quality Gate (85%)
- Code quality (>85%)
- Test coverage (>80%)
- Security scan passed
- Performance benchmarks met

### Validation Quality Gate (95%)
- Code review passed
- All tests passing
- Documentation complete
- Deployment ready

## Best Practices

### 1. Let the System Route
Don't manually specify workflow level. The system automatically determines optimal routing.

### 2. Trust the Quality Gates
Quality gates ensure standards. Don't skip them for complex tasks.

### 3. Provide Clear Requirements
Clear requirements lead to better analysis and planning.

### 4. Review Quality Gate Results
Quality gate outputs provide actionable feedback for improvement.

### 5. Monitor Token Usage
Track token usage to optimize prompts and workflows.

## Token Optimization

### Strategies
1. **Model Selection:** haiku for orchestration, sonnet for specialists
2. **Prompt Optimization:** Adaptive prompt sizes based on complexity
3. **Context Caching:** Reuse project analysis across agents
4. **Parallel Execution:** Execute independent tasks in parallel

### Estimated Token Usage
- Simple tasks: 500-2000 tokens
- Medium tasks: 3000-8000 tokens
- Complex tasks: 15000-50000+ tokens

## Integration

### MCP Servers
- **context7:** Library documentation and best practices
- **sequential-thinking:** Complex reasoning and analysis

### Project Integration
- Works with existing Claude Code projects
- Integrates with project structure
- Respects existing patterns and conventions

## Documentation

- **[ARCHITECTURE.md](docs/ARCHITECTURE.md)** - System architecture details
- **[USAGE_GUIDE.md](docs/USAGE_GUIDE.md)** - Detailed usage guide
- **[BEST_PRACTICES.md](docs/BEST_PRACTICES.md)** - Best practices and recommendations

## Contributing

This is a hybrid system combining best practices from:
- [lst97/claude-code-sub-agents](https://github.com/lst97/claude-code-sub-agents)
- [VoltAgent/awesome-claude-code-subagents](https://github.com/VoltAgent/awesome-claude-code-subagents)
- [zhsama/claude-sub-agent](https://github.com/zhsama/claude-sub-agent)

## License

This system combines practices from multiple open-source repositories. Please refer to original repositories for licensing information.

## Support

For issues, questions, or contributions, please refer to the original repositories or create an issue in this repository.

---

**Built with ❤️ combining the best practices from the Claude Code subagent community.**
