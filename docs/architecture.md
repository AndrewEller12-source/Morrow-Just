# Software architecture proposal

Status: repository boundaries approved on 2026-09-17; detailed interfaces remain proposed, with no implementation or framework selected.

## Local product loop

Companion input -> shared local note state -> HUD rendering.

The companion provides editing and controls. The HUD renders a compact card model. They may initially be two views in one application; these folders do not require separate processes. The core owns note content, placement, size, persistence behavior, and cancellation semantics. Shared contracts prevent each view from inventing a different card format.

A host service connects hardware and optionally AI. Orientation input is a device signal, not a language-model request. The display transport remains unspecified until the actual optical driver interface is confirmed. Browser rendering success must not be labeled confirmed optical presentation.

## Optional assistant path

Explicit user request -> host AI gateway -> selected provider -> task status/result -> local card state.

All paid requests should pass through one controllable gateway. The card loop must continue while a task is slow, fails, or is disabled. Keep provider credentials in the host environment, not the UI.

## Development modes to implement

- **Simulation (default):** deterministic fixtures for text results, voice transcripts, loading, failure, disconnect, and stale input. No provider request or live voice session; reject accidental attempts rather than silently falling back to live AI.
- **Live AI (explicit opt-in):** separate development credentials/project, model allowlist, output limits, bounded retries/tool steps, request timeouts, usage recording, and an immediate stop control. Start voice only on explicit engagement and stop it after the session.

Add an application-side request/token budget with conservative preflight reservation and reconciliation. Provider dashboard budgets alone are not a substitute for enforcing the application's own limits. Dollar estimates depend on current provider prices and modality; do not promise an exact universal dollar cap.

These controls are requirements, not implemented safeguards. An SDK or sandbox alone does not enforce them. Ordinary automated tests should use fixtures; live integration tests must be separately invoked and bounded.

## First implementation slice

Inspect and reuse existing code where suitable. Implement a short note with a stable ID, editable text, bounded position/size, and explicit visibility. Verify create, edit, resize, dismiss, and re-show. Specify whether notes survive restart before adding persistence. Then connect the confirmed physical display transport.
