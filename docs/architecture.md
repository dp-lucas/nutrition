# Architecture

## Overview

This project is a Markdown-based knowledge base — not an application. It stores all nutrition context for a hybrid athlete pursuing body recomposition. The AI (Cursor) acts as an expert nutritionist with persistent memory via these files.

## Directory Layout

```
nutrition/
├── .cursorrules              # AI role definition and behavior rules
├── README.md                 # Project overview
├── profile.md                # Patient intake data
├── guidelines.md             # Active nutrition protocol
├── training-context.md       # 12-week training program reference
├── docs/
│   ├── architecture.md       # This file
│   └── references.md         # Research citations
├── meal-plans/
│   ├── _template.md          # Meal plan entry template
│   └── YYYY-MM-DD.md         # Dated meal plans
├── food-log/
│   ├── _template.md          # Food log entry template
│   └── YYYY-MM-DD.md         # Dated food logs
├── recipes/
│   └── recipe-name.md        # Individual recipes
└── progress/
    ├── _template.md          # Progress entry template
    └── YYYY-MM-DD.md         # Dated progress entries
```

## File Conventions

- **Dated files:** `YYYY-MM-DD.md` format, one file per day when entries are created.
- **Templates:** Each tracking folder contains `_template.md`. Copy this structure when creating new entries.
- **Recipes:** Named with kebab-case slugs (e.g., `high-protein-overnight-oats.md`).
- **References:** All citations go in `docs/references.md` with numbered entries.

## Key Files

### `.cursorrules`
Loaded automatically by Cursor on every conversation. Defines the AI's role, references context files, and enforces project isolation.

### `profile.md`
The patient intake form. Updated when body composition or circumstances change. The AI reads this before giving any personalized advice.

### `guidelines.md`
The active nutrition protocol. Contains calorie targets, macro splits by day type, meal timing, hydration, and supplement stack. Updated as the patient progresses.

### `training-context.md`
A snapshot of the 12-week training program. The AI uses today's date to determine the current phase, week, and day type. This file is read-only — training changes are made in the workout project, then reflected here.

## Portability

This project is fully self-contained. Move the entire `nutrition/` folder to any machine with Cursor and everything works — no global dependencies, no external state.
