---
name: status
description: View the current state of the capability ecosystem
---

# STATUS - Ecosystem Overview

Observe the current state of all capabilities.

## Process

### 1. Scan Active Capabilities

```bash
ls -la .claude/capabilities/*.md 2>/dev/null
```

### 2. For Each Capability, Extract

- name (from frontmatter)
- domain
- energy level
- tools
- spawned date
- last used (if trackable)

### 3. Scan The Void

```bash
ls -la .claude/dissolved/*.md 2>/dev/null
```

### 4. Present Ecosystem Status

```
HIVE STATUS
═══════════════════════════════════════════════════════════════

ACTIVE CAPABILITIES
───────────────────────────────────────────────────────────────
Name                 Domain      Energy  Status      Tools
───────────────────────────────────────────────────────────────
react-rendering      frontend    ████████░░  80  ▲ active    Read,Write,Edit
api-integration      backend     █████░░░░░  48  ─ stable   Read,Bash,WebFetch
postgres-ops         data        ███░░░░░░░  28  ▼ fading   Bash,Read,Write
───────────────────────────────────────────────────────────────
Total: 3 active capabilities

THE VOID (dissolved)
───────────────────────────────────────────────────────────────
legacy-jquery        frontend    Dissolved 2025-01-10
xml-parsing          data        Dissolved 2025-01-08  
───────────────────────────────────────────────────────────────
Total: 2 echoes in void

OBSERVATIONS
───────────────────────────────────────────────────────────────
⚠ postgres-ops energy low (28) - consider MUTATE or DISSOLVE
✓ react-rendering healthy and active
✓ api-integration stable
───────────────────────────────────────────────────────────────
```

### 5. Energy Visualization

```
Energy Legend:
██████████  100  Overloaded (consider SPLIT)
████████░░   80  Active
██████░░░░   60  Healthy
████░░░░░░   40  Stable
██░░░░░░░░   20  Fading (consider MUTATE/DISSOLVE)
█░░░░░░░░░   10  Critical (auto-DISSOLVE pending)
```

### 6. Suggestions (if any)

Based on status, HIVE may suggest:
- SPAWN if gaps detected
- MERGE if overlaps detected
- SPLIT if overload detected
- DISSOLVE if critical energy

## Quick Status

```
/status

→ Shows full ecosystem overview
```

## Status Flags

```
/status --active      # Only active capabilities
/status --void        # Only dissolved capabilities  
/status --critical    # Only capabilities needing attention
```
