# Momentum 2.1

Free, single-file, mobile-first health and habit tracker. Burnt-orange hybrid design, dark/light themes, and five bottom tabs: Home, Calories, Habits, Exercise, Progress.

## 2.1 features
- Nutrition: daily calorie and macro logs, personal searchable food library, favourite-style quick logging and saved meals
- Habits: daily check-ins, per-habit weekly schedules, 14-day calendar and streaks
- Exercise: goal logging, workout sessions, timed sets, best daily totals and workout history
- Progress: 7/14-day nutrition chart, 30-day activity overview, optional weight/reflection logs, 1–5 hunger/energy/mood/sleep check-ins, six achievement milestones
- Local browser storage, editable goals, JSON export/import, dark/light toggle

## Deploy
GitHub Settings → Pages → Deploy from branch → main → /(root). No build tools, subscriptions or third-party APIs.

## Data and privacy
The application retains the `momentum.v2` storage key and extends records with new optional fields; existing records remain in place. Backups are plain-text JSON and contain personal data: store them privately and never commit them to this public repository. Browser storage is not encrypted and can be lost if site data is cleared. Import replaces local records only after confirmation. Back up before upgrading or switching devices.

## Verification
JavaScript syntax checked after the 2.1 update. Full interactive browser testing and Pages deployment verification are still required. Suggested checks: all five tabs, light/dark persistence, saved food search and logging, habit schedule/streaks, workout sessions and timed sets, progress analytics, wellbeing check-ins, achievements, backup export and restore, narrow mobile screens.

Default calorie and exercise references are illustrative, not medical advice.