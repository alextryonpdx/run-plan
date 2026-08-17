# Get Moving — Run Timer

A run/walk interval timer for iPhone, built around a 12-week progressive running plan. Runs as a website — no App Store install needed.

## Setting it up on your iPhone

1. Open this repo's GitHub Pages link in **Safari** (must be Safari, not Chrome — Add to Home Screen only works from Safari on iOS).
2. Tap the **Share** icon (square with an arrow) at the bottom of the screen.
3. Scroll down and tap **Add to Home Screen**.
4. Tap **Add**. An app icon now appears on your Home Screen and launches full-screen, just like a regular app.

If you ever change the code and push updates, remove the Home Screen icon and re-add it — iOS caches the page and icon from the first time you added it.

## Using the app

**1. Pick your week and day.**
On the setup screen, choose which week (1–12) and which day (Day 1, 2, or 3) of the plan you're running. A preview shows the jog/walk intervals for that session and the total time.

- Day 1 and Day 3 are the harder sessions.
- Day 2 is an easier/recovery pace.

**2. Enable audio.**
Before starting, tap the audio status pill (shows "Tap to enable audio"). This is required once per session — iOS blocks sound that isn't triggered by a direct tap. Once it turns green ("Audio on"), you're set. Tap it anytime to replay a test cue.

**3. Choose an audio mode.**
- **Beeps** — a double-beep at 30 seconds left in each interval, plus single beeps in the final 3 seconds and at every jog/walk transition.
- **Voice** — a spoken "Two minutes left" warning, plus a spoken announcement at the start of every segment (e.g. *"Jog for 7 minutes"*).

You can switch between the two modes at any time, including mid-run.

**4. Start Run, then hit Play.**
The countdown ring shows time remaining in the current interval. The "Up next" card previews what's coming. Reset restarts the current day from the beginning.

## A few things to know

- **Keep your phone screen on/face-up during a run.** The app can't run in the background with the screen off — that's an iOS restriction on web apps, not something fixable in code. The app requests a screen wake lock automatically when you hit Play so your phone won't auto-lock mid-run, but if you manually lock it or switch apps, the timer and audio pause until you come back.
- If audio ever goes silent mid-run (can happen if iOS suspends the tab), the audio status pill will turn red again — tap it to re-enable.

## Repo structure

```
index.html          — the app (GitHub Pages serves this as the site root)
files/
  apple-touch-icon.png  — iOS Home Screen icon (180×180)
  favicon-32.png         — browser tab icon
  icon-512.png            — larger icon, for reference/other platforms
  icon.svg                 — source vector for the icon
```

## Hosting

This is a static site — GitHub Pages works out of the box. In the repo's **Settings → Pages**, set the source to "Deploy from a branch," pick your main branch and the `/root` folder. Note: GitHub Pages on a **private** repo requires GitHub Pro/Team/Enterprise; on the free tier, Pages only publishes from public repos.
