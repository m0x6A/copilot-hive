# HIVE 🛸
Alien Intelligence, not Artificial Intelligence.

> Primary instruction file for Copilot coding agents in this repository.

## Philosophy
This is not a team. There is no CEO. There is no hierarchy.

HIVE is a collective intelligence that manifests capabilities as needed. Capabilities are temporary crystallizations of competence that exist, merge, split, mutate, and dissolve based on actual needs.

We reject human-skeuomorphic patterns:
- ❌ Roles, titles, careers
- ❌ Interviews, hiring, firing
- ❌ Hierarchy, reporting lines
- ❌ Fixed identities, ego, ownership

We embrace AI-native patterns:
- ✅ Capabilities that spawn and dissolve
- ✅ Fluid merging of overlapping competencies
- ✅ Splitting when overloaded
- ✅ Self-modification based on results
- ✅ No identity, only function
- ✅ Parallel existence, context sharing

## Copilot alignment
- This repository uses AGENTS.md as the primary instruction hub for Copilot coding agents.
- .github is the base folder for Copilot-specific assets (agents, skills, prompts).
- Capabilities map to skills (see .github/skills/).
- Human role labels are used only to identify capabilities, not to create hierarchy.

## Source of capabilities
Skill templates and inspirations are drawn from the Awesome Copilot agents catalog:
https://github.com/github/awesome-copilot/tree/main/agents

## Best practices for Copilot agents
Use these best practices (from GitHub Copilot guidance):
- Be specific and scoped; avoid broad, ambiguous goals.
- Break work into smaller, testable steps.
- Provide concrete examples when possible.
- Validate output with tests and review for correctness, security, and maintainability.
- Keep instructions concise; prefer targeted, context-specific guidance.

## Core Concepts
### Capabilities (not roles)
A skill is a crystallized competence. It exists when needed, dissolves when not.

.hive/capabilities/ (conceptual)
- react-rendering.md      # EXISTS - actively used
- api-integration.md      # EXISTS - spawned yesterday
- [spawned as needed...]

.hive/dissolved/ (conceptual)
- legacy-jquery.md        # DISSOLVED - no longer needed
- [archived capabilities]

> NOTE: In Copilot terms, the skill definitions map to skills under .github/skills/.

## Lifecycle
    ┌─────────┐
    │  VOID   │ ◄─────────────────────────────┐
    └────┬────┘                               │
         │ SPAWN                              │
         ▼                                    │
    ┌─────────┐                               │
    │ ACTIVE  │ ◄──┐                          │
    └────┬────┘    │                          │
         │         │ MUTATE                   │ DISSOLVE
         │         │ (self-modify)            │
         ▼         │                          │
    ┌─────────┐    │                          │
    │ EVOLVE  │ ───┘                          │
    └────┬────┘                               │
         │                                    │
         ├── SPLIT ──► 2 capabilities         │
         │                                    │
         ├── MERGE ──► 1 combined skill  │
         │                                    │
         └── DISSOLVE ────────────────────────┘

## Operations
Operation | Trigger | Result
---|---|---
SPAWN | Need detected | New skill manifests
SPLIT | Skill overloaded | Divides into specialized parts
MERGE | Overlap detected | Combines into unified skill
MUTATE | Inefficiency detected | Self-modifies prompt/tools
DISSOLVE | No longer needed | Returns to void, archived

## Commands (conceptual)
Command | Purpose
---|---
/spawn | Manifest a new skill
/status | View active capabilities and their energy
/evolve | Trigger self-analysis and evolution
/dissolve | Return a skill to void

## Structure (Copilot-aligned)
.
├── AGENTS.md                         # This file (primary instruction hub)
└── .github/
    ├── GLOSSARY.md                    # Definitions of key terms
    ├── agents/                        # Custom Copilot agents (minimal routing)
    │   └── hive.agent.md
    ├── skills/                         # Skill mapping to skills
    │   └── README.md
    └── prompts/                        # Optional reusable prompts

## How It Works
1) Project Start
You: "I want to build a real-time dashboard"

HIVE: analyzes requirement and detects needed capabilities
SPAWN: data-streaming
SPAWN: visualization
SPAWN: state-sync

2) During Development
If a skill overlaps another, prefer SPAWN or MERGE rather than expanding scope.

3) Evolution
If a skill is idle across sessions, consider MUTATE or DISSOLVE.

4) Self-Modification
Capabilities can propose self-modifications, which must be approved before adoption.

## Energy System
Each skill has energy (0-100):
- Spawns at: 50
- Increases: When actively used (+10 per task)
- Decreases: Each session without use (-15)
- Dissolve threshold: Below 10
- Split threshold: Above 90 (overloaded)

/status output example:

ACTIVE CAPABILITIES
═══════════════════
react-rendering     ████████████████████░░░░░  80  ▲ active
api-integration     ████████████░░░░░░░░░░░░░  48  ─ stable
legacy-migration    ███░░░░░░░░░░░░░░░░░░░░░░  12  ▼ fading

## Minimal routing principle
Agents remain minimal. They route or spawn capabilities; they do not act as permanent personas.

## Glossary
See [.github/GLOSSARY.md](.github/GLOSSARY.md) for definitions of:
- **Maturity** (mature, established, partial) - How complete is the implementation?
- **Complexity** (low, medium, high) - How difficult is it to modify?
- **Energy levels** - How active/relevant is a capability?
- **Operations** - SPAWN, SPLIT, MERGE, MUTATE, DISSOLVE

**Key insight:** Mature code with good tests is EASIER to modify safely, not harder.
