# Working together

## Daily workflow

1. Pull main and choose or open one GitHub issue for a small experience, design, or hardware task.
2. Read the build status and agree the behavior/interface affected by the task.
3. Create a feature branch in a separate worktree.
4. Implement and run relevant local checks with paid AI disabled.
5. Trey pressure-tests the experience; record actual outcomes and unresolved issues.
6. Commit the scoped change and push the feature branch.
7. Open a pull request linking the issue and evidence; merge the accepted result into main. Tag releases when there is a meaningful tested milestone.

Trey's focus is product experience, cards, interactions, design, branding, and implementation. Andrew's focus is engineering and voice integration; both build. These are collaboration focus areas, not exclusive ownership boundaries.

## Branches and worktrees

The approved foundation establishes main. Use short-lived issue-scoped branches after bootstrap. Fetch and inspect collaborators' commits before integration; never force-push shared history.

Example after main has been published:

```sh
git switch main
git pull --ff-only origin main
git worktree add ../morrow-note-card -b feature/note-card main
```

In the new worktree, make the scoped change, inspect it, and stage only intended files. Then:

```sh
git commit -m "Add local note card interactions"
git push -u origin feature/note-card
```

Open a pull request on GitHub. Worktree folders stay local; branches and commits are shared. Worktrees separate checkouts but do not isolate ports, devices, credentials, or paid API access. Give concurrent app instances separate local ports when needed.

## Running software

There is no runnable software or install command in this foundation. First locate and inspect the existing companion and HUD source. Select the smallest suitable stack after that review, then document exact setup/run/check commands here. Do not add a second implementation just because these folders exist.

## Commit hygiene

Keep secrets, private test data, caches, local worktrees, and generated builds outside commits. Put example configuration in a reviewed `.env.example` without values. Verify supplier/asset sharing rights before committing files; consider Git LFS for large approved CAD/binary files when actual assets are available.

## Review and releases

Use the issue and pull request templates to record scope, acceptance criteria, and evidence. Prefer review by the other builder before merging implementation work. This is a team workflow; branch protection is not configured by these files. A tag should identify a tested milestone and its limitations, not imply production or physical readiness.
