# Presenter notes - Session 1 · Git under the hood

## Preflight (5 min before)
- Open courses/01-git-under-the-hood.html, Projector zoom 125%.
- Have a real terminal visible (big font) AND a Codespace open in a tab as the zero-install fallback.
- Test the gitplay widget once (commit, branch, commit, switch, merge - confirm the two-parent merge draws).
- Have an empty scratch folder ready to git init live.
- Confirm `git --version` and `gh --version` both work on your machine.

## Run of show
- 0-3 · Welcome. Ask: "who has used the GitHub website but never the terminal?" - that is exactly the graduation this track is for. Name the running artifact (my-project) they build across all six.
- 3-8 · Part 1 the model. This is THE session-maker. Draw the snapshot chain on the whiteboard even with the SVG up. Hammer: commit = snapshot, branch = pointer, HEAD = you. Do not let anyone leave thinking git stores diffs.
- 8-13 · Part 2 setup. Fast. Local install OR Codespace - show the Codespace `.` trick live, it wins the room every time. The three config lines, then move on.
- 13-18 · Part 3 first commits. Type it live in the scratch folder, narrating which zone each command touches. Run `git status` between every step - model the habit.
- 18-24 · Build-along 1 setup. Circulate. The two blockers: install fighting (send them to Codespaces immediately, do not debug installs for 10 min) and identity config typos.
- 24-33 · Build-along 2 first commits. Everyone types their own three commits. Watch for add-then-edit confusion - it is the teachable moment for the staging snapshot idea.
- 33-40 · Build-along 3 gitplay. Let them play freely 2 min, then call out: "the merge commit has two parent lines - that is what you will create for real in Session 3."
- 40-45 · Q&A + quiz. Q1 (snapshot not diff) is the one that matters - reinforce.

## Never cut
- The snapshot-not-diff model (Part 1) - everything downstream depends on it.
- The Codespace `.` demo - it is the unblock-anyone escape hatch, and it is delightful.
- gitplay's two-parent merge callout - it pre-loads Sessions 3 and 4.

## Cut if long
- Part 3 self-study remote/push card - point at it, Session 2 owns push.
- Build-along 2's extra two files - one commit is enough to feel the loop.
- The gh auth self-study card - only matters for local users, Codespace users skip it.

## Expected questions
- "Do I have to use the terminal? The website worked fine." - The website is the non-tech track and it is great. The terminal is faster, scriptable, and where CI/automation live. This track is the graduation.
- "git vs GitHub again?" - git = the local engine (this session). GitHub = the hosting + collaboration layer (Sessions 3+). gh = GitHub's CLI.
- "I am on a locked-down work laptop, cannot install." - Codespaces. Browser terminal, nothing to install, git + gh pre-configured.
- "What is the difference between add and commit really?" - add stages a snapshot (guest list); commit freezes it into history. The three-zone model card.
- "Is my Codespace free?" - Generous free monthly hours for individuals; more than enough for this course.
