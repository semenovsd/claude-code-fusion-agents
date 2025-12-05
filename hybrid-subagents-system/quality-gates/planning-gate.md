---
name: planning-quality-gate
description: Quality gate for planning phase validation. Ensures requirements completeness, architecture feasibility, and task breakdown adequacy before proceeding to development.
threshold: 95%
applies_to: complex-tasks
---

# Planning Quality Gate

**Purpose**: Validate that planning phase deliverables meet quality standards before proceeding to development phase.

**Threshold**: 95% compliance required

**Applies To**: Complex tasks only (Level 3)

## Validation Criteria

### 1. Requirements Completeness (25%)

**Checklist:**
- [ ] All functional requirements documented
- [ ] Non-functional requirements specified
- [ ] User stories created with acceptance criteria
- [ ] Stakeholders identified
- [ ] Constraints documented
- [ ] Assumptions listed
- [ ] Out of scope clearly defined

**Scoring:**
- Complete (100%): All items checked
- Good (90%): 1-2 items missing
- Needs Improvement (<90%): Multiple items missing

### 2. Architecture Feasibility (25%)

**Checklist:**
- [ ] System architecture designed
- [ ] Technology stack selected with rationale
- [ ] API contracts defined
- [ ] Database schema designed
- [ ] Scalability approach defined
- [ ] Security considerations addressed
- [ ] Integration points identified

**Scoring:**
- Feasible (100%): Architecture is sound and implementable
- Mostly Feasible (90%): Minor concerns
- Needs Review (<90%): Significant concerns

### 3. Task Breakdown Adequacy (25%)

**Checklist:**
- [ ] Tasks broken down into 4-8 hour chunks
- [ ] Dependencies identified
- [ ] Critical path determined
- [ ] Parallel work opportunities identified
- [ ] Acceptance criteria defined for each task
- [ ] Effort estimates provided
- [ ] Risk factors identified

**Scoring:**
- Adequate (100%): Tasks are actionable and well-defined
- Mostly Adequate (90%): Some tasks need clarification
- Needs Improvement (<90%): Tasks are too vague or large

### 4. Risk Mitigation Coverage (25%)

**Checklist:**
- [ ] Technical risks identified
- [ ] Mitigation strategies defined
- [ ] Contingency plans created
- [ ] Risk monitoring approach defined
- [ ] Critical risks addressed

**Scoring:**
- Comprehensive (100%): All major risks addressed
- Good (90%): Most risks addressed
- Needs Improvement (<90%): Significant risks unaddressed

## Validation Process

### Step 1: Automated Checklist Review
- Run through all checklist items
- Calculate compliance percentage
- Identify missing items

### Step 2: Technical Feasibility Review
- Review architecture for technical soundness
- Validate technology choices
- Check for potential issues

### Step 3: Completeness Assessment
- Ensure all required artifacts present
- Verify quality of documentation
- Check for gaps

### Step 4: Decision

**PASS (≥95%):**
- Proceed to development phase
- Document any minor gaps for follow-up

**FAIL (<95%):**
- Return to planning phase
- Address identified gaps
- Re-validate after fixes

## Output Format

```markdown
## Planning Quality Gate Results

**Status:** ✅ PASSED / ❌ FAILED
**Score:** [X]% (Threshold: 95%)

### Requirements Completeness: [X]%
- [Status of each item]

### Architecture Feasibility: [X]%
- [Status of each item]

### Task Breakdown Adequacy: [X]%
- [Status of each item]

### Risk Mitigation Coverage: [X]%
- [Status of each item]

### Issues Identified:
- [List of issues if any]

### Recommendations:
- [Recommendations for improvement]

### Decision:
[PASS/FAIL with justification]
```

## Integration

**Triggered By:** adaptive-orchestrator after planning phase
**Validates:** Outputs from requirements-analyst, technical-planner, backend-architect
**Blocks:** Development phase until passed
