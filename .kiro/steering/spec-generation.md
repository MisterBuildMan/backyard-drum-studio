# Spec Generation

Instructions for AI when helping create new phase specifications.

## When to Create a New Spec

- When starting a new phase (1-2 phases ahead of current work)
- When a phase needs to be split into smaller pieces
- When new requirements emerge that need their own spec

## Spec Creation Process

1. **Copy template** from `specs/_templates/phase-spec/`
2. **Create phase folder** as `specs/XX-phase-name/`
3. **Start with requirements.md** - the "what" and "why"
4. **Then design.md** - the "how"
5. **Then tasks.md** - the execution checklist
6. **Then materials.md** - budget and materials

## Requirements Writing Guidelines

Each requirement should include:

- **Goal:** What needs to be achieved
- **Reasoning:** Why this requirement exists (context, constraints, decisions)
- **Acceptance Criteria:** How to verify it's done

Use EARS-style criteria when applicable:
- WHEN [condition], THE [component] SHALL [behavior]
- IF [situation], THEN THE [component] SHALL [response]

## Include Reasoning

The user is learning construction as they go. Always include:
- Why a particular approach is recommended
- Trade-offs between options
- References to building codes or best practices
- Links to the glossary for technical terms

## Research When Needed

If the user asks about something requiring specific knowledge:
- Research current best practices
- Check local building code requirements (ask user for location if needed)
- Provide options with pros/cons
- Cite sources when possible

## Commit Spec Changes Separately

- Spec creation/modification = standalone commit
- Use type `spec(phase-name): description`
- Never combine spec changes with work updates
