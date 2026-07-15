# Presenter notes - Session 6: Ship like a professional

The graduation session. Tone: you already have the moves, today we make them enforced.
End on a real release and a protected main they can feel.

## Preflight (do before anyone arrives)

- A `my-project` repo that already has the Session 5 CI workflow, on GitHub, ready to protect.
- `gh` authenticated in your terminal (`gh auth status` shows a green check).
- GitHub open to Settings → Branches for the demo repo, in a tab you can switch to fast.
- Test the graduation checklist widget: click a few rows, confirm the percentage and verdict update live.
- Have a throwaway commit ready for the "direct push gets rejected" beat so you are not editing live.

## Minute-by-minute (45 min)

- 0-3 · Welcome. "Five sessions of habits. Today they become rules the machine enforces." Show the scorecard you will fill at the end.
- 3-8 · Part 1, tags + releases + semver. Walk the SVG: tags pin versions, semver decodes risk. One line each on MAJOR / MINOR / PATCH.
- 8-12 · Part 2, branch protection. Walk the gates SVG. Land the point: the green check was a suggestion, now it is a gate.
- 12-16 · Part 3, deploy via Actions + the pro-repo bar. Show the deploy.yml snippet; name the checklist files (CONTRIBUTING, templates, Dependabot).
- 16-24 · Build-along 1, cut a release. Everyone tags v1.0.0, pushes it, runs `gh release create --generate-notes`, opens the Release page.
- 24-31 · Build-along 2, protect main. Everyone adds the ruleset, then tries a direct push and watches it get rejected.
- 31-37 · Build-along 3, the scorecard widget. Everyone scores their own repo honestly and reads the verdict.
- 37-40 · Homework + what is next (AI + security courses). Star the repo.
- 40-45 · Q&A.

## Never-cut beats

- The direct-push-to-protected-main rejection. Do it live. The moment the push is refused is the emotional payoff of the whole track - "the rules protected main, not me remembering to."
- Cutting a real release with `--generate-notes`. Open the actual Release page and show the changelog GitHub built from their merged PRs. Tangible proof.

## Cuts if running long

- Trim the semver self-study table to a verbal one-liner (breaking / feature / fix).
- Skip reading the deploy.yml line by line - just show it exists and merge-to-main republishes.
- Community-health files (CONTRIBUTING / templates / Dependabot) become a homework pointer only.

## Five expected questions

1. **"When is the AI / Copilot course?"** It is deliberately out of scope here - a future AI-literacy course covers Copilot and AI pair-programming. Today is about the workflow they sit on top of.
2. **"Do I need semver for internal tools nobody else uses?"** Even solo, PATCH/MINOR/MAJOR gives you a readable changelog and a way to talk about "before/after" a change. It costs nothing; skip the ceremony, keep the numbers.
3. **"Can I protect main on a free private repo?"** Branch protection rules on private repos historically needed a paid plan; rulesets have loosened this and free private repos now get core protection. If it is greyed out, that is the plan, not a mistake - demo on a public repo.
4. **"What if I am the only maintainer - the required-approval rule blocks me?"** Either drop the approval requirement and keep required checks + PR, or use an admin bypass sparingly. The CI gate is the higher-value rule for a solo repo anyway.
5. **"Lightweight vs annotated tag - does it matter?"** For releases, yes - annotated (`-a`) carries a message, author, and date, which release notes and tooling expect. Use annotated for anything you ship.

by Phoebe Fu
