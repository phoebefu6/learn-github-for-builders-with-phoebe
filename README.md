<!-- phoebe header -->

[![Open the live course](https://img.shields.io/badge/%E2%96%B6%20open%20the%20live%20course-1f6feb?style=for-the-badge)](https://phoebefu6.github.io/learn-github-for-builders-with-phoebe/)
[![Star this repo](https://img.shields.io/github/stars/phoebefu6/learn-github-for-builders-with-phoebe?style=for-the-badge&label=star%20this%20repo&color=444444)](https://github.com/phoebefu6/learn-github-for-builders-with-phoebe/stargazers)
[![Free courses](https://img.shields.io/badge/dynamic/json?url=https%3A%2F%2Fphoebefu6.github.io%2Flearn-with-phoebe%2Fstats.json&query=%24.courses_live&label=free%20courses&style=for-the-badge&color=111111)](https://phoebefu6.github.io/learn-with-phoebe/)

### ▶︎ [Open the live course →](https://phoebefu6.github.io/learn-github-for-builders-with-phoebe/)

Free, runs in your browser. No install, no login.

> 📚 Part of **[Learn with Phoebe](https://phoebefu6.github.io/learn-with-phoebe/)** - free, hands-on courses on AI, data, and the craft around them. **[Browse every course ↗](https://phoebefu6.github.io/learn-with-phoebe/)**

<!-- /phoebe header -->

# learn-github-for-builders-with-phoebe

The terminal + GitHub workflow, for builders. Six sessions that take you from the
GitHub web UI to the real command-line workflow engineers use every day - git from
the terminal, branches and PRs via `gh`, merge conflicts without fear, and CI you
author yourself. You carry one real repo, `my-project`, from `git init` all the way
to protected-main-with-CI-and-releases.

This is the tech companion to the non-tech track,
[learn-github-with-phoebe](https://phoebefu6.github.io/learn-github-with-phoebe/) -
start there if GitHub is brand new to you, then come back to the terminal here.

## Sessions

| # | Title | What you learn | Build-along |
|---|-------|----------------|-------------|
| 1 | Git under the hood | snapshots not diffs, install + `git config`, first commits by hand | init a repo, three commits, graph playground |
| 2 | The daily loop | status → add → commit → push/pull, remotes, `.gitignore`, the undo toolbox | run the loop; pick the right undo |
| 3 | Branches + PRs from the CLI | `switch -c`, `push -u`, `gh pr create`, review deep half, CODEOWNERS | branch, PR, review from the terminal |
| 4 | Merge conflicts without fear | reading conflict markers, resolve in editor, merge vs rebase, stash + cherry-pick | force a conflict and resolve it |
| 5 | Actions authoring | YAML anatomy, write CI that lints + tests every PR, marketplace, reading failed runs | author a CI workflow on a PR |
| 6 | Ship like a professional | tags + `gh release` + semver, branch protection, deploy Pages via Actions, the pro-repo bar | cut a release, protect main, score the repo |

## Maps to the official GitHub Skills courses

- [introduction-to-git](https://github.com/skills/introduction-to-git) (Sessions 1-2)
- [review-pull-requests](https://github.com/skills/review-pull-requests) (Session 3)
- [resolve-merge-conflicts](https://github.com/skills/resolve-merge-conflicts) (Session 4)
- [hello-github-actions](https://github.com/skills/hello-github-actions) (Session 5)
- [test-with-actions](https://github.com/skills/test-with-actions) (Session 5)

## Run locally

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

## Structure

```
learn-github-for-builders-with-phoebe/
├── index.html              # landing page
├── README.md
├── assets/                 # style.css, app.js, widgets.js
├── courses/
│   ├── 01-git-under-the-hood.html
│   ├── 02-the-daily-loop.html
│   ├── 03-branches-and-prs-cli.html
│   ├── 04-merge-conflicts.html
│   ├── 05-actions-authoring.html
│   └── 06-ship-like-a-pro.html
└── materials/              # course-map.md, presenter notes
```

by Phoebe Fu

## Sibling courses

- [learn github (non-tech)](https://phoebefu6.github.io/learn-github-with-phoebe/)
- [learn data literacy](https://phoebefu6.github.io/learn-data-literacy-with-phoebe/)
- [learn strategic thinking](https://phoebefu6.github.io/learn-strategic-thinking-with-phoebe/)
- [learn claude](https://phoebefu6.github.io/learn-claude-with-phoebe/)
- [learn codex](https://phoebefu6.github.io/learn-codex-with-phoebe/)
- [learn markdown](https://phoebefu6.github.io/learn-markdown-with-phoebe/)
- [learn mermaid](https://phoebefu6.github.io/learn-mermaid-with-phoebe/)
- [learn html](https://phoebefu6.github.io/learn-html-with-phoebe/)
