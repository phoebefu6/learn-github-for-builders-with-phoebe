# learn-github-for-builders-with-phoebe - course map (tech track)

Audience: **builders** - analysts, data scientists, junior devs, anyone graduating from the GitHub web UI to the real terminal + GitHub workflow. Assumes comfort with a code editor; assumes NO prior git.
Sibling: learn-github-with-phoebe (non-tech, browser-only, published). This track picks up its explicit "not covered by design" list.
Format: 6 sessions x 45 min (3 welcome / ~15 concepts / ~22 build-along / 5 Q&A).
Running artifact: **one project repo driven entirely from the CLI** - initialized S1, daily-looped S2, branched + PR'd S3, conflict-resolved S4, CI'd S5, released + protected + deployed S6.
Zero-install path: GitHub Codespaces (browser terminal) for anyone who cannot install locally - called out every session.
Design: same GitHub Primer palette as the non-tech track (ink #24292F / deep #1B1F23, green #2DA44E, soft #86D9A3, tint #DAFBE1, link blue #0969DA, flagship merged-PR purple #8250DF, terminal bg #0D1117).

## Official GitHub Skills mapping (fetched via `gh api orgs/skills/repos`)

| Skills course | Covered in | Depth |
|---|---|---|
| introduction-to-git | S1 + S2 | ✓ full working content (CLI) |
| review-pull-requests (deep half) | S3 | ✓ CLI + gh PR flow, CODEOWNERS |
| resolve-merge-conflicts | S4 | ✓ full |
| hello-github-actions | S5 | ✓ author a workflow |
| test-with-actions | S5 | ✓ CI lint+test on PR |
| workflow-artifacts | S5 | ◐ mentioned |
| reusable-workflows | S5 | ◐ mentioned |
| code-with-codespaces | S1 | ◐ the zero-install path |
| Copilot / CodeQL / secret-scanning courses | not covered | ✗ AI + security literacy courses |

## Session map

| # | Title | Diff | Core content | Widget |
|---|-------|------|--------------|--------|
| 1 | Git under the hood | 🟢 | what git is (snapshots + movable pointers, NOT diffs); install + `git config` (or Codespaces zero-install); `git init` / `clone`; the first commits: `status`, `add`, `commit -m`, `log`, `diff`; HEAD + the working-tree/staging/repo three-zone model | gitplay: commit-graph simulator |
| 2 | The daily loop | 🟢 | `status → add → commit → push/pull` rhythm; remotes + `origin`; `.gitignore`; commit-message hygiene (conventional-ish); the undo toolbox in safe tiers: `restore` (discard working), `revert` (safe public undo), `reset` (rewrite local only) | sorter: which undo do you reach for |
| 3 | Branching + PRs from the CLI | 🟡 | `branch` / `switch -c` / `push -u`; PRs via `gh pr create`; trunk-based vs git-flow-lite; the review deep half: `gh pr review`, request changes, suggestions, CODEOWNERS, draft PRs; keeping a branch current | gitplay: branch scenarios |
| 4 | Merge conflicts without fear | 🟡 | why conflicts happen (two edits, same lines); reading `<<<<<<< ======= >>>>>>>` markers; resolve in editor; merge vs rebase intuition + when-to-use each; `stash` and `cherry-pick` as surgical tools | sorter: rebase or merge? |
| 5 | Actions authoring | 🟠 | YAML anatomy (on / jobs / steps / uses / run); write real CI: lint + test on every PR; the marketplace + `uses:`; secrets; artifacts; reading a failed run's logs; matrix builds (mention) | checklist: CI-ready |
| 6 | Ship like a professional | 🟠 | tags + `gh release` + semver; changelogs; branch protection rules (require review + green CI); deploy Pages via an Actions workflow; the professional-repo checklist; graduation + what is next | checklist: professional-repo scorecard |

## Widgets

gitplay (NEW - clickable commit graph, S1 + S3) · sorter (S2 undo, S4 rebase/merge) · checklist (S5 CI-ready, S6 pro-repo). Terminal code-along uses the .termbox CSS (cmd/out/cmt spans), not a widget.

## Not covered by design

GUI git clients (GitHub Desktop, editor integrations) beyond a mention; Copilot / AI pair-programming (AI literacy course); CodeQL / secret-scanning / supply-chain security (a future security course); language-specific CI beyond a generic lint+test; monorepo tooling; git internals plumbing (cat-file, packfiles). Say so on Session 6 + index.
