# Kopi · a design-to-production demo

A one-screen point of sale UI whose entire look is driven by one file:
`tokens.json`. Colours, radii, spacing, type and the thumbnail tints all
load from it at runtime. Change one value there and the till reskins.

This repo exists as the companion to two tutorials: *GitHub for
designers* and *Shipping a design change without fear*. It is set up the
way those tutorials assume: checks on every pull request, deploy
previews, and a protected main branch.

Two pages, same data:

- `index.html` - text tiles
- `index-thumbs.html` - illustrated thumbnails (SVG sprite, no images)

## The exercise: ship a design change

1. **Fork this repository** (top right). Your fork is your own copy.
2. In your fork, open `tokens.json` and press the pencil icon.
3. Change `color.accent` from `#C4472B` to a colour of yours.
4. Commit to a **new branch** and open the pull request GitHub offers.
5. Watch the checks run. If you removed a comma by accident, the
   `build` check fails and tells you so: that is the system working.
6. Open the deploy preview once it appears, and look at your till.
7. Merge. You have shipped a design change through the same gate
   professional teams use.

One honest note: forks do not inherit branch protection. If you want
the full experience in your fork, switch it on: Settings, Branches,
add a rule for `main` requiring a pull request and passing checks.

## Undo, both ways

- **Revert**: every merged PR has a Revert button that opens a new PR
  undoing it, through the same checks.
- **Rollback**: the hosting dashboard lists every deploy production has
  run; publishing an older one switches back in seconds.

The catastrophe was always one minute deep.
