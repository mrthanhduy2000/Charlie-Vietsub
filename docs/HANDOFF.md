# Handoff (2026-11-26, dubbing delay attribution and speaker benchmark, lanes B/D)

## Current state
- Charlie Vietsub stays at 3.2.4. This handoff changes the speaker benchmark and documentation.
- Chrome Profile 42 loads ID alijbbmpkioojdegjipbbhmlgchpfgof from the canonical checkout.
- 145 saved videos, 16,481 spoken segments. Playback onsets over 0.5 s: 2,008.
- At +0.5 s an earlier take was unfinished in 1,495 cases, its successor lacked audio in 28
  other cases, and 485 cases were gated by rest, scheduling or element startup.
- Zero simulated startup: 1,655 late onsets. Zero modeled generation RTF: 1,856. Translations
  were ready in both; this comparison does not measure live translation waits.
- An earlier finish target (rest plus 150 ms of startup allowance) yielded 1,911 late onsets
  but 990 versus 900 adjacent rate jumps over 15%. The worst lag was unchanged. No pacing change.
- Speaker lab replays real archived Gemini 3.1 Flash-Lite text answers against named PBS captions.
- Experimental October run v3: 87.8% average for plain captions, 91.8% with edited labels stripped.
- The scorer rejects incompatible line indices. New answers save the ordered caption text hash.
- The exact historical input line builder for October v2/v3 is dub-planner.js at e43f006.
- No audio was played. The 145-video experiment was a simulator run.

## Unfinished
- Live audio, exact current production speaker prompt accuracy, and source-meaning judgments.
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
- The October lab tag v3 is different from production SPEAKER_PROMPT_VERSION 3.
- Measure playbackLag for first movement; the scheduling lag omits element startup.
- Never identify a YouTube reading by its media element; navigation can reuse it.
- Keep the canonical path stable. Reload the existing extension to retain settings after updates.
- Keep private recovery data and API keys outside Git.
