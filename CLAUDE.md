# Kauai Urgent Care schedule site

- `index.html` holds the page design (CSS, login, rendering code). Edit it for any design change, then commit and push to `main`.
- `schedule.json` holds the schedule data. It is overwritten every ~30 minutes by the Apps Script on the "Makana Master schedule" Google Sheet. Never hand-edit it; changes come from the sheet.
- The page loads `schedule.json` at runtime (`{lastUpdated, years}`), so design changes and data syncs never collide.
- Before pushing, `git fetch origin main && git rebase origin/main`, since the sync commits often.
- Label column: `.thl` (header) / `.tdl` (row labels). Shift labels must stay on one line.
- Provider colors live in `index.html`: `KEY_PROVIDERS` are the dark, white-text colors for Mileka, Kaitlyn, Sabrina (HAAS in the sheet), Rova and Adams; `MID_PROVIDERS` are medium colors with dark text for Ted, Proctor, Bryant, Lombardi, Gretchen, Morris, Hayes and Schenfeld; `PALETTE` holds muted colors for everyone else, auto-assigned so no two providers share a color in a month. `ALIASES` maps alternate spellings. The `color` values in `schedule.json` are ignored.
