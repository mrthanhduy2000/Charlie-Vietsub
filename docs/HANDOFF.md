# Handoff (2026-11-15, Chrome path migration and verification, lane D)

## Current state
- Charlie Vietsub runtime remains 3.2.3; only maintainer tools/docs changed this turn.
- Canonical checkout: /Users/damduy/Downloads/Charlie Vietsub; origin is Charlie-Vietsub/main.
- Chrome Profile 42 now loads the real folder as alijbbmpkioojdegjipbbhmlgchpfgof.
- Initial inspection found Chrome still running commit 94238bc while disk/GitHub were 13329d8.
- Reload changed the extension ID because Chrome resolved the renamed/symlinked folder.
- With user consent Chrome was closed; local/sync stores were backed up and local data copied.
- Raw sync-database copying did not preserve settings through Chrome startup; supported import did.
- All 48 original settings were imported, including Gemini key, Kim Thanh voice and Lexend style.
- Key connection succeeded in Settings; key/voice/style survived another Chrome restart.
- Old-path symlink was retired into the private backup; only one Charlie toolbar button remains.
- Old registration metadata remains in Chrome but its path no longer exists; it cannot load.
- Backup: ~/Library/Application Support/Charlie Vietsub/migration-backup-20261115-013300/.
- tools/platform-paths.js, AGENTS.md/CLAUDE.md and docs now identify the new extension/store.
- Full offline suite: 1,187 pass, zero fail, two skips; no runtime release note required.

## Unfinished
- Fresh ASR accuracy, CPU/latency/cost and full-video semantic truth remain unmeasured.
- Complex clause completeness, causality, conditions, arbitrary names and pronouns remain unverified;
  consistent term usage and refinement checklists are not independent semantic correctness labels.
- Natural local domains/senses have no human annotation; keyword evidence remains English-oriented.
  Current corpus measurements do not establish real-provider translation improvement or billed cost.
- Source/audio mismatch needs an independent reference; a structurally clean track may disagree.
  The saved Russian-source discrepancy remains unresolved (one prior ASR excerpt conflict).
- Multi-speaker attribution, glossary loading/UI states and full-video/source-meaning listening remain.
- Documentary 9T1Nvtn3QOk: earlier inspection only 39-43 minutes, no complete ytcache4 record.
- Carry forward native fullscreen, real-page overlay fade, sparse notice on iYL-UuNE_9w,
  TED embed/hold issues, Mac auto-update install and old UI redesign-note reconciliation.

- The Codex sidebar label may still show the old project name; rename it manually.

## Traps
- A symlink is not an extension-ID preservation mechanism; do not recreate the retired old path.
- Never expose the private backup or API key. Restore settings via supported import, not raw sync DB.
- Reload only the canonical extension after runtime updates; never remove/reinstall the active copy.
- Verify browser runtime separately from the popup's disk version; source equality alone is insufficient.
