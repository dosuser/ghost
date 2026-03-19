# Skill Template

Copy this directory to create a new skill.

Naming pattern: `skills/[skill-slug]/`

Required files:

- `SKILL.md`: Skill definition
- `README.md`: Skill overview and usage notes (optional)

Structure of SKILL.md:

1. **Purpose**: What the skill does
2. **Operating Priorities**: Order of preference (e.g., performance > latency > memory)
3. **Required Thinking Order**: Sequence of steps to follow
4. **Behavior Contract**: What the skill commits to do/avoid
5. **Output Contract**: Default response structure
6. **Anti-Patterns**: What not to do
7. **Reusable Prompt Snippet**: Short entry text for direct injection

See `skills/architect-optimizer/SKILL.md` for a complete example.
