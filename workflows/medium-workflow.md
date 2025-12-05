# Medium Workflow

**Complexity**: 4-6  
**Agents**: 2-3 (planner + specialist + reviewer)  
**Tokens**: 30K-80K  
**Time**: 5-15 minutes  
**Gates**: 1 (basic review)

## Execution Flow

```yaml
workflow:
  phase_1_planning:
    - task-planner: Create execution plan
      - Break down task into subtasks
      - Identify dependencies
      - Estimate effort
  
  phase_2_execution:
    - specialist-agent(s): Implement solution
      - Backend: backend-developer
      - Frontend: frontend-developer
      - Fullstack: both
  
  phase_3_review:
    - code-reviewer: Basic review
      - Check code quality
      - Verify best practices
      - Gate: basic_review (threshold: 80%)
      - Pass → Complete
      - Fail → Fix issues → Re-review
```

## Example

**Task**: "Add user profile picture upload feature"

**Execution**:
1. **Planning**: task-planner creates plan
   - Backend: API endpoint for upload
   - Frontend: Upload component
   - Storage: File storage integration

2. **Execution**: 
   - backend-developer: Implements upload API
   - frontend-developer: Implements upload UI

3. **Review**: code-reviewer reviews code
   - Score: 85/100 → Pass
   - Complete

## When to Use

- Multiple files/components
- Some dependencies
- Minor architecture considerations
- Requires planning
- New features
- Module refactoring
