# 🎓 StudyPilot
 
A personal academic dashboard that turns your subjects, course outlines, and exam dates into a day-by-day study plan — built as a single, self-contained web app with no backend required.
 
**Live demo / preview:** celebrated-griffin-594de7.netlify.app
 
---
 
## What it does
 
StudyPilot takes a few things you already know about your semester — your subjects, your target grades, your syllabus, your exam dates — and turns them into something actionable every day:
 
- **Dashboard** — a daily checklist of what to study today, your progress percentage, a personalized recommendation, and a countdown to your next exam.
- **Subjects** — each subject shows how far it is from its target, color-coded by priority (high / medium / low).
- **Course outline** — paste your full syllabus (one topic per line) or add topics one at a time, and check them off as you cover them.
- **Study plan generator** — click "Prepare me a study plan" and it spreads your remaining outline topics evenly across the days left until that subject's exam (or a 7-day default if no exam is set yet). That plan then feeds directly into your daily dashboard checklist.
- **Exams** — add quizzes, assignments, midterms, and finals per subject; each shows a color-coded countdown (red = close, amber = soon, teal = plenty of time).
- **Study session timer** — start/pause/complete a focused session per subject; completed sessions log your study time and build your streak.
- **Progress** — GPA-to-target progress, a subject performance breakdown, and a 7-day study-time chart.
- **Streak & badges** — tracks consecutive study days and unlocks a few badges for consistency.
## Tech stack
 
- Plain **HTML, CSS, and vanilla JavaScript** — no framework, no build step, no dependencies to install.
- **Google Fonts** (Baloo 2, Space Grotesk, Inter) loaded via CDN for the display type.
- **`localStorage`** for saving your data in your own browser — no backend, no database, no account needed.
Because it's one self-contained `index.html` file, it can be opened directly in a browser or hosted anywhere that serves static files.
 
## Getting started
 
### Run it locally
Just open `index.html` in any modern browser — that's it.
 
### Host it for free with GitHub Pages
1. Upload `index.html` to this repository (root folder).
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to "Deploy from a branch," choose branch `main` and folder `/root`.
4. Save — GitHub will give you a live link like `https://yourusername.github.io/studypilot/`.
## How your data is stored
 
All data (profile, subjects, outlines, exams, sessions, streaks) is saved locally in **your own browser** via `localStorage`. This means:
 
- Nothing is sent to a server — it's fully private to your device.
- Data isn't shared between different people visiting the hosted link; each visitor sees their own empty dashboard until they set it up.
- Clearing your browser data, or switching browsers/devices, will reset your progress. There's a **Reset all progress** option in Settings if you want to start over intentionally.
## Using the course outline & study plan feature
 
1. Go to **Subjects → [pick a subject] → Course outline**.
2. Paste your syllabus into the textarea (one topic per line) and click **Load outline**, or add topics individually.
3. Optionally, go to the **Exams** tab and add that subject's midterm or final date — the plan will pace itself against it.
4. Back on the subject card, click **✨ Prepare me a study plan**. It splits your remaining topics across the available days and shows a day-by-day breakdown.
5. Each day's assigned topics automatically appear on your **Dashboard** as that day's tasks.
## Customizing
 
Everything lives in one file, so it's straightforward to tweak:
 
- Colors and fonts are defined as CSS variables near the top of the `<style>` block.
- Study plan pacing logic lives in the `generatePrepPlan()` function.
- Task/recommendation rules live in `ensureTodayTasks()` and `priorityOf()`.
## License
 
Add a license of your choice (MIT is a common pick for personal projects like this).
 
