# Handoff (2026-11-26, dubbing delivery, lane B)

## Current state
- Charlie Vietsub 3.2.4 in the canonical checkout and GitHub Charlie-Vietsub/main.
- Chrome Profile 42 loads ID alijbbmpkioojdegjipbbhmlgchpfgof from this folder. Reload after updating.
- Dubbing reads use the full timed caption track and the current playback engine as scope.
- Shared source cues cannot duplicate speaker marks. Source context for speech uses the segment span.
- Voice selection is captured with the cache key; stale source or cast work cannot replace current audio.
- Duration forecasts use recorded take units, and learned speed follows the actual TTS voice.
- A confirmed cache miss on the next take can proceed before looking up later takes.
- Dubbing still preserves subtitle content in order while video plays and drains remaining speech at EOF.
- Measurement used offline playback and read-only archived/Chrome captions. No audio was played.
- npm test: 1,193 pass, 0 fail, 2 skips. Across 145 videos, 16,481 segments kept all their words.
- Simulated late starts 1,890 to 1,889. Recorded startup was unchanged; gap time 6.56 s to 6.77 s.
- The 45-video and 24-scenario regression run's three small trade-offs are recorded in DUBBING.md.

## Unfinished
- Live audio, speaker attribution accuracy and source-meaning judgments remain unverified.
- Dense speech can build up queued delay, especially with a slow server or a low rate cap.
- Fresh ASR accuracy, CPU/latency/cost and full-video semantic truth remain unmeasured.
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
- Never identify a YouTube reading by its media element; navigation can reuse it.
- Cache keys must describe the voice that actually made the audio, including during cast updates.
- The corpus and simulator check structure and delivery, without labeled answers for speaker identity.
- Never expose private recovery data or API keys. Keep the migration backup outside Git.
- Keep the canonical directory stable. Reload the existing extension to retain its settings.
