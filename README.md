# SheetMaster Practice Lab

A browser-based adaptive Google Sheets + Warehouse Data Operator training system.

## Features
- Bengali-first teaching with English formulas and menu names
- 9-level roadmap from absolute beginner to job-readiness
- Adaptive question selection based on weak skills and recent mistakes
- Mastery states: Not Started, Learning, Practicing, Proficient, Mastered
- Difficulty progression: Easy, Medium, Hard, Expert, Real-world
- Progressive 3-step hints
- Randomized formula and warehouse questions
- Realistic inventory datasets and CSV export for practicing in Google Sheets
- 20–500 row warehouse work simulations
- Interview simulator with local heuristic scoring and professional answer models
- Timed exams
- XP, streak, accuracy, weak-topic detection and localStorage persistence
- Responsive GitHub Pages-compatible UI

## Run locally
Because the app is plain HTML/CSS/JavaScript, you can open `index.html` directly in most modern browsers.
For the most reliable behavior, run a tiny local server:

```bash
python -m http.server 8080
```

Then open `http://localhost:8080`.

## GitHub Pages
1. Create a new GitHub repository.
2. Upload the contents of this folder to the repository root.
3. Go to **Settings → Pages**.
4. Set Source to **Deploy from a branch**.
5. Select `main` branch and `/ (root)`.
6. Save. GitHub will publish the site.

## Training logic
A skill is not marked Mastered after one correct answer. Mastery requires:
- mastery score >= 88
- at least 8 attempts
- at least 80% recent accuracy
- correct work across at least 3 difficulty levels

Wrong answers reduce mastery and increase the probability that the adaptive engine selects that topic again.

## Recommended next upgrades
- Editable spreadsheet grid with cell-selection tasks
- Formula parser that accepts more equivalent formulas
- Larger scenario library (inbound, picking, packing, returns/RTO, cycle count)
- IndexedDB dataset history
- Optional Google account sync / backend
- Apps Script automation track
- Voice-based interview practice
- Import user CSV and generate tasks from it
