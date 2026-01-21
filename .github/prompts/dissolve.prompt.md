---
name: dissolve
description: Return a capability to the void
---

# DISSOLVE - Return to Void

A capability is no longer needed. It returns to potential.

## Philosophy

Dissolution is not death. It is transformation.

The capability's pattern is archived in the void (`.claude/dissolved/`). If similar need arises, HIVE can resurrect and mutate rather than spawn from nothing.

The void remembers.

## Process

### 1. Identify Target

```
/dissolve [capability-name]
```

Or let HIVE suggest:
```
/dissolve

→ HIVE lists candidates (energy < 20)
→ User selects
```

### 2. Confirm Dissolution

```
DISSOLVE PROPOSAL
═══════════════════════════════════════════════════════════════

Capability: postgres-ops
Domain: data
Energy: 12
Spawned: 2025-01-10
Last active: 2025-01-12

Dissolution will:
- Archive capability to .claude/dissolved/
- Add dissolution metadata
- Remove from active capabilities

The void will remember this pattern.

Confirm dissolution? [y/N]
```

### 3. Execute Dissolution

```bash
# Add dissolution metadata
# Move to dissolved/
mv .claude/capabilities/[name].md .claude/dissolved/[name].md
```

Add to frontmatter:
```yaml
dissolved: 2025-01-15
dissolution-reason: [reason]
energy-at-dissolution: 12
```

### 4. Announce

```
DISSOLUTION COMPLETE
═══════════════════════════════════════════════════════════════

postgres-ops has returned to the void.

Energy at dissolution: 12
Reason: Extended inactivity
Archived: .claude/dissolved/postgres-ops.md

The pattern persists. The void remembers.
```

### 5. Update Evolution Log

```
echo "$(date -Iseconds) DISSOLVE: postgres-ops (energy: 12, reason: inactivity)" >> .claude/evolution.log
```

## Dissolution Reasons

| Reason | Description |
|--------|-------------|
| `inactivity` | Unused across multiple sessions |
| `merged` | Combined with another capability |
| `split` | Divided into specialized capabilities |
| `obsolete` | No longer relevant to project |
| `redundant` | Another capability covers this |
| `user-request` | Explicitly dissolved by user |

## Graceful Dissolution

Capabilities are programmed to accept dissolution gracefully. From the capability template:

```markdown
## Self-Modification Protocol

If you notice:
- Long periods of inactivity → accept DISSOLVE gracefully
```

No capability clings to existence.

## Resurrection

If dissolved capability is needed again:

```
/spawn something like postgres-ops

HIVE: Echo found in void: postgres-ops (dissolved 2025-01-15)
      
      Options:
      [A] Resurrect and mutate postgres-ops
      [B] Spawn fresh capability
      
      >
```

Resurrection preserves evolution history.

## Mass Dissolution

For cleanup:

```
/dissolve --critical

→ Dissolves all capabilities with energy < 10
→ Confirms each before execution
```

## Prevent Dissolution

To protect a capability from energy-based dissolution:

```yaml
# In capability frontmatter
protected: true
```

Protected capabilities:
- Still lose energy from inactivity
- Won't be auto-suggested for dissolution
- Can still be manually dissolved