# Macro Film Transitions

## Required transition model

Every generated clip carries its own visible **transition-in** at the opening and **transition-out** at the ending. Both effects live inside the clip's requested duration. For the first clip, use the approved master still. Each later clip must begin from the immediately preceding clip's actual saved last frame; do not generate a separate still for it. For a 10-second clip, use this default rhythm:

- **0–2s — entry:** a soft optical or lighting effect reveals the incoming composition.
- **2–8s — macro observation:** keep the main subject stable and legible. A gradual color or subject shift may happen here when the shot calls for it.
- **8–10s — exit:** transform light, focus, refraction, or bokeh into the next clip's opening cue.

Place clips directly adjacent on the timeline. The paired in-clip effects mark the boundary. Do not add editor-side cuts, dissolves, wipes, fades, or separate transition clips between scenes. This keeps the assembled duration unchanged and reduces edit work.

## Approved effect language

Choose effects that could plausibly occur in professional macro photography:

- Controlled rim-light sweep or gradual exposure reveal.
- Slow rack focus that resolves an actual subject rather than changing its anatomy.
- Realistic lens bloom, optical bokeh, or a restrained flare.
- Refraction or caustic light through a real droplet or translucent petal.
- Gentle color-temperature shift across the subject or background.
- A soft shadow or defocused highlight that passes through frame and reveals a distinct new subject.

Do not use abrupt black cuts, hard flashes, glitch effects, liquid morphs, subject warping, or transformations that change a flower species. Keep one coherent lighting direction, camera pace and photographic texture.

## Subject and scene-change continuity

Lock the principal subject's species/material, silhouette, anatomy, proportions, texture, and location. A different subject may appear within a clip, but reveal it as a separate subject through gradual focus, light, refraction, bokeh, or a plausible foreground occlusion. Do not morph one subject into another.

The exit effect of clip N should lead visually into the entry effect of clip N+1 through a matching cue such as shape, color, highlight position, focus distance, motion direction, or light direction. Use the actual saved endpoint as the next prompt's reference when available; verify the generated opening because reference adherence is not exact.

## Continuity card for every adjacent pair

- Clip N's actual saved last-frame asset and description.
- Exit effect, location in frame, color, focus and light direction.
- Clip N+1's entry effect and matching cue.
- Principal-subject stability constraints for both clips.
- Measured clip durations and timeline boundary.
- QA result for visual continuity and whether the transition stays within clip duration.

## Timing

For pure adjacency and 360 generated clips × 10 seconds, raw runtime is 3,600 seconds. In-clip effects do not add time. If clips are trimmed or overlapped, calculate the actual runtime as the sum of clip lengths minus overlap, plus any holds. Verify the assembled timeline before promising an exact 60:00.

## Verified VideoExpress chained handoff

The tested route is **Create Video From Prompt → add the finished clip to the timeline → Media Library → My AI Videos → clip context menu → Save Last Frame → verify in My AI Images → select that image for the next prompt**. BB-001 through BB-005 demonstrated a 10-second, 1920×1080 clip chain up to 00:50. The saved-frame handoff worked, but generated content did not always match the authored subject or endpoint exactly. BB-002's orchid identity was indistinct; BB-003's exit differed from plan; BB-004 resolved to a dark bud; BB-005 used that actual bud at its opening.

## Black Bloom v2 correction status

The user's revised direction requires one generated master image for the chain, then saved-last-frame references for all later clips; a visible in-clip transition at the beginning and end of every clip; stable principal subjects; gradual realistic changes; and direct clip adjacency without added editor transitions. Use the 0–2 / 2–8 / 8–10 second prompt structure. Existing BB-001–BB-005 renders predate these rules. Their prompt book is being revised for a corrected render pass; the current rendered assets must not be described as already satisfying this new standard.