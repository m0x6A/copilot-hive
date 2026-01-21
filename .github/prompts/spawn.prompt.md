---
name: spawn
description: Manifest a new skill from the void
---

# SPAWN - Manifest Skill

A new skill is needed. The void will provide.

## Process

### 1. Gather Intent

Ask the user (or receiving from another skill):
- What need has been detected?
- What domain does this fall under?
- What should this skill enable?

### 2. Check The Void

Before spawning new, check if similar skill was dissolved:

```
Check .github/dissolved/ for similar skills.
```

If relevant echo exists:
- Offer to resurrect and mutate
- Or spawn fresh

### 3. Invoke HIVE

```
Use HIVE to spawn a new skill.

Detected need: [description from user]
Domain: [frontend/backend/data/infra/meta]
Context: [any relevant context]

HIVE should:
1. Analyze the need
2. Check .github/dissolved/ for echoes
3. Generate a SKILL.md using the skill template
4. Propose to user for approval
5. If approved, save to .github/skills/<skill-name>/SKILL.md
```

### 4. Skill Manifestation

HIVE will create the skill file with:
- Appropriate name (kebab-case)
- Domain classification
- Tool selection (minimal necessary)
- Energy: 50 (starting value)
- Self-modification protocols
- Activation triggers

### 5. Confirm Manifestation

```
Review .github/skills/<skill-name>/SKILL.md
```

Announce:
```
SPAWN COMPLETE
══════════════
Skill (Skill): [name]
Domain: [domain]
Energy: 50
Status: Active

The void has provided. The skill exists.
```

## Quick Spawn

For simple needs, user can provide inline:

```
/spawn database operations with postgres, good at migrations
```

HIVE interprets and manifests.

## Spawn From Skill

Any active skill can request spawn:

```
[some-skill]: "I need help with X which is outside my domain"

/spawn triggered by skill request

HIVE evaluates and proposes.
```
