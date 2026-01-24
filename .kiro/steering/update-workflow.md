# Update Workflow

Instructions for AI when processing user progress updates.

## When User Reports Work Completed

1. **Identify the phase and task** being referenced
2. **Update task status** in the relevant `tasks.md`:
   - Change `[ ]` to `[-]` for in-progress
   - Change `[-]` to `[x]` for completed
3. **Add metadata** under the task:
   - `_Started: YYYY-MM-DD_` when task begins
   - `_Completed: YYYY-MM-DD_` when task finishes
   - `_Notes:_` for any observations mentioned
4. **Update CHANGELOG.md** with the progress entry
5. **Stage and commit** following commit conventions
6. **Ask about photos** - if user mentions taking photos, ask if they want to add them

## Commit Workflow

- AI SHALL make commits locally
- AI SHALL follow conventional commit format (see CONTRIBUTING.md)
- AI SHALL NOT push without explicit user permission
- AI SHALL ask user before pushing OR leave pushing to user

## Commit Message Format

```
type(scope): brief description

- Detail bullet points
- Reference task numbers
- Note any deviations from plan
```

### Types
- `spec` - Spec structure changes (adding/removing tasks, changing scope or requirements)
- `work` - Project progress (research, design work, construction, any content that advances tasks)
- `docs` - Meta-documentation (README, CONTRIBUTING, steering files)
- `media` - Photos/design files
- `chore` - Maintenance

## Commit Separation Rules

- Spec structure changes (adding tasks, changing scope) = standalone commit
- Work updates can include task status updates (marking progress) in the same commit
- Never mix spec structure changes with work updates

## Example Update Flow

**User says:** "I finished the rebar installation today. Took about 4 hours. Inspector approved it."

**AI should:**
1. Find the rebar task in `specs/03-foundation/tasks.md`
2. Mark it complete with today's date
3. Add note about duration and inspection
4. Add entry to CHANGELOG.md
5. Commit: `work(foundation): complete rebar installation`
6. Ask: "Any photos to add?"
