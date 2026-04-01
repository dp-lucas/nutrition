# Nutrition — Hybrid Athlete Body Recomposition

A self-contained knowledge base for an ongoing nutritionist-patient relationship managed through Cursor AI.

## Goals

- Body recomposition (build muscle, lose fat)
- Hybrid athletic performance (lifting + running)
- Nutrition periodized to a 12-week training program (2026-03-29 to 2026-06-21)

## How It Works

Open this project in Cursor and ask questions. The AI acts as an expert sports nutritionist with full context of the patient's profile, training program, and dietary guidelines. All consultations, meal plans, food logs, and progress entries are persisted as Markdown files.

## Structure

| Path | Purpose |
|------|---------|
| `profile.md` | Patient demographics, body composition, preferences |
| `guidelines.md` | Macro targets, calorie cycling, meal timing, supplements |
| `training-context.md` | 12-week training program summary |
| `docs/` | Architecture docs and research references |
| `meal-plans/` | Daily/weekly meal plans |
| `food-log/` | Daily food intake logs |
| `recipes/` | Individual recipe files |
| `progress/` | Body composition and performance tracking |

## Conventions

- Dated files use `YYYY-MM-DD.md` format.
- Each tracking folder has a `_template.md` for consistent entries.
- All paths are relative to the project root.
