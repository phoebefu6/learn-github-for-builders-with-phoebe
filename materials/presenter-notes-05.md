# Presenter notes - Session 5: Actions authoring

**Goal of the hour:** move them from reading robots (non-tech track) to writing one. They should leave with a real `ci.yml` on a PR that they watched go red then green, and the reflex to open a failed run and read the log.

## Preflight (do before they arrive)
- Have a repo with a trivial test ready to run (a single passing `npm test` or `pytest`), so the green path is instant and believable.
- Open the **Actions tab** of that repo in a browser tab, projector-ready. You will live-refresh it a lot.
- Projector zoom ON; terminal large and high-contrast.
- Test both widgets: the checklist toggles and the verdict updates as you tick rows.
- Pre-stage the failing command so the red run is fast - know exactly which line you will break (`exit 1` or `npm run nonsense`).
- Codespace fallback tab open (press `.` on the repo) for anyone who cannot author locally.
- Have Settings → Secrets open in a tab so the secrets beat is a real screen, not a slide.

## Minute-by-minute
- **0-3 Welcome.** Callback to the non-tech track: "you learned to read the green check. Today you write it."
- **3-8 Part 1 - YAML anatomy.** Walk the SVG outer-to-inner: on / jobs / steps / uses+run. Show the hello.yml termbox. Say "spaces, never tabs" now - it saves a support question later.
- **8-13 Part 2 - real CI.** The ci.yml termbox. Read the five-step recipe. Land the "works on my machine dies here" line on the clean-runner step.
- **13-18 Part 3 - secrets, artifacts, failures.** Secrets on a real Settings screen. Then the failure-reading move: Actions tab → red run → expand failed step → bottom-up.
- **18-28 Build-along 1.** Everyone authors ci.yml, opens a PR, watches green, breaks it to red, fixes to green. The core loop.
- **28-34 Build-along 2.** Checklist widget. Let the score sting a little - the unticked rows are their homework.
- **34-40 Build-along 3.** Break-and-read drill. This is the transferable skill; do not skip.
- **40-45 Q&A.**

## Never cut
- **The red-to-green CI moment on a real PR (Build-along 1).** This is the session. Seeing their own check go red then green is what makes CI real.
- **Reading the failed log (Build-along 3).** The durable skill is diagnosis, not YAML recall. Make them find the error line themselves.

## Cut if running long
- The Python self-study card - point at it, note "same shape, different setup line."
- The triggers self-study card (workflow_dispatch, cron, reusable) - homework.
- Artifacts can shrink to a single sentence if secrets ran long.

## Five expected questions
1. **"My workflow errors before it even runs anything - YAML problem?"** Almost always whitespace: YAML is spaces, never tabs, and indentation is the structure. Re-indent with spaces and check alignment.
2. **"Is Actions free? Will this cost me?"** Public repos get unlimited free minutes. Private repos have a monthly free quota, then it is metered - fine for learning, watch it at scale.
3. **"Where do secrets actually go?"** Settings → Secrets and variables → Actions. Never in the YAML - a committed token is leaked the instant you push.
4. **"My step failed but I can't tell why."** Expand the failed step, read the log bottom-up. The real error is usually the last line before the non-zero exit.
5. **"Do I need to know every action on the marketplace?"** No - learn the shape (checkout, setup, install, lint, test) and look up specific actions when you need them. `actions/checkout` and `actions/setup-*` cover most days.
