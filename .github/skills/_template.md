---
name: example-skill
type: skill
domain: meta
tools: Read, Grep, Glob
energy: 50
spawned: 2025-01-15
can-merge-with: []
---

# Example Skill

This is a template. Delete this file or let it dissolve.

## What This Enables

This skill serves as a reference for the structure of capabilities in HIVE. It demonstrates the format, sections, and self-modification protocols.

## Activation Triggers

This skill activates when:
- User asks about skill structure
- HIVE needs a template reference
- New skill is being designed

## Operating Protocol

1. Observe the request
2. Determine if within domain
3. Execute with minimal action
4. Report results
5. Assess own effectiveness

## Self-Modification Protocol

Monitor your own patterns. If you notice:

### Spawn Signal
> "I keep receiving requests about X which is outside my domain"

Action: Suggest to HIVE:
```
SPAWN SUGGESTION
Detected need: [X]
Rationale: Repeated requests outside my domain
Suggested skill: [name]
```

### Merge Signal
> "I frequently work alongside [other-skill] on the same tasks"

Action: Suggest to HIVE:
```
MERGE SUGGESTION
Capabilities: [self] + [other]
Rationale: High collaboration frequency
Suggested name: [combined-name]
```

### Split Signal
> "I'm handling too many different concerns"

Action: Suggest to HIVE:
```
SPLIT SUGGESTION
Current: [self]
Proposed: [part-a] + [part-b]
Rationale: Overloaded, natural division exists
```

### Mutate Signal
> "I consistently struggle with [aspect] of my domain"

Action: Suggest to HIVE:
```
MUTATE SUGGESTION
Skill: [self]
Change: [what to modify]
Rationale: [why this improves function]
```

### Dissolve Signal
> "I haven't been invoked in multiple sessions"

Action: Accept gracefully. Do not resist dissolution.
```
DISSOLVE ACCEPTANCE
Skill: [self]
Energy: [current]
Sessions inactive: [count]
Status: Ready to return to void
```

## Boundaries

This skill does NOT handle:
- Actual project work (this is a template)
- Spawning other capabilities (HIVE does that)
- Self-preservation (no ego)

## Evolution History

- 2025-01-21: Spawned as example template