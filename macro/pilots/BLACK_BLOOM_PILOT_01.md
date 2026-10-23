# BLACK BLOOM · Pilot production 01

**Status:** prompts prepared only. No image/video generation, spending, tool authentication, or renders have occurred.

## Goal
Produce five ten-second macro clips with precise transition entry/exit descriptions, on pure black background. Theme is premium botanical studio macro, realistic water droplets, very shallow focus, professional upper-left lighting, restrained movement. Final nominal film length: **50 seconds** before editing overlaps.

## Preflight and approval
1. In signed-in Artistly, manually verify image dimensions, photo-realistic model and image-reference support. Record credit price.
2. In signed-in VideoExpress, verify 10-second generation, image-to-video input, last-frame export and first-frame reference, batch and queue limits, and cost. Do not assume any feature is supported.
3. Record user-approved total maximum credits and get explicit **GO** before launching paid generations.
4. Generate stills for BB-001 through BB-005 (see `pilot_prompt_book.json`). For strongest frame continuity, replace next still's prompt with actual previous end-frame reference only after tool feature verification.
5. Generate 5 clips one by one for the pilot; batch only if tool capacity is verified. Inspect first and last frames; capture actual last frame after each render.
6. Assemble in order and measure timing; exact 50 s requires butt cuts or extension/compensation for overlapped dissolves.
7. Document observed spending, visual artifacts, rejected generations, editor steps and exported file location in `pilot_state.example.json`.

## Evaluation scorecard
Rate each axis 0–5 for each clip: (1) botanical realism, (2) water physics, (3) camera steadiness, (4) lighting consistency, (5) transition entry/exit alignment, (6) temporal stability. Fail any clip with conspicuous anatomy glitches, sudden morphing, floating droplets or motion discontinuities. **Gate:** review all clips before moving to 60-minute production.

## Operational caveat
Files in this folder are planning and production instructions, **not a functioning Artistly/VideoExpress integration**. A browser-operating agent and authenticated sessions would be needed to execute them. Do not save private credentials in this public repository.
