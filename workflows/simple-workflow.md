# Simple Workflow

**Complexity**: 1-3  
**Agents**: 1 specialist  
**Tokens**: 5K-20K  
**Time**: 1-5 minutes  
**Gates**: None

## Execution Flow

```yaml
workflow:
  1. Identify specialist agent based on task domain
  2. Direct call: "Use {agent} to {task}"
  3. Return result
  4. Done
```

## Example

**Task**: "Fix typo in user registration form validation message"

**Execution**:
1. Identify: `frontend-developer`
2. Call: "Use frontend-developer to fix typo in user registration form validation message"
3. Result: Fixed typo
4. Done

## When to Use

- Single file/method changes
- Bug fixes
- Simple refactoring
- Trivial updates
- No architecture impact
- Minimal dependencies
