# Macro Video Studio · Independent Macro Workflow

This directory contains an original macro-film production workflow inspired by the orchestration patterns of [ai-playbooks/nursery_rhyme_music_video](https://github.com/ai-playbooks/nursery_rhyme_music_video). The root-level legacy files are retained for reference; **use this directory for macro production**.

## Purpose
Plan and coordinate photorealistic macro films with configurable subjects, chapter structure, image prompts, 10-second video prompts, matched entrance/exit transitions, generation checkpoints, budget controls, and final assembly QA.

Default target: **60 minutes, 16:9, 360 nominal clips at 10 seconds each**. Actual clip count and timeline length must be recalculated if transition overlaps, trims, or alternate clip durations are used.

## Files
- `SYSTEM_PROMPT.md`: operator contract and production stages.
- `config/WORKFLOW.json`: machine-readable defaults.
- `prompts/MACRO_PROMPT_GUIDE.md`: macro realism, movement and transition language.
- `prompts/prompt_book.template.json`: structured prompt and scene template.
- `state/WORKFLOW_STATE.example.json`: checkpoint template.
- `TRANSITIONS.md`: transition rules.
- `BUDGET.md`: credit estimation and approval gates.

## Operating instructions
1. Select macro theme, audience, aesthetic, duration, frame ratio, soundtrack type, and rights.
2. Develop a six-chapter visual progression, visual bible, scene map, and adjacent-frame plan.
3. Price the tools with **current account-specific prices**; obtain explicit GO before paid generation.
4. Generate 3–5 test clips and evaluate continuity before proceeding.
5. Produce approved clips in confirmed batch sizes. Record tool IDs, output locations, and checkpoints after each batch.
6. Assemble using verified editor features. Confirm final audio synchronization, runtime, frame size and export.

## Automation limitations
Artistly, VideoExpress and optional CloneVoice are *planned tools*, not proven integrations. A browser-capable agent with authenticated sessions and application permissions is required to automate GUI operations. This repository by itself is **not an executable video generator**. Do not invent supported features, completed actions, export URLs, pricing, or render results.

## Attribution and reuse
The source repository is credited above for workflow inspiration. Review the source project's applicable license before distributing copied original text or code. These new macro documents are independently authored and do not purport to grant rights to any inherited material.
