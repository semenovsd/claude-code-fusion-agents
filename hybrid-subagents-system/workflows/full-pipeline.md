---
name: full-pipeline
description: Complete pipeline workflow for complex tasks. Full orchestration with quality gates, 5-10+ agents, comprehensive planning and validation.
complexity_level: 3
estimated_tokens: 15000-50000
estimated_time: 45-120 minutes
---

# Full Pipeline Workflow

**Purpose**: Handle complex tasks with full pipeline orchestration, comprehensive planning, and quality gates.

**Complexity Level**: 3 (Complex Tasks)

**When to Use:**
- New projects or major subsystems
- Architectural changes
- Multi-domain requirements
- Requires comprehensive planning
- Needs full QA pipeline
- Multiple integration points

## Workflow Process

```
User Request
    ↓
Task Complexity Analyzer
    ↓
[Complex Task Detected]
    ↓
═══════════════════════════════════
  PHASE 1: PLANNING
═══════════════════════════════════
requirements-analyst → requirements
technical-planner → implementation plan
backend-architect → architecture design
    ↓
[Planning Quality Gate] → PASS/FAIL
    ↓
═══════════════════════════════════
  PHASE 2: DEVELOPMENT
═══════════════════════════════════
backend-architect → backend implementation
frontend-developer → frontend implementation
test-automator → test creation
    ↓
[Development Quality Gate] → PASS/FAIL
    ↓
═══════════════════════════════════
  PHASE 3: VALIDATION
═══════════════════════════════════
code-reviewer → code review
security-auditor → security audit
quality-validator → final validation
    ↓
[Validation Quality Gate] → PASS/FAIL
    ↓
═══════════════════════════════════
  RESULT
═══════════════════════════════════
```

## Phase 1: Planning

### Agents
- `requirements-analyst` - Requirements analysis
- `technical-planner` - Implementation planning
- `backend-architect` - Architecture design (if backend)
- `frontend-developer` - UI/UX planning (if frontend)

### Deliverables
- Requirements specification
- Implementation plan
- Architecture design
- Task breakdown

### Quality Gate
- **Planning Quality Gate** (95% threshold)
- Validates requirements, architecture, planning

## Phase 2: Development

### Agents
- `backend-architect` - Backend implementation
- `frontend-developer` - Frontend implementation
- `test-automator` - Test creation
- Language specialists as needed

### Deliverables
- Implemented code
- Tests (unit + integration)
- Documentation

### Quality Gate
- **Development Quality Gate** (85% threshold)
- Validates code quality, test coverage, security, performance

## Phase 3: Validation

### Agents
- `code-reviewer` - Code review
- `security-auditor` - Security audit
- `quality-validator` - Final validation
- `documentation-expert` - Documentation review

### Deliverables
- Code review report
- Security audit report
- Quality validation report
- Complete documentation

### Quality Gate
- **Validation Quality Gate** (95% threshold)
- Validates review completion, tests, documentation, deployment readiness

## Typical Team Compositions

### New Full-Stack Project
**Planning:**
- `requirements-analyst`
- `technical-planner`
- `backend-architect`
- `frontend-developer`

**Development:**
- `backend-architect`
- `frontend-developer`
- `test-automator`

**Validation:**
- `code-reviewer`
- `security-auditor`
- `quality-validator`
- `documentation-expert`

### Microservices Refactoring
**Planning:**
- `requirements-analyst`
- `technical-planner`
- `backend-architect` (multiple instances)

**Development:**
- `backend-architect` (multiple instances)
- `test-automator`
- `performance-engineer`

**Validation:**
- `code-reviewer`
- `security-auditor`
- `performance-engineer`
- `quality-validator`

## Example Execution

**Request:** "Build e-commerce platform from scratch"

**Execution:**

**Phase 1: Planning (20 minutes)**
- `requirements-analyst`: Requirements analysis
- `technical-planner`: Implementation plan
- `backend-architect`: Architecture design
- Planning Quality Gate: ✅ PASSED (96%)

**Phase 2: Development (60 minutes)**
- `backend-architect`: Backend implementation
- `frontend-developer`: Frontend implementation
- `test-automator`: Test creation
- Development Quality Gate: ✅ PASSED (88%)

**Phase 3: Validation (20 minutes)**
- `code-reviewer`: Code review
- `security-auditor`: Security audit
- `quality-validator`: Final validation
- Validation Quality Gate: ✅ PASSED (91%)

**Total Time:** 100 minutes
**Total Tokens:** 35000 tokens

## Output Format

```markdown
## Pipeline Execution

**Task:** [Task description]
**Team:** [5-10 agents]
**Status:** ✅ Complete
**Time:** [X] minutes
**Tokens:** [X] tokens

### Phase 1: Planning
- ✅ Requirements analysis
- ✅ Architecture design
- ✅ Task planning
- ✅ Planning Quality Gate: PASSED ([X]%)

### Phase 2: Development
- ✅ Backend implementation
- ✅ Frontend implementation
- ✅ Testing
- ✅ Development Quality Gate: PASSED ([X]%)

### Phase 3: Validation
- ✅ Code review
- ✅ Security audit
- ✅ Final validation
- ✅ Validation Quality Gate: PASSED ([X]%)

**Deliverables:**
- [Comprehensive list]

**Result:** [Detailed summary]
```

## Quality Gates

### Planning Gate (95% threshold)
- Requirements completeness
- Architecture feasibility
- Task breakdown adequacy
- Risk mitigation coverage

### Development Gate (85% threshold)
- Code quality (>85%)
- Test coverage (>80%)
- Security scan passed
- Performance benchmarks met

### Validation Gate (95% threshold)
- Code review passed
- All tests passing
- Documentation complete
- Deployment ready

## Optimization

- **Comprehensive planning** prevents rework
- **Quality gates** ensure standards
- **Parallel execution** when possible
- **Iterative improvement** through gates
