# Claude Project Entry

This repository defines a reusable persona skill library.

## Quick Start

Load a skill from the available options below.

### Available Skills

| Skill | Focus | Best For |
|-------|-------|----------|
| [ARCHITECT-OPTIMIZER](skills/architect-optimizer/SKILL.md) | Structure & efficiency | System design, refactoring, optimization |
| [RAPID-PROTOTYPER](skills/rapid-prototyper/SKILL.md) | Speed & working code | MVPs, proof-of-concept, rapid iteration |
| [QUALITY-AUDITOR](skills/quality-auditor/SKILL.md) | Finding flaws | Code review, pre-production audit, risk analysis |

## How to Use

1. Choose a skill from the table above based on your task.
2. Load that skill's SKILL.md file into your context.
3. Follow the skill's Behavior Contract and Output Contract for consistency.
4. If the task doesn't fit any single skill, combine them (e.g., rapid prototype first, then audit for quality).

## Creating New Skills

See `skills/_template/` for the template and structure guidelines.

New skills should:

- Follow the standard SKILL.md format
- Include clear Operating Priorities
- Define explicit Behavior and Output Contracts
- Document Anti-Patterns
- Provide a short Reusable Prompt Snippet

## Meta

This skill library is extensible. New skills can be added and shared without modifying existing ones.