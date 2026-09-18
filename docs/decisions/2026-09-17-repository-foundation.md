# Repository foundation

Status: accepted for repository structure, 2026-09-17.

Participants: Trey and Andrew. Approval evidence: Trey reported in the setup session that Andrew approved the GitHub structure during their phone call and instructed publication. This records Trey's report, not an independent GitHub review by Andrew.

## Decision

Use the existing `AndrewEller12-source/Morrow-Just` repository as one shared home for apps, reusable packages, host services, firmware, hardware evidence, design handoffs, tests, and project decisions. Keep the prepared top-level boundaries. Work through issues, short-lived branches/worktrees, relevant checks, pull requests, review, and meaningful milestone tags.

A monorepo keeps two builders' interfaces and evidence together. Split repositories only if real ownership or release needs justify it.

## Scope

This approval establishes the repository structure. It does not finalize detailed architecture, HUD visual design, framework choice, font licensing, hardware compatibility, purchases, or an open-source license. Simulation remains the default development requirement, and paid AI must be deliberately enabled and bounded before use.

The remote is public and the connected account has write permission, not repository administration permission. This setup does not change visibility or configure branch protection. Private assets, font files, and original review material remain local. Design subfolders clarify handoff locations; their proposed Illustrator workflow is open for discussion.

## Next work

1. Inventory existing companion/HUD/assistant source before implementing a new app.
2. Define the first HUD experience and reusable card states.
3. Establish an Illustrator design source and reviewable exports after the design discussion.
4. Validate real optics separately from any desktop preview.
