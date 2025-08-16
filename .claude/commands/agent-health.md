---
command: agent-health
description: ❤️‍🩹 Check health of dynamic agents. Params: [module] --report
---

# Agent Health Check Command

Delegates health analysis of dynamic agents to the specialized `agent-health-monitor` agent to avoid context pollution.

## Usage

### Check All Dynamic Agents
```
/agent-health
```

### Check Specific Module
```
/agent-health api            # Checks api-agent
/agent-health payment        # Checks payment-agent
```

### Generate Report Only (no scanning)
```
/agent-health --report       # Shows table with all agents status
/agent-health api --report   # Shows report for specific agent
```

## How It Works

This command simply invokes the `agent-health-monitor` agent with the Task tool, passing your parameters:

1. **Delegates to specialist agent** - Preserves your context window
2. **Agent loads project context** - Reads CLAUDE.md and previous analysis
3. **Performs delta analysis** - Compares with last health check
4. **Returns summary** - You get the results without context pollution

## What Gets Analyzed

- **ONLY dynamic agents** (project-specific like `api-agent`, `auth-agent`)
- **NOT global agents** (engineer-*, coordinator-*, specialist-*)
- **Delta changes** since last analysis (not from scratch)

## Example Output

When you run `/agent-health`, the agent-health-monitor will return something like:

```
Dynamic Agents Health Summary
============================
Project: Laravel API (3 dynamic agents found)

✅ auth-agent: Healthy (drift: 5)
⚠️ api-agent: Degraded (drift: 45) - 12 new files detected
🔴 payment-agent: Critical (drift: 72) - Needs immediate upgrade

Recommendation: Run /agent-health payment-agent --upgrade
```

## Memory Locations

Results are stored in:
- `.claude/memory/health/` - Analysis results and history
- `.claude/memory/metrics/` - Performance and usage stats

## Implementation Note

This command is lightweight - it just calls:
```
Use Task tool to invoke agent-health-monitor with parameters
```

The heavy lifting is done by the specialist agent, keeping your main context clean.

---

_This health system ensures all dynamic agents maintain accurate, up-to-date knowledge of their modules._
