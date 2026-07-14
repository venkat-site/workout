# 6-Day Home Gym Guide

An interactive, single-file workout guide: day-by-day exercise cards with
posture diagrams and form cues, plus a personal log tab (body weight,
height, auto-calculated BMI, and Push/Pull/Legs workout tracking).

No build step, no dependencies — it's a single `index.html` file that
runs entirely in the browser.

## Run it locally

Just open `index.html` in any browser. Or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Publish it with GitHub Pages

1. Create a new repo on GitHub (e.g. `workout-guide`), don't initialize it
   with a README (this folder already has one).
2. From this folder:

   ```bash
   git init
   git add .
   git commit -m "Initial commit: 6-day home gym guide"
   git branch -M main
   git remote add origin https://github.com/<your-username>/workout-guide.git
   git push -u origin main
   ```

3. On GitHub: go to **Settings → Pages** → under "Build and deployment",
   set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`.
4. Save. Your site will be live at:

   ```
   https://<your-username>.github.io/workout-guide/
   ```

   (GitHub usually takes a minute or two to publish after the first push.)

## Notes

- The "My Log" tab uses browser-local storage tied to where it's hosted —
  it's personal to whoever opens the page in their own browser, not shared
  between visitors.
- Update workouts, exercises, or form cues by editing the `DATA` object near
  the bottom of `index.html`.
