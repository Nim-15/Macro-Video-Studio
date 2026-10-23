# Macro Video Studio · Independent Macro Workflow

This directory contains an original macro-film production workflow inspired by the orchestration patterns of [ai-playbooks/nursery_rhyme_music_video](https://github.com/ai-playbooks/nursery_rhyme_music_video). The root-level legacy files are retained for reference; **use this directory for macro production**.

## Purpose
Plan and coordinate photorealistic macro films with configurable subjects, chapter structure, image prompts, nominal 10-second video prompts with in-clip entry/exit effects, stable subjects, gradual realistic reveals, generation checkpoints, membership-credit controls, and final assembly QA.

Default target: **60 minutes, 16:9, 360 nominal clips at 10 seconds each**. Actual clip count and timeline length must be recalculated for trims, overlaps, or alternate durations.

## Files
- `SYSTEM_PROMPT.md`: operator contract and production stages.
- `config/WORKFLOW.json`: machine-readable defaults and verified VideoExpress route.
- `prompts/MACRO_PROMPT_GUIDE.md`: macro realism, movement and transition language.
- `prompts/prompt_book.template.json`: structured prompt and scene template.
- `state/WORKFLOW_STATE.example.json`: checkpoint template.
- `TRANSITIONS.md`: transition rules and tested editor handoff.
- `BUDGET.md`: membership-credit use and retry discipline.
- `pilots/BLACK_BLOOM_PILOT_01.md`: Black Bloom five-clip runbook.
- `pilots/BLACK_BLOOM_PREFLIGHT.md`: live-app observations and test results.
- `pilots/pilot_prompt_book.json`: Black Bloom prompts, chain details and test records.
- `pilots/pilot_state.example.json`: Black Bloom run checkpoint.

## Operating instructions
1. Lock the theme, audience, visual bible, duration, frame ratio and rights needs.
2. Build the scene map and pair each clip's in-clip entry/exit effects before generation. Keep every effect inside that clip's duration.
3. Check the existing account's included membership allowance and existing assets. Use the paid membership for authorized project generations; no top-up or upgrade without explicit authorization.
4. Generate the minimum reference imagery needed. Use VideoExpress **Create Video From Prompt**, Advanced Mode and Manual Video Length = 10 for tested 10-second clips.
5. Run dependent clips sequentially: add each video to the timeline for review, save its endpoint through the media-library clip menu → Save Last Frame, verify it in My AI Images and select it for the next clip. This avoids exact-boundary seeking.
6. Review every output before continuing. If a specific defect occurs, diagnose it, make one targeted edit, and allow at most one retry. Never submit an unchanged prompt again.
7. Save a checkpoint after each clip with source and output assets, measured duration, transition QA and observed credit use when available.
8. Assemble clips directly adjacent without added editor transitions; measure trims, holds, audio and export settings explicitly.

## Verified route and limits
The VideoExpress prompt workflow produced two 10-second 1920×1080 clips at Manual Video Length = 10. BB-002 used BB-001's saved endpoint as the reference and appeared directly after it on the timeline. The clip menu → Save Last Frame created an 831 KB endpoint in My AI Images; the endpoint was selectable in the next prompt form. BB-002 retained the violet droplet palette but did not clearly depict an orchid. The First Frame, Last Frame route produced 7 seconds in the tested 10-second request. Review opening continuity and subject identity on each chained render; frame selection does not guarantee exact adherence in generated motion.

Artistly and VideoExpress are not connected to a repository API by these files. A browser-capable agent with an authenticated session is needed for UI actions. Keep credentials out of this repository. Do not claim an automated generation happened unless the live product confirms it.

## Attribution and reuse
The source repository is credited above for workflow inspiration. Review the source project's applicable license before distributing copied original text or code. These macro documents are independently authored and do not purport to grant rights to inherited material.


## Transition standard v2
Every clip begins with a visible optical/light transition-in and ends with a visible optical/light transition-out, both inside its requested duration. Lock the principal subject's identity and geometry; allow subject or color changes only as gradual, realistic optical/light reveals of a distinct subject. Place clips directly adjacent with no editor-side cuts, dissolves, or added transition time. See `TRANSITIONS.md` and `prompts/MACRO_PROMPT_GUIDE.md`.
