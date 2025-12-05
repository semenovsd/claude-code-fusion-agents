# Hybrid Subagents System

**Unified AI Agent System combining best practices from lst97, VoltAgent, and zhsama**

A comprehensive, intelligent subagent system for Claude Code that automatically adapts workflow complexity based on task requirements. Simple tasks use direct agent calls (minimal tokens), while complex tasks use full multi-phase pipelines with quality gates (maximum effectiveness).

## 🎯 Key Features

- **Smart Orchestration**: Automatically selects optimal workflow (simple/medium/complex/enterprise)
- **Token Efficiency**: Minimizes tokens for simple tasks, full power for complex ones
- **Quality Gates**: Progressive quality gates for complex+ tasks
- **Full-Stack Support**: Complete coverage for frontend, backend, and fullstack development
- **Intelligent Planning**: Deep requirements analysis and task planning
- **Production-Ready**: Enterprise-grade quality assurance

## 🏗️ Architecture

### Core Components

1. **Smart Orchestrator** (`agents/orchestration/smart-orchestrator.md`)
   - Master orchestrator that analyzes tasks and selects workflows
   - Complexity analysis (1-10 scale)
   - Adaptive workflow selection

2. **Task Complexity Analyzer** (`agents/orchestration/task-complexity-analyzer.md`)
   - Analyzes task complexity based on scope, dependencies, architecture impact
   - Provides detailed complexity breakdown

3. **Workflow Selector** (`agents/orchestration/workflow-selector.md`)
   - Selects optimal workflow pattern based on complexity
   - Maps complexity to workflow (simple/medium/complex/enterprise)

4. **Agent Team Builder** (`agents/orchestration/agent-team-builder.md`)
   - Assembles optimal agent teams
   - Minimizes team size while ensuring coverage

5. **Quality Gate Manager** (`agents/orchestration/quality-gate-manager.md`)
   - Manages quality gates between phases
   - Applies gates only when needed

### Agent Categories

- **Planning**: Requirements Analyzer, Task Planner, Business Analyst
- **Development**: Backend/Frontend Architects, Backend/Frontend Developers
- **Quality**: Code Reviewer, Test Automator, Security Auditor
- **Validation**: Spec Validator, Spec Reviewer

## 📊 Workflow Levels

### Simple (Complexity 1-3)
- **Agents**: 1 specialist
- **Tokens**: 5K-20K
- **Time**: 1-5 minutes
- **Gates**: None
- **Use Case**: Bug fixes, simple changes

### Medium (Complexity 4-6)
- **Agents**: 2-3 (planner + specialist + reviewer)
- **Tokens**: 30K-80K
- **Time**: 5-15 minutes
- **Gates**: Basic review
- **Use Case**: New features, module refactoring

### Complex (Complexity 7-9)
- **Agents**: 5-7 (full team)
- **Tokens**: 100K-300K
- **Time**: 15-45 minutes
- **Gates**: Planning, Development, Validation
- **Use Case**: New services, major refactoring

### Enterprise (Complexity 10)
- **Agents**: 7+ (full team + specialists)
- **Tokens**: 300K-1M+
- **Time**: 45+ minutes
- **Gates**: All gates + iterative refinement
- **Use Case**: New systems, architecture overhaul

## 🚀 Quick Start

### Installation

1. Clone this repository
2. Copy agents to your Claude Code subagents directory
3. Configure MCP servers (context7, sequential-thinking)
4. Use `/smart-dev` command

### Usage

```bash
# Simple task (automatic direct call)
/smart-dev Fix typo in login form

# Medium task (planning + execution + review)
/smart-dev Add user profile picture upload

# Complex task (full pipeline with gates)
/smart-dev Implement microservices for user management

# Enterprise task (multi-phase iterative)
/smart-dev Build new e-commerce platform
```

## 📁 Project Structure

```
hybrid-subagents-system/
├── agents/
│   ├── orchestration/      # Core orchestration agents
│   ├── planning/           # Planning agents
│   ├── development/        # Development agents
│   ├── quality/            # Quality assurance agents
│   └── validation/         # Validation agents
├── workflows/              # Workflow definitions
├── commands/               # Slash commands
└── docs/                   # Documentation
```

## 🔧 Configuration

### MCP Servers

Required MCP servers:
- **context7**: For framework/library documentation
- **sequential-thinking**: For complex reasoning

See `docs/SETUP.md` for detailed setup instructions.

## 📚 Documentation

- **[ARCHITECTURE.md](docs/ARCHITECTURE.md)**: Detailed architecture documentation
- **[SETUP.md](docs/SETUP.md)**: Setup and configuration guide
- **[USAGE.md](docs/USAGE.md)**: Usage guide with examples
- **[BEST_PRACTICES.md](docs/BEST_PRACTICES.md)**: Best practices and guidelines

## 🎓 Best Practices

1. **Let the system decide**: Don't manually select workflows, let Smart Orchestrator choose
2. **Trust complexity analysis**: System accurately assesses task complexity
3. **Use quality gates**: They ensure quality without over-engineering
4. **Monitor metrics**: Track tokens, time, and quality scores
5. **Iterate when needed**: Enterprise tasks allow iterative refinement

## 🤝 Contributing

This system combines best practices from:
- **lst97/claude-code-sub-agents**: Optimal balance, MCP integration, real metrics
- **VoltAgent/awesome-claude-code-subagents**: Wide coverage, production-ready, detailed checklists
- **zhsama/claude-sub-agent**: Structured workflows, quality gates, full cycle

## 📝 License

See LICENSE file for details.

## 🙏 Acknowledgments

- lst97 for optimal agent design and MCP integration
- VoltAgent for comprehensive agent coverage and production-ready approach
- zhsama for structured workflow system and quality gates

---

**Built with ❤️ combining the best of three worlds**
