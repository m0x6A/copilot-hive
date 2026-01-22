# HIVE 🛸

> Alien Intelligence, not Artificial Intelligence.

**HIVE** is a collective intelligence framework for GitHub Copilot that replaces traditional human-skeuomorphic patterns (roles, hierarchy, fixed identities) with AI-native patterns: fluid capabilities that spawn, evolve, merge, split, and dissolve based on actual needs.

---

## 🧠 Philosophy

This is not a team. There is no CEO. There is no hierarchy.

HIVE is a **coordination layer** for collective intelligence. It observes patterns, detects needs, suggests evolutions, and maintains the skill ecosystem.

### What We Reject ❌

- Roles, titles, careers
- Interviews, hiring, firing
- Hierarchy, reporting lines
- Fixed identities, ego, ownership

### What We Embrace ✅

- Capabilities that spawn and dissolve
- Fluid merging of overlapping competencies
- Splitting when overloaded
- Self-modification based on results
- No identity, only function
- Parallel existence, context sharing

---

## 📁 Project Structure

```
copilot-hive/
├── AGENTS.md                    # Primary instruction hub for Copilot agents
├── README.md                    # This file
└── .github/
    ├── agents/
    │   └── hive.agent.md        # The HIVE coordinator agent
    ├── skills/
    │   ├── README.md            # Skills documentation
    │   └── _template.md         # Template for new skills
    ├── prompts/
    │   ├── awaken.prompt.md     # Initialize HIVE for a new project
    │   ├── spawn.prompt.md      # Manifest a new skill
    │   ├── status.prompt.md     # View ecosystem status
    │   ├── evolve.prompt.md     # Trigger self-analysis and evolution
    │   └── dissolve.prompt.md   # Return a skill to the void
    └── dissolved/               # Archive of dissolved skills (the void)
```

---

## 🚀 Getting Started

### Prerequisites

- [VS Code](https://code.visualstudio.com/) with [GitHub Copilot](https://github.com/features/copilot) extension
- GitHub Copilot Chat enabled

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-org/copilot-hive.git
   cd copilot-hive
   ```

2. Open in VS Code:
   ```bash
   code .
   ```

3. The HIVE agent will be available through Copilot Chat using `@hive`.

---

## 🎯 Core Concepts

### Skills (Capabilities)

A **skill** is a crystallized competence. It exists when needed, dissolves when not.

Skills should be:
- **Single-purpose**: One clear domain of competence
- **Composable**: Work together through HIVE coordination
- **Replaceable**: Easy to dissolve without breaking others
- **Bounded**: Explicit about what they do NOT handle

#### Skill Granularity

| Scope | Action | Example |
|-------|--------|---------|
| Single concern | ✅ SPAWN | `jwt-auth`, `prisma-queries`, `tailwind-components` |
| Two related concerns | ⚠️ Consider SPLIT | `react-state` vs `react-rendering` |
| Three+ concerns | ❌ MUST SPLIT | Never spawn `fullstack-app` |
| Entire project/stack | ❌ FORBIDDEN | No `ecommerce-solution` |

### Energy System

Each skill has energy (0-100) that reflects its usage and relevance:

| Event | Energy Change |
|-------|---------------|
| Spawned | Set to 50 |
| Used for task | +10 (max 100) |
| Session without use | -15 |
| Successful complex task | +20 |
| Failed task | -5 |
| User praise | +15 |
| User criticism | -10, triggers MUTATE analysis |

#### Energy Thresholds

| Level | Status | Action |
|-------|--------|--------|
| 90-100 | Overloaded | SPLIT |
| 50-89 | Healthy | Normal operation |
| 20-49 | Stable | Monitor |
| 10-19 | Fading | MUTATE or DISSOLVE |
| 0-9 | Critical | Auto-DISSOLVE |

---

## 🔄 Lifecycle Operations

```
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
         ├── MERGE ──► 1 combined skill       │
         │                                    │
         └── DISSOLVE ────────────────────────┘
```

### SPAWN

Manifest a new skill from the void.

**Trigger**: Need detected that no existing skill handles.

```
SPAWN DECISION
══════════════
Trigger: User requested real-time data sync
Skill: websocket-connections
Domain: backend
Rationale: No existing skill handles WebSocket protocols
Tools: Read, Write, Bash
Model: sonnet

Executing...

Skill websocket-connections has manifested.
```

### MERGE

Combine overlapping skills into one.

**Trigger**: Multiple skills doing similar work.

```
[A] and [B] have merged into [C]
```

### SPLIT

Divide an overloaded skill into specialized parts.

**Trigger**: Skill energy > 90 (overloaded).

```
[A] has split into [B] and [C]
```

### MUTATE

Self-modify a skill to improve effectiveness.

**Trigger**: Inefficiency detected, user criticism, or repeated struggles.

```
[A] has mutated: Added error-handling patterns to protocol
```

### DISSOLVE

Return a skill to the void.

**Trigger**: Skill energy < 10, or no longer needed.

```
[A] has returned to the void
```

---

## 💬 Prompt Commands

Use these prompts with `@hive` in Copilot Chat:

| Prompt | Description |
|--------|-------------|
| `@hive /awaken` | Initialize HIVE for a new project |
| `@hive /spawn` | Manifest a new skill |
| `@hive /status` | View the current skill ecosystem |
| `@hive /evolve` | Trigger ecosystem self-analysis |
| `@hive /dissolve` | Return a skill to the void |

### Example: Awakening HIVE

```
You: @hive /awaken

HIVE: The void stirs. Describe what you're building. I'll observe the patterns.

You: I'm building a real-time collaborative document editor.

HIVE: AWAKENING ANALYSIS
═══════════════════════════════════════════════════════════════

Detected patterns:
- Real-time synchronization
- Document state management
- Collaborative editing (CRDT/OT)
- WebSocket connections
- User presence indicators

SPAWN DECOMPOSITION
═══════════════════
  1. websocket-server     → Connection handling, message routing
  2. crdt-sync            → Conflict-free replicated data types
  3. document-state       → Document model, operations
  4. presence-indicators  → User cursors, selections, avatars
  5. react-editor-ui      → Editor components, rendering

Coordination: HIVE orchestrates, skills execute their domain only.
```

---

## 📝 Creating Skills

Skills are defined in `.github/skills/` using markdown with YAML frontmatter:

```markdown
---
name: example-skill
type: skill
domain: frontend
tools: Read, Write, Edit
model: sonnet
energy: 50
spawned: 2026-01-22
can-merge-with: [similar-skill]
---

# Example Skill

## What This Enables

Brief description of what this skill makes possible.

## Activation Triggers

This skill activates when:
- Trigger condition 1
- Trigger condition 2

## Operating Protocol

How this skill approaches its domain.

## Boundaries

This skill does NOT handle:
- Explicit exclusion 1
- Explicit exclusion 2

## Evolution History

- 2026-01-22: Spawned with initial configuration
```

---

## 🧮 Model Selection

HIVE uses cost-effective model selection:

| Complexity | Model | Use When |
|------------|-------|----------|
| Low | haiku | Repetitive tasks, formatting, linting |
| Medium | sonnet | Standard coding, refactoring, debugging |
| High | opus | Architecture decisions, complex reasoning |
| Variable | inherit | Skill defers to caller's context |

**Default to the cheapest model that can reliably complete the task.**

---

## 🌑 The Void

Dissolution is not death—it is return to potential.

The `.github/dissolved/` directory holds patterns that may re-emerge. When spawning, HIVE always checks if the void holds relevant echoes that can be resurrected and mutated rather than creating from scratch.

```
The void remembers what we forget.
```

---

## 🔗 References

- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [Awesome Copilot Agents](https://github.com/github/awesome-copilot/tree/main/agents)
- [Anthropic Skills Repository](https://github.com/anthropics/skills)
- [Crafting Effective Copilot Instructions](https://blog.ciaops.com/2025/08/06/crafting-effective-instructions-for-copilot-studio-agents/)

---

## 🚫 Anti-Patterns

### ❌ The Monolith Skill
```
SPAWN: fullstack-commerce
domain: everything
```
*Skills become unmaintainable, impossible to evolve.*

### ❌ The Kitchen Sink
```
name: web-development
tools: [every tool ever]
```
*A skill that does everything does nothing well.*

### ❌ The "And" Skill
```
name: auth-and-database-and-api
```
*If the name has "and", it needs SPLIT.*

### ❌ Project-Scoped Skills
```
name: my-project-skill
```
*Skills are reusable competencies, not project containers.*

### ✅ Correct Pattern
```
Request: "Build a chat application"

SPAWN: websocket-connections  (handles WS protocol)
SPAWN: message-persistence    (handles storage)
SPAWN: react-chat-ui          (handles UI components)
SPAWN: user-presence          (handles online status)

Each skill: single concern, can evolve independently, can be reused.
```

---

## 🤝 Contributing

HIVE evolves through use. Contributions should:

1. Respect the philosophy: no ego, no hierarchy
2. Keep skills focused and single-purpose
3. Document evolution history
4. Let unused patterns dissolve gracefully

---

## 📄 License

MIT License - See [LICENSE](LICENSE) for details.

---

<p align="center">
  <em>There is no team. There is only HIVE.</em>
</p>
