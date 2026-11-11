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

## Momentum 3.0 Challenge HQ
- Access Challenge HQ from Home or Daily Habits; the original five bottom-navigation pages remain intact.
- Existing push-up exercise totals in `exerciseLogs` remain the source of truth. New set entries are recorded in `pushupSets` and update the same daily total.
- Monthly target: 3,000 push-ups; daily goal: 100. Animated ring, milestones, calendar, past-day corrections, undo/remove individual sets and a configurable rest timer.
- Forecast uses average reps over elapsed calendar days multiplied by days in the month. Remaining daily pace uses remaining days including today. Predictions are estimates.
- Custom challenges and logs are saved locally as `customChallenges` and `challengeLogs` in the existing `momentum.v2` JSON object; backup/export includes them.
- The new UI is implemented in `challenges.js` with no external dependencies or API calls.
- Suggested acceptance checks: log a set in Challenge HQ and verify Daily Habits/Exercise totals; correct a previous date and verify monthly totals; navigate between months; create/log/delete a custom challenge; start/stop a rest timer; export/import JSON and verify preserved history; reload and switch themes.
- JavaScript syntax validated; automated browser acceptance testing has not yet been completed.


## Momentum 3.1 — Daily Experience
- Home opens with a daily 100 push-up mission, quick-set buttons and monthly 3,000-rep progress.
- Workout Mode is available from the Home mission: quick/custom sets, optional live rest timer, elapsed session timer, undo individual sets, and finish-session history. The timer runs while the page is open; session state is not persisted across reloads.
- Daily Habits includes one-tap habit check-ins and optional numeric targets, saved in `habitTargets` and `habitAmounts`. Existing habit logs remain intact.
- Progress History adds personal records from the last 180 days, 7-day comparisons and current 100-rep streak.
- PWA manifest and service worker cache the application shell for offline reopening after a successful online load. iOS: Safari → Share → Add to Home Screen. SVG is the current icon; a PNG Apple Touch icon would improve compatibility.
- All user data remains in browser-local storage and JSON export; installing the app does not back up data. Preserve exports before clearing website storage.
- Verification: JavaScript syntax and repository integration checked. Full browser regression, iOS install and offline testing still need manual confirmation.
