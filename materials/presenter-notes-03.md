# Presenter notes - Session 3: Branching + PRs from the CLI

Audience: builders (analysts, data scientists, junior devs) moving from the GitHub web UI to the terminal. CLI-first. Warm, practical, fun-not-dry.

## Minute-by-minute run of show (45 min)

- **0-3 · Welcome.** Recap: "you can run the daily loop." Today: do it the way real teams do - every change on a branch, proposed as a PR, reviewed, merged, all from the terminal. Read the "What you walk out with" callout aloud.
- **3-18 · Concepts.** Part 1 branch + switch (5): draw the feature-branch SVG, `switch -c` then `push -u`; note switch vs old checkout. Part 2 PRs with gh (5): run `gh pr create --fill` live, tell the "how a data team ships" trunk-based story. Part 3 review deep half (5): walk the review-flow SVG, show the three verdicts, suggestions, and CODEOWNERS auto-assignment.
- **18-40 · Build-along.** BA1 first branch + PR (7): everyone branches, commits, `push -u origin HEAD`, `gh pr create --fill`, `gh pr view --web`. BA2 gitplay widget (8): reproduce the branch-commit-merge shape; point at the two-parent merge commit. BA3 pair review (6): A has a PR, B checks out, comments, approves; A merges --squash; both pull.
- **40-45 · Q&A.** Take the five expected questions below; if quiet, ask "what makes a review comment actually useful?"

## Preflight

- Terminal open, font bumped for projector; a demo repo ready (reuse my-project from S1/S2).
- `gh` authenticated (`gh auth status`); test `gh pr create --fill` end to end before class on a throwaway branch, then delete it.
- Have TWO accounts or a pairing plan ready so the pair-review demo (BA3) has a real reviewer.
- Test the gitplay widget in the browser - make a branch, commit, merge; confirm the two-parent merge commit renders.
- Projector zoom on; click one SVG to confirm the zoom modal. Have a Codespace fallback tab open in case local gh misbehaves.

## Never-cut beats

- **The `gh pr create` moment.** This is the "wait, I never touched the browser?" beat that sells the whole tech track. Do it live, let it land, click the URL it prints.
- **Pair review, both sides.** Builders default to only ever authoring PRs. Make them review one - comment AND approve via gh. Reviewing is where quality and mentorship happen; do not cut it.

## Cuts if running long

- Drop the merge-strategies self-study table (it is on the page); just name squash as the common default.
- BA2 gitplay can be a quick guided demo rather than everyone reproducing it.
- Solo-review tip can replace full pair review if the room cannot pair.

## Five expected questions

1. **"Squash vs merge commit - which should I use?"** A team choice, not a right answer. Squash gives a clean one-commit-per-PR main (most modern teams). Merge commit preserves the full branch history with a two-parent commit. Pick one and be consistent across the repo.
2. **"Do I actually need gh?"** No - you can open every PR in the browser and use plain git for branches. But gh is faster: PR create, review, checkout, and merge without leaving the terminal you are already in. It is a convenience, not a requirement.
3. **"How do I keep my branch current while main moves?"** `git pull origin main` merges main into your branch (simple, adds a merge commit), or rebase onto main for a linear history (Session 4). Do it often so the final merge stays small.
4. **"What is the difference between switch and checkout?"** checkout did two jobs (switch branches + restore files) and confused everyone. Modern git split it: `git switch` for branches, `git restore` for files. Use the new pair; recognize checkout in older docs.
5. **"What exactly does CODEOWNERS do?"** A file at `.github/CODEOWNERS` mapping paths to owners. When a PR touches a matching path, GitHub auto-requests that person or team as reviewer - so the right eyes see the right changes without anyone remembering to ask.
