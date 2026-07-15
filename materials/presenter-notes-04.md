# Presenter notes - Session 4: Merge conflicts without fear

**Goal of the hour:** turn the scariest word in git into a 30-second reflex. They should leave having caused and resolved a real conflict with their own hands, and knowing the merge-vs-rebase golden rule cold.

## Preflight (do before they arrive)
- Have your my-project repo in a known-good state, or be ready to manufacture the conflict live (Build-along 1 does exactly this - rehearse it once so the `HEAD~1` branch point lands clean).
- Open a terminal large and high-contrast; projector zoom ON in the toolbar.
- Test both widgets: the sorter drag-and-drop responds and turns green on correct drops.
- Codespace fallback tab open (press `.` on the repo) in case a local git is misbehaving.
- Have an editor open showing the conflict markers with syntax coloring - VS Code makes the accept buttons visible, good for the "you have help" beat.

## Minute-by-minute
- **0-3 Welcome.** Name the fear out loud: "raise a hand if merge conflicts scare you." Normalize it. Promise they cause one on purpose today.
- **3-8 Part 1 - read the markers.** Walk the SVG left to right, then the marker anatomy panel. Say the mantra: yours above, theirs below, divider in between. Show the git status termbox - "status is still your compass."
- **8-12 Part 2 - resolve.** Four moves: open, choose combination, delete all three markers, add + commit. Hammer "the answer is often BOTH." Show `git merge --abort` and call it the panic button.
- **12-18 Part 3 - merge vs rebase.** SVG side-by-side. Then the golden rule, said twice. Stash and cherry-pick as one-liners.
- **18-28 Build-along 1.** The centerpiece. Everyone manufactures and resolves the conflict. Do not rush - this is the fear-killer.
- **28-34 Build-along 2.** Sorter widget. Let them argue about the "colleague already pulled" row - it teaches the golden rule.
- **34-40 Build-along 3.** Stash drill. Fast and tactile.
- **40-45 Q&A.**

## Never cut
- **Resolving the live conflict end to end (Build-along 1).** If you cut everything else, keep this. The fear only dies by doing it once with hands on keys.
- **The merge-vs-rebase golden rule.** Say it, show it, put it on the board. This is the one thing that prevents real damage later.

## Cut if running long
- Build-along 3 (stash) can shrink to a 60-second demo you drive while they watch.
- The interactive-rebase self-study card - point at it, do not present it.
- Self-study cards throughout are read-after-class by design.

## Five expected questions
1. **"I get a conflict every single time I pull."** Your branch is stale - it drifted far from main. Pull main often and keep branches short-lived; conflicts shrink to nothing.
2. **"Is rebase dangerous / scary?"** Only on shared, pushed history. On your own local commits it is completely safe and makes your history clean. The golden rule is the whole safety story.
3. **"I resolved it but the build still complains about `<<<`."** You left a marker line in the file. Search the file for `<<<<<<<`, `=======`, `>>>>>>>` and delete any that remain.
4. **"Which side is mine again?"** HEAD is always your current branch, always above the `=======`. The incoming branch is below.
5. **"I made it worse - can I start over?"** `git merge --abort` (or `git rebase --abort`) resets you to before you started. Nothing lost.
