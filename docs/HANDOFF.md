# Handoff (2026-11-26, dubbing pace and live speaker prompt benchmark, lanes B/D)

## Current state
- Charlie Vietsub 3.2.5 in the canonical checkout and GitHub Charlie-Vietsub/main.
- Chrome Profile 42 loads ID alijbbmpkioojdegjipbbhmlgchpfgof. Reload the existing extension.
- The buffered complete-speech engine reserves the boundary rest and 150 ms of startup.
- Short actual rests limit rate changes using the previous played rate. FIFO and rate caps remain.
- 145 saved videos, 16,481 segments, zero lost or repeated words. Onsets late by over 0.5 s:
  2,008 to 1,917. The 290 onsets past 2 s were unchanged. Short-rest changes over 15%: 43 to 1.
- Long-rest rate changes increased, and the two small standard-suite trade-offs are in DUBBING.md.
- Fresh A/B on 30 edited PBS excerpts without speaker labels, paired by input and model.
  Gemini 3.1 Flash-Lite: mean accuracy 93.724% production, 92.773% trial. Production prompt retained.
- Read-only speakerLab answers use tags n26base and n26rev. The paired harness runs both in one tab.
- Prior ignored lab input/config files were restored after the run. No audio was played.
- npm test: 1,195 pass, 0 fail, 2 skips. Regression baseline saved for the release.

## Unfinished
- Listening quality and attribution outside the benchmark's edited English news remain unverified.
- Dense speech can accumulate delay, especially with slow synthesis or a low voice rate cap.
- Fresh ASR accuracy, user-specific CPU/latency/cost and full-video semantic truth remain unmeasured.
- Complex clause completeness, causality, conditions, arbitrary names and pronouns remain unverified.
- Natural local domains/senses have no human annotation; keyword evidence remains English-oriented.
  Current corpus measurements do not establish real-provider translation improvement or billed cost.
- Source/audio mismatch needs an independent reference; a structurally clean track may disagree.
  The saved Russian-source discrepancy remains unresolved (one prior ASR excerpt conflict).
- Glossary loading/UI states remain open.
- Documentary 9T1Nvtn3QOk: earlier inspection only 39-43 minutes, no complete ytcache4 record.
- Carry forward native fullscreen, real-page overlay fade, sparse notice on iYL-UuNE_9w,
  TED embed/hold issues, Mac auto-update install and old UI redesign-note reconciliation.
- The Codex sidebar label may still show the old project name; rename it manually.

## Traps
- Lab tags and production prompt version numbers are different. Pair actual line hashes and models.
- Measure playbackLag for first movement; scheduling lag omits element startup.
- Never identify a YouTube reading by its media element; navigation can reuse it.
- Keep the canonical path stable. Keep recovery data and API keys outside Git.
