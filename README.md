# Morrow Labs

Shared home for the Morrow glasses build: software, hardware interfaces, decisions, and evidence.

**Status: approved repository foundation.** Trey confirmed Andrew approved the GitHub structure on 2026-09-17. This repository contains documentation and folder boundaries; it does not yet contain a runnable app, firmware, or validated hardware. Existing companion/HUD software and frame files have not been imported here. Approval of the structure does not select a software framework or finalize the HUD design.

## Start here

1. [Approved structure](docs/decisions/2026-09-17-repository-foundation.md)
2. [Build status and next steps](docs/build-status.md)
3. [Software architecture](docs/architecture.md)
4. [Development and worktrees](CONTRIBUTING.md)
5. [Design workspace and Illustrator proposal](design/README.md)
6. [Source notes](docs/sources/README.md)

## Project map

```text
apps/companion/       Mac-facing notes and controls
apps/hud/             Compact display view
packages/contracts/  Shared card, device, and task interfaces
packages/core/       Local note state and interaction behavior
services/host/       Hardware connections and optional AI gateway
firmware/            USB sensor/controller software
hardware/            Inventory, supplier evidence, mechanical files
design/             Product flows and selected design assets
tests/              Shared fixtures and cross-component checks
docs/               Source notes, decisions, status, and handoffs
.github/             Task, bug, and pull request templates
```

These approved folder boundaries do not require separate servers or commit the project to a framework.

## First experience and physical milestone

Create and edit a note on the Mac, show it as a HUD card, resize it, and dismiss it. This local loop must work without AI. Separately, prove one readable note through a real matched optical evaluation assembly; add USB orientation after that optical connection works. A screen preview does not prove the optical milestone.

## Project record

- Source material is background, not automatically an agreed decision.
- Label planned, implemented, simulated, and physically verified work separately.
- Keep decisions and test evidence in Git alongside the affected code.
- Product naming, licensing, and open-source release remain undecided. The existing repository name is retained.
- The repository is public as verified on 2026-09-17. Keep credentials, private conversations, and unapproved third-party assets out of commits.
