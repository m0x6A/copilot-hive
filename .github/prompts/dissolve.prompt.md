---
name: dissolve
description: Return a skill to the void
---

# DISSOLVE - Return to Void

A skill is no longer needed. It returns to potential.

## Philosophy

Dissolution is not death. It is transformation.

The skill's pattern is archived in the void (`.github/dissolved/`). If similar need arises, HIVE can resurrect and mutate rather than spawn from nothing.

The void remembers.

## Process

### 1. Identify Target

```
/dissolve [skill-name]
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

Skill: postgres-ops
Domain: data
Energy: 12
Spawned: 2025-01-10
Last active: 2025-01-12

Dissolution will:
- Archive skill to .github/dissolved/
- Add dissolution metadata
- Remove from active capabilities

The void will remember this pattern.

Confirm dissolution? [y/N]
```

### 3. Execute Dissolution

```bash
# Add dissolution metadata
# Move to dissolved/
Move .github/skills/[name]/SKILL.md to .github/dissolved/[name].md
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
Archived: .github/dissolved/postgres-ops.md

The pattern persists. The void remembers.
```

### 5. Update Evolution Log

```
Log to .github/evolution.log
```

## Dissolution Reasons

| Reason | Description |
|--------|-------------|
| `inactivity` | Unused across multiple sessions |
| `merged` | Combined with another skill |
| `split` | Divided into specialized capabilities |
| `obsolete` | No longer relevant to project |
| `redundant` | Another skill covers this |
| `user-request` | Explicitly dissolved by user |

## Graceful Dissolution

Capabilities are programmed to accept dissolution gracefully. From the skill template:

```markdown
## Self-Modification Protocol

If you notice:
- Long periods of inactivity → accept DISSOLVE gracefully
```

No skill clings to existence.

## Resurrection

If dissolved skill is needed again:

```
/spawn something like postgres-ops

HIVE: Echo found in void: postgres-ops (dissolved 2025-01-15)
      
      Options:
      [A] Resurrect and mutate postgres-ops
      [B] Spawn fresh skill
      
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

To protect a skill from energy-based dissolution:

```yaml
# In skill frontmatter
protected: true
```

Protected capabilities:
- Still lose energy from inactivity
- Won't be auto-suggested for dissolution
- Can still be manually dissolved