---
name: development-quality-gate
description: Quality gate for development phase validation. Ensures code quality, test coverage, security, and performance standards before proceeding to validation phase.
threshold: 85%
applies_to: medium-tasks, complex-tasks
---

# Development Quality Gate

**Purpose**: Validate that development phase deliverables meet quality standards before proceeding to validation phase.

**Threshold**: 85% compliance required

**Applies To**: Medium tasks (Level 2) and Complex tasks (Level 3)

## Validation Criteria

### 1. Code Quality (30%)

**Checklist:**
- [ ] Code follows project style guide
- [ ] No linting errors
- [ ] Type checking passes (if applicable)
- [ ] Code is readable and maintainable
- [ ] Functions are focused and small
- [ ] Error handling implemented
- [ ] Logging added where appropriate

**Scoring:**
- Excellent (100%): All checks pass, code is exemplary
- Good (90%): Minor issues, easily fixable
- Needs Improvement (<85%): Significant quality issues

**Metrics:**
- Code quality score: >85/100
- Linting errors: 0
- Type errors: 0

### 2. Test Coverage (25%)

**Checklist:**
- [ ] Unit tests written for core logic
- [ ] Integration tests for APIs
- [ ] Test coverage meets targets
- [ ] Tests are meaningful and test behavior
- [ ] Edge cases covered
- [ ] Error scenarios tested

**Scoring:**
- Excellent (100%): Coverage exceeds targets, comprehensive tests
- Good (90%): Coverage meets targets, good test quality
- Needs Improvement (<85%): Coverage below targets or poor tests

**Metrics:**
- Unit test coverage: >80% (complex), >70% (medium)
- Integration test coverage: >70% (complex), >60% (medium)
- All tests passing: 100%

### 3. Security Standards (25%)

**Checklist:**
- [ ] Input validation implemented
- [ ] SQL injection prevention (if applicable)
- [ ] XSS prevention (if applicable)
- [ ] Authentication/authorization implemented
- [ ] Sensitive data encrypted
- [ ] Security best practices followed
- [ ] Dependency vulnerabilities scanned

**Scoring:**
- Secure (100%): All security checks pass
- Mostly Secure (90%): Minor security concerns
- Needs Improvement (<85%): Security vulnerabilities present

**Metrics:**
- Security scan: 0 critical, 0 high vulnerabilities
- OWASP compliance: Pass

### 4. Performance Benchmarks (20%)

**Checklist:**
- [ ] Performance targets met
- [ ] Database queries optimized
- [ ] Caching implemented where appropriate
- [ ] No obvious performance bottlenecks
- [ ] Response times within targets

**Scoring:**
- Excellent (100%): Exceeds performance targets
- Good (90%): Meets performance targets
- Needs Improvement (<85%): Performance issues

**Metrics:**
- p95 response time: <200ms (API endpoints)
- Database query time: <100ms (p95)
- No N+1 queries

## Validation Process

### Step 1: Automated Checks
- Run linting and type checking
- Execute test suite
- Run security scan
- Check test coverage

### Step 2: Code Review
- Review code quality
- Check for best practices
- Verify error handling
- Assess maintainability

### Step 3: Performance Analysis
- Review performance metrics
- Check for bottlenecks
- Validate optimization

### Step 4: Decision

**PASS (≥85%):**
- Proceed to validation phase
- Document any minor issues for follow-up

**FAIL (<85%):**
- Return to development phase
- Address identified issues
- Re-validate after fixes

## Output Format

```markdown
## Development Quality Gate Results

**Status:** ✅ PASSED / ❌ FAILED
**Score:** [X]% (Threshold: 85%)

### Code Quality: [X]%
- Linting: ✅ Pass / ❌ Fail
- Type Checking: ✅ Pass / ❌ Fail
- Code Quality Score: [X]/100
- [Issues if any]

### Test Coverage: [X]%
- Unit Test Coverage: [X]% (Target: [Y]%)
- Integration Test Coverage: [X]% (Target: [Y]%)
- All Tests Passing: ✅ Yes / ❌ No
- [Issues if any]

### Security Standards: [X]%
- Security Scan: ✅ Pass / ❌ Fail
- Critical Vulnerabilities: [X]
- High Vulnerabilities: [X]
- [Issues if any]

### Performance Benchmarks: [X]%
- p95 Response Time: [X]ms (Target: <200ms)
- Database Query Time: [X]ms (Target: <100ms)
- [Issues if any]

### Issues Identified:
- [List of issues]

### Recommendations:
- [Recommendations for improvement]

### Decision:
[PASS/FAIL with justification]
```

## Integration

**Triggered By:** adaptive-orchestrator after development phase
**Validates:** Outputs from backend-architect, frontend-developer, test-automator
**Blocks:** Validation phase until passed
