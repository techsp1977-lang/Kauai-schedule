# Kauai Urgent Care schedule site

- `index.html` holds the page design (CSS, login, rendering code). Edit it for any design change, then commit and push to `main`.
- `schedule.json` holds the schedule data. It is overwritten every ~30 minutes by the Apps Script on the "Makana Master schedule" Google Sheet. Never hand-edit it; changes come from the sheet.
- The page loads `schedule.json` at runtime (`{lastUpdated, years}`), so design changes and data syncs never collide.
- Before pushing, `git fetch origin main && git rebase origin/main`, since the sync commits often.
- Label column: `.thl` (header) / `.tdl` (row labels). Shift labels must stay on one line.
