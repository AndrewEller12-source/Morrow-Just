# HUD design workspace — proposal for discussion

Start with a separate `Morrow HUD System.ai` document alongside the existing brand master. These are proposed names, not files created by this setup.

## Illustrator organization

Use RGB and pixel units. Select the artboard resolution after confirming the display target. Label provisional preview sizes as simulation; they do not establish optical readability or compatibility.

1. `00 Foundations` — type roles, spacing, color roles, icon strokes, and provisional safe area.
2. `01 Components` — note card, compact status, action prompt, and supporting icons.
3. `02 States` — idle, listening, working, result, approval needed, failure, stale, and disconnected. These are proposals, not implemented capabilities.
4. `03 Screens` — whole HUD compositions using the same components.
5. `04 Flows` — note create/edit/show/resize/dismiss/re-show and assistant request/cancel.
6. `05 Readability` — long/short text, contrasting scene backgrounds, edge targets, and size comparisons for later real-optics checks.

Use consistent layers: `Guides` (locked), `Scene reference` (locked, excluded from asset exports), `UI`, and `Annotations` (excluded from asset exports). Name groups by component and state. Use symbols for reused elements, global swatches for shared colors, and named character/paragraph styles. Keep text editable in the master; outline only a separate export if needed.

## First design slice

Define one clear note card and its controls before building many applications. Keep dismiss, re-show, and resize behavior explicit. Then explore one assistant status/approval flow independently of the local card interaction.

Decide where the HUD rests, how it is engaged, information priority, and what happens during disconnect. Do not assume world anchoring or positional tracking. Provisional safe areas and desktop previews require confirmation through actual optics.

## Handoff

Export named screens as PNG for review and selected vectors as SVG for implementation. Record dimensions, typography, behavior, source revision, and token values in a Markdown specification. Include failure states. Artwork is visual reference; live text, state, interaction, and accessibility still need implementation.

Example names: `note-card--default.svg`, `hud--note-visible.png`, `hud--disconnected.png`. Add `exports/` when selected assets exist.

## Adobe references

- [Swatches and global colors](https://helpx.adobe.com/illustrator/desktop/manage-colors/use-swatches/about-swatches.html)
- [Export assets for web and app design](https://www.adobe.com/learn/illustrator/web/export-assets-web-app-design)

This proposal is not an approved visual system or a claim of hardware-tested sizes, colors, or typography.
