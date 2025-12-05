---
name: validation-quality-gate
description: Final quality gate for validation phase. Ensures code review completion, all tests passing, documentation completeness, and deployment readiness.
threshold: 95%
applies_to: complex-tasks
---

# Validation Quality Gate

**Purpose**: Final validation before considering task complete. Ensures all quality standards are met and system is ready for deployment.

**Threshold**: 95% compliance required

**Applies To**: Complex tasks only (Level 3)

## Validation Criteria

### 1. Code Review Completion (25%)

**Checklist:**
- [ ] Code review completed
- [ ] All review comments addressed
- [ ] Code follows best practices
- [ ] Architecture consistency verified
- [ ] No technical debt introduced
- [ ] Code is production-ready

**Scoring:**
- Complete (100%): All review items addressed
- Mostly Complete (90%): Minor items remaining
- Needs Work (<90%): Significant issues

### 2. Test Suite Status (25%)

**Checklist:**
- [ ] All unit tests passing
- [ ] All integration tests passing
- [ ] All E2E tests passing (if applicable)
- [ ] Performance tests passing
- [ ] Security tests passing
- [ ] No flaky tests

**Scoring:**
- All Passing (100%): 100% test pass rate
- Mostly Passing (95%): <5% failure rate
- Needs Fix (<95%): Significant test failures

**Metrics:**
- Test pass rate: 100%
- Flaky test rate: <1%

### 3. Documentation Completeness (25%)

**Checklist:**
- [ ] API documentation complete
- [ ] Code comments added where needed
- [ ] README updated
- [ ] Architecture documentation updated
- [ ] Deployment guide created (if applicable)
- [ ] Changelog updated

**Scoring:**
- Complete (100%): All documentation present and accurate
- Mostly Complete (90%): Minor gaps
- Needs Work (<90%): Significant documentation gaps

### 4. Deployment Readiness (25%)

**Checklist:**
- [ ] Environment variables documented
- [ ] Database migrations tested
- [ ] Deployment scripts verified
- [ ] Rollback procedure tested
- [ ] Monitoring configured
- [ ] Error tracking configured
- [ ] Performance monitoring set up

**Scoring:**
- Ready (100%): Fully ready for deployment
- Mostly Ready (90%): Minor items remaining
- Not Ready (<90%): Significant gaps

## Validation Process

### Step 1: Automated Validation
- Run full test suite
- Check documentation completeness
- Verify deployment readiness checks

### Step 2: Manual Review
- Code review verification
- Documentation quality check
- Deployment readiness assessment

### Step 3: Final Assessment
- Compile all validation results
- Calculate overall score
- Make final decision

### Step 4: Decision

**PASS (≥95%):**
- Task marked as complete
- Ready for deployment
- Document any minor follow-up items

**FAIL (<95%):**
- Return to appropriate phase
- Address identified issues
- Re-validate after fixes

## Output Format

```markdown
## Validation Quality Gate Results

**Status:** ✅ PASSED / ❌ FAILED
**Score:** [X]% (Threshold: 95%)

### Code Review Completion: [X]%
- Code Review: ✅ Complete / ❌ Incomplete
- Review Comments Addressed: [X]/[Y]
- [Issues if any]

### Test Suite Status: [X]%
- Unit Tests: [X]% passing
- Integration Tests: [X]% passing
- E2E Tests: [X]% passing
- Overall Pass Rate: [X]%
- [Issues if any]

### Documentation Completeness: [X]%
- API Documentation: ✅ Complete / ❌ Incomplete
- Code Comments: ✅ Adequate / ❌ Needs Work
- README: ✅ Updated / ❌ Outdated
- [Issues if any]

### Deployment Readiness: [X]%
- Environment Config: ✅ Ready / ❌ Not Ready
- Migrations: ✅ Tested / ❌ Untested
- Monitoring: ✅ Configured / ❌ Missing
- [Issues if any]

### Issues Identified:
- [List of issues]

### Recommendations:
- [Recommendations]

### Decision:
[PASS/FAIL with justification]

### Next Steps:
[If PASS: Deployment instructions]
[If FAIL: Remediation steps]
```

## Integration

**Triggered By:** adaptive-orchestrator after validation phase
**Validates:** Outputs from code-reviewer, test-automator, security-auditor, quality-validator
**Final Gate:** Last checkpoint before task completion
