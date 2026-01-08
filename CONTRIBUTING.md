# Contributing Guide

This document outlines the conventions and workflows used in this project.

## Project Structure

```
backyard-drum-studio/
├── README.md                    # Project overview
├── CONTRIBUTING.md              # This file
├── CHANGELOG.md                 # Progress log
├── master-plan.md               # High-level phase tracking
├── glossary.md                  # Construction terminology
│
├── specs/                       # Phase specifications
│   ├── 00-project-setup/        # Meta: how this project works
│   ├── 01-planning-permits/     # Planning and permits phase
│   └── _templates/              # Templates for new phases
│
├── designs/                     # Design files
│   └── models/                  # SketchUp files
│
├── images/                      # Progress photos
│
└── .kiro/
    └── steering/                # AI steering files
```

## Spec-Driven Development

Each phase of the build follows a spec-driven approach with three documents:

1. **requirements.md** - The "what" and "why"
   - Goals and constraints
   - Code/permit requirements
   - Acceptance criteria
   - Reasoning behind decisions

2. **design.md** - The "how"
   - Specific materials and methods
   - Measurements and specifications
   - Links to design files (SketchUp, PDFs)

3. **tasks.md** - The execution checklist
   - Granular steps to complete the phase
   - Status tracking (not started, in progress, completed)
   - Start/completion dates

4. **materials.md** - Budget and materials tracking
   - Materials list with quantities
   - Costs and suppliers
   - Tools required

## Task Status Format

Tasks use checkbox notation:

```markdown
- [ ] Not started
- [-] In progress
- [x] Completed
```

With optional metadata:

```markdown
- [x] 1.1 Mark out foundation footprint
  - _Started: 2026-01-10_
  - _Completed: 2026-01-15_
  - _Notes: Used string lines and batter boards_
```

## Commit Conventions

This project adapts the [Conventional Commits](https://www.conventionalcommits.org/) format specifically for this project:

### Commit Types

| Type | Use Case | Example |
|------|----------|---------|
| `spec` | Creating or modifying specs | `spec(foundation): add requirements for concrete slab` |
| `work` | Construction progress updates | `work(foundation): complete rebar installation` |
| `docs` | Project documentation, README | `docs: add commit conventions to CONTRIBUTING.md` |
| `media` | Adding photos, videos, design files | `media(foundation): add rebar inspection photos` |
| `chore` | Project maintenance, reorganization | `chore: reorganize image folders` |

### Commit Message Format

```
type(scope): brief description

- Detail bullet points
- Reference task numbers when applicable
- Note any deviations from plan
```

### Commit Separation Rules

- **Spec changes** = standalone commit (never mix with work updates)
- **Work updates** = standalone commit
- **Media** = can bundle multiple related photos
- **Budget** = standalone or with related work update

## Photo Conventions

### Naming Format

```
YYYY-MM-DD-description.jpg
```

Examples:
- `2026-01-15-foundation-rebar-grid.jpg`
- `2026-01-15-foundation-inspection-passed.jpg`

### Organization

Photos are organized by phase:

```
images/
├── foundation/
│   ├── 2026-01-10-site-marked.jpg
│   └── 2026-01-15-rebar-complete.jpg
├── framing/
└── ...
```

## Creating a New Phase Spec

1. Copy the template folder: `specs/_templates/phase-spec/`
2. Rename to match the phase: `specs/XX-phase-name/`
3. Fill in requirements.md first
4. Complete design.md once requirements are clear
5. Break down into tasks.md
6. Add materials.md with budget estimates

## AI Workflow

This project uses AI assistance (Kiro) for documentation updates:

- AI makes commits locally following conventional commit format
- AI does NOT push without explicit permission
- User controls when changes go to GitHub

### Typical Session

1. User reports work completed verbally
2. AI updates task status in tasks.md
3. AI updates CHANGELOG.md
4. AI stages and commits changes
5. User reviews and pushes when ready
