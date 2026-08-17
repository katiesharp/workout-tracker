# Workout Trackers 🏋️

Simple, personalized workout tracker pages. Check off exercises as you go — progress is saved in your browser (localStorage), and every workout is logged to a history list by date. No build step, no dependencies.

## Pages

Live at **https://katiesharp.github.io/workout-tracker/** — a landing page linking to each person's tracker:

- **Katie** — https://katiesharp.github.io/workout-tracker/katie/ — Hiking Strength Program
- **Elyse** — https://katiesharp.github.io/workout-tracker/elyse/ — personalized program coming soon (placeholder for now)

Each page keeps its own history under its own localStorage key, so they never collide even on the same device.

## Katie's program

Two ~50–60 minute sessions per week:

- **Day 1 — Strength + Climbing:** Leg Press, Dumbbell Step-Ups, Single-Leg Elevated Hip Thrust + Band, Step-Downs, Hip Abduction Machine, 15 min Incline Treadmill
- **Day 2 — Strength + Endurance:** Leg Press, Step-Downs, Dumbbell Step-Ups, Single-Leg Elevated Hip Thrust + Band, Seated Leg Curl, 15 min Incline Treadmill

Tap any exercise name to expand its description and progression tips.

## Adding or editing a program

Each person's page is a self-contained `index.html` in their folder. Edit the `WORKOUTS` object near the top of the `<script>` block — each day has a `label` and a list of exercises with `name`, `scheme`, and `desc`.

To add a new person: copy an existing folder (e.g. `elyse/`), update the name in the page title/header/manifest, change `STORAGE_KEY` to something unique (e.g. `workout-log-sam-v1`), and add a link on the root `index.html`.

## On your iPhone

Open your page (not the landing page), then use *Share → Add to Home Screen* (iPhone) or *menu → Add to Home screen* (Android). It installs like an app with its own icon and launches full-screen straight to your tracker.

Notes:
- Check-off state is stored per date, so each day starts fresh automatically.
- History shows past sessions with a completion badge.
- Data lives in your browser's localStorage, so use the same browser/device to keep your history.
