# Complex Workflow

**Complexity**: 7-9  
**Agents**: 5-7 (full team)  
**Tokens**: 100K-300K  
**Time**: 15-45 minutes  
**Gates**: 3 (planning, development, validation)

## Execution Flow

```yaml
workflow:
  phase_1_planning:
    - requirements-analyzer: Analyze requirements
      - Extract functional requirements
      - Identify non-functional requirements
      - Create user stories
    
    - backend-architect: Design backend architecture
      - System design
      - API contracts
      - Database schema
    
    - frontend-architect: Design frontend architecture (if needed)
      - Component structure
      - State management
      - Routing
    
    - gate_1: planning_validation (threshold: 95%)
      - Pass → Continue to development
      - Fail → Refine planning → Re-gate
  
  phase_2_development:
    - backend-developer: Implement backend
      - API endpoints
      - Business logic
      - Database integration
    
    - frontend-developer: Implement frontend (if needed)
      - Components
      - API integration
      - State management
    
    - test-automator: Write tests
      - Unit tests
      - Integration tests
      - E2E tests (if needed)
    
    - gate_2: development_validation (threshold: 85%)
      - Pass → Continue to validation
      - Fail → Fix issues → Re-gate
  
  phase_3_validation:
    - code-reviewer: Comprehensive review
      - Code quality
      - Best practices
      - Security
      - Performance
    
    - spec-validator: Final validation
      - Requirements coverage
      - Production readiness
    
    - gate_3: production_readiness (threshold: 95%)
      - Pass → Complete
      - Fail → Fix issues → Re-gate
```

## Example

**Task**: "Implement microservices architecture for user management"

**Execution**:
1. **Planning Phase**:
   - requirements-analyzer: Analyzes requirements
   - backend-architect: Designs microservices architecture
   - Gate 1: 96/100 → Pass

2. **Development Phase**:
   - backend-developer: Implements user-service, auth-service
   - test-automator: Writes comprehensive tests
   - Gate 2: 88/100 → Pass

3. **Validation Phase**:
   - code-reviewer: Reviews all code
   - spec-validator: Validates against requirements
   - Gate 3: 92/100 → Pass
   - Complete

## When to Use

- Multiple modules/services
- Significant dependencies
- Architecture changes
- Requires comprehensive planning
- New services/APIs
- Major refactoring
- Full-stack features
