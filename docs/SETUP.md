# Setup Guide

Complete guide for setting up the Hybrid Subagents System in Claude Code.

## Prerequisites

- Claude Code installed and configured
- Access to MCP servers (context7, sequential-thinking)
- Basic understanding of Claude Code subagents

## Step 1: Install Agents

### Option A: Copy All Agents

```bash
# Copy entire agents directory to Claude Code subagents location
cp -r agents/ ~/.cursor/subagents/
```

### Option B: Selective Installation

Copy only the agents you need:

```bash
# Core orchestration (required)
cp agents/orchestration/* ~/.cursor/subagents/orchestration/

# Planning agents (for complex+ tasks)
cp agents/planning/* ~/.cursor/subagents/planning/

# Development agents (required)
cp agents/development/**/* ~/.cursor/subagents/development/

# Quality agents (for medium+ tasks)
cp agents/quality/* ~/.cursor/subagents/quality/

# Validation agents (for complex+ tasks)
cp agents/validation/* ~/.cursor/subagents/validation/
```

## Step 2: Configure MCP Servers

### Context7 Setup

Context7 is used for framework/library documentation. Configure in your MCP settings:

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@context7/mcp-server"],
      "env": {
        "CONTEXT7_API_KEY": "your-api-key"
      }
    }
  }
}
```

### Sequential Thinking Setup

Sequential Thinking is used for complex reasoning. Configure in your MCP settings:

```json
{
  "mcpServers": {
    "sequential-thinking": {
      "command": "npx",
      "args": ["-y", "@sequential-thinking/mcp-server"]
    }
  }
}
```

## Step 3: Install Slash Command

Copy the slash command to Claude Code commands directory:

```bash
cp commands/smart-dev.md ~/.cursor/commands/smart-dev.md
```

## Step 4: Verify Installation

1. Open Claude Code
2. Check that agents are available in subagents list
3. Test `/smart-dev` command
4. Verify MCP servers are connected

## Step 5: Test Simple Task

Try a simple task to verify basic functionality:

```
/smart-dev Fix typo in README.md
```

Expected: Direct call to appropriate agent, quick completion.

## Step 6: Test Complex Task

Try a complex task to verify full pipeline:

```
/smart-dev Implement user authentication system with JWT
```

Expected: Full pipeline with planning, development, validation phases.

## Troubleshooting

### Agents Not Found

- Verify agents are in correct directory
- Check file permissions
- Restart Claude Code

### MCP Servers Not Working

- Verify MCP server configuration
- Check API keys (for context7)
- Review MCP server logs

### Workflow Not Selected Correctly

- Check complexity analysis output
- Verify workflow selector configuration
- Review agent team builder logs

## Next Steps

- Read [USAGE.md](USAGE.md) for usage guide
- Review [ARCHITECTURE.md](ARCHITECTURE.md) for architecture details
- Check [BEST_PRACTICES.md](BEST_PRACTICES.md) for best practices
