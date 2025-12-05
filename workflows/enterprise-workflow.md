# Enterprise Workflow

**Complexity**: 10  
**Agents**: 7+ (full team + specialists)  
**Tokens**: 300K-1M+  
**Time**: 45+ minutes  
**Gates**: 4 (all gates + iterative refinement)

## Execution Flow

```yaml
workflow:
  iteration_1_planning:
    - requirements-analyzer: Deep requirements analysis
      - Comprehensive requirement extraction
      - Business requirement analysis
      - Technical requirement analysis
    
    - business-analyst: Business requirements
      - Business logic definition
      - Business rules
      - Business constraints
    
    - backend-architect: System architecture
      - Complete system design
      - Service architecture
      - Data architecture
    
    - frontend-architect: UI/UX architecture (if needed)
      - Complete UI architecture
      - UX flow design
      - Component architecture
    
    - gate_1: planning_completeness (threshold: 95%)
      - Pass → Continue to development
      - Fail → Iterate planning → Re-gate
  
  iteration_2_development:
    - backend-developer: Backend implementation
      - Complete backend implementation
      - All services
      - All APIs
    
    - frontend-developer: Frontend implementation (if needed)
      - Complete frontend implementation
      - All components
      - All pages
    
    - test-automator: Comprehensive testing
      - Full test suite
      - Unit, integration, E2E tests
      - Performance tests
    
    - gate_2: development_quality (threshold: 85%)
      - Pass → Continue to optimization
      - Fail → Iterate development → Re-gate
  
  iteration_3_optimization:
    - security-auditor: Security audit
      - Security review
      - Vulnerability assessment
      - Security best practices
    
    - performance-engineer: Performance optimization
      - Performance profiling
      - Bottleneck identification
      - Optimization implementation
    
    - gate_3: security_performance (threshold: 90%)
      - Pass → Continue to validation
      - Fail → Iterate optimization → Re-gate
  
  iteration_4_validation:
    - code-reviewer: Final review
      - Comprehensive code review
      - Architecture review
      - Best practices validation
    
    - spec-reviewer: Specification review
      - Requirements coverage
      - Architecture compliance
    
    - spec-validator: Production validation
      - Production readiness check
      - Deployment readiness
      - Documentation completeness
    
    - gate_4: production_readiness (threshold: 95%)
      - Pass → Complete
      - Fail → Iterate validation → Re-gate
```

## Example

**Task**: "Build new e-commerce platform"

**Execution**:
1. **Iteration 1 - Planning**:
   - requirements-analyzer: Comprehensive analysis
   - business-analyst: Business requirements
   - backend-architect: System architecture
   - frontend-architect: UI architecture
   - Gate 1: 96/100 → Pass

2. **Iteration 2 - Development**:
   - backend-developer: Complete backend
   - frontend-developer: Complete frontend
   - test-automator: Full test suite
   - Gate 2: 87/100 → Pass

3. **Iteration 3 - Optimization**:
   - security-auditor: Security audit
   - performance-engineer: Performance optimization
   - Gate 3: 92/100 → Pass

4. **Iteration 4 - Validation**:
   - code-reviewer: Final review
   - spec-reviewer: Specification review
   - spec-validator: Production validation
   - Gate 4: 96/100 → Pass
   - Complete

## When to Use

- System-wide changes
- Multiple services
- Complex architecture
- Requires iterative refinement
- New system development
- Major architecture overhaul
- Large-scale migration
- Enterprise feature set
