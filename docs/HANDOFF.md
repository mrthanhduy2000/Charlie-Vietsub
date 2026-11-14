# Handoff (2026-11-14, lane C with D release/install metadata)

## Current state
- Release 3.2.3 renames the extension to Charlie Vietsub in manifest, popup, settings and onboarding.
- GitHub repository renamed to mrthanhduy2000/Charlie-Vietsub; origin and current install links updated.
- Working folder: /Users/damduy/Downloads/Charlie Vietsub.
- The former folder name is a compatibility symlink, not a duplicate checkout.
- Chrome Profile 42 still uses that old path and extension ID lpknjhmnlocilmkmooomffknibghibao.
- npm test: 1,187 pass, zero fail, two skips; local build verification passed after commit.
- No translation, dubbing, storage schema, model default or settings migration changed.
- Previous 3.2.2 local context/scoped terminology and preservation constraints remain in place.
- Old Downloads copies (three folders, five ZIPs, 94.1 MiB) were moved to Trash, not purged.
- Old GitHub repos translator and dich-phu-de-long-tieng remain: CLI lacks delete_repo permission.
- Codex sidebar project rename could not be automated: computer access to Codex is blocked.

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

- Finish deleting the two old GitHub repositories after the user supplies authenticated access.
- The Codex sidebar label may still show the old project name; rename it manually.

## Traps
- Keep the old-path symlink: removing/reinstalling or loading the new path can lose access to settings.
- Click Reload at chrome://extensions; never remove the extension and Load unpacked again.
- GitHub renames do not update origin automatically when gh repo rename uses --repo.
- Brand and metadata changes do not establish real-provider translation or listening quality.
- Preserve complete FIFO speech and auto model selection; no shortening of dubbing lines.
