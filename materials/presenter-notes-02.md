# Presenter notes - Session 2: The daily loop

Audience: builders (analysts, data scientists, junior devs) moving from the GitHub web UI to the terminal. CLI-first. Warm, practical, fun-not-dry.

## Minute-by-minute run of show (45 min)

- **0-3 · Welcome.** Recap Session 1 in one line: "you made history by hand." Today: that becomes a daily loop, connected to GitHub, with an undo toolbox you trust. Read the "What you walk out with" callout aloud.
- **3-18 · Concepts.** Part 1 the loop (5): draw the cycle SVG, hammer pull-before-push. Part 2 .gitignore (4): show the sample .gitignore, tell the leaked-AWS-keys story. Part 3 undo toolbox (6): walk the decision strip left to right; land the six-word rule "revert in public, reset only locally"; one-line each on --soft/--mixed/--hard.
- **18-40 · Build-along.** BA1 wire the loop (7): everyone connects an origin and runs one full loop, confirms on github.com. BA2 .gitignore (6): create fake .env, ignore it, watch it vanish from status. BA3 sorter widget (8): work the six oh-no cards together; green = right tier.
- **40-45 · Q&A.** Take the five expected questions below; if quiet, ask the room "what did you always reset when you should have reverted?"

## Preflight

- Terminal open, font bumped for projector; a demo repo ready to `git init` fresh OR reuse Session 1's my-project.
- `gh` authenticated (`gh auth status`) so `gh repo create` works live.
- Test the sorter widget in the actual browser before class - drag one card, confirm green feedback fires.
- Projector zoom: toggle it on; click one SVG to confirm the zoom modal works.
- Have a Codespace fallback tab open (press `.` on any repo) in case local git or gh misbehaves live.

## Never-cut beats

- **The revert-in-public / reset-in-local rule.** This is the session's spine. Say it, show it on the decision strip, repeat it in Q&A. If they remember one thing, this is it.
- **The secret-in-history warning.** Deleting a committed secret does NOT remove it - it lives in history forever; rotate the key. This is a security lesson, not tidiness. Do not skip even if short on time.

## Cuts if running long

- Drop the fetch-vs-pull self-study aside (it is on the page to read).
- Shorten BA1: skip the no-gh `git remote add` path unless someone lacks gh.
- BA2 can be a live demo instead of everyone typing.

## Five expected questions

1. **"What if I already committed a secret?"** The file is still in earlier history even if you delete it later. Two steps: rotate the secret (make the leaked one useless - the only real fix), then optionally rewrite history to scrub it. Prevention via .gitignore beats both.
2. **"reset --hard ate my work - is it gone?"** Almost certainly not. `git reflog` lists every place HEAD has been for ~90 days; find the commit and `git reset --hard <hash>` to bring it back. Caveat: reflog cannot recover work you never committed.
3. **"When do I use fetch instead of pull?"** Fetch downloads without merging - use it to look before you leap. Pull is fetch + merge in one. Day to day, pull; when you want to inspect first, fetch then review.
4. **"Do I have to stage with git add every time?"** Yes - staging captures a snapshot at add-time (Session 1's model). `git add .` stages everything changed; `git commit -am` stages tracked files and commits in one go.
5. **"What is origin, exactly?"** Just a nickname for the main remote (your repo on GitHub). Set on first connect; see it with `git remote -v`. You can have several remotes, but origin is the conventional main one.
