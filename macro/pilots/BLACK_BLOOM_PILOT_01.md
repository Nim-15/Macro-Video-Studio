# BLACK BLOOM · Pilot production 01

**Status:** The first pass contains five 10-second clips on the saved timeline from 00:00 to 00:50. The user reviewed them and requested transition and subject-stability corrections. A v3 prompt pass now follows the user's copy-ready structure and one-image chaining rule. Two BB-001 v3 candidates were reviewed and failed endpoint-focus QA. A single targeted v3.1 retry was also reviewed and failed endpoint-visibility QA. The prompt book now contains a v3.2 fixed-camera, locked-focus/exposure plan with background-only light transitions, pending review.

## Goal

Produce five connected 10-second macro clips with visible in-clip entry and exit effects on a pure black background. Keep each effect within its clip duration. Style: premium botanical studio macro, realistic water droplets, very shallow optical focus, professional upper-left lighting, restrained motion. Nominal sequence length: **50 seconds** using direct adjacency; in-clip transition effects mark boundaries and no editor-side transitions are added.

## Verified VideoExpress route

Use **Create Video From Prompt** for the 10-second target. In Advanced Mode, enable **Manual Video Length, sec** and set it to **10**. The BB-001 prompt-mode test played at 0:10 / 0:10 in 16:9 at 1920×1080.

For each dependent clip:
1. In Media Library → **My AI Videos**, close the creator if needed, find the finished clip, and choose **Add to Timeline**.
2. From the finished clip's context menu, choose **Save Last Frame**. Name it `BB-00N_SUBJECT_LAST_FRAME_10S` and confirm it appears in **My AI Images**. This avoids seeking to the exact timeline boundary, which can show black after the clip ends.
3. Start **Create Video From Prompt**. Choose **Use from Library → My AI Images** and select the previous scene's saved endpoint.
4. Confirm the selected image, 16:9, **Photorealistic (Cinematic)**, Advanced Mode, and Manual Video Length = 10. Replace both sample prompts.
5. State that the selected image is the exact opening composition. Describe plausible motion and the planned exit state; do not ask the model to morph one flower species into another.
6. Generate one clip. Retrieve it from **Media Library → My AI Videos**, play it, verify runtime and continuity, add it to the timeline, save its endpoint, and continue.

## Generation discipline

- Reuse assets already in My AI Images/My AI Videos before creating replacements.
- Generate one approved master still for BB-001 only. For every later clip, use the preceding clip's saved endpoint; create a replacement still only if that endpoint is missing or unusable.
- Run one clip at a time because each next input depends on the actual preceding output.
- Check prompt, reference, aspect ratio, and 10-second setting before submitting.
- Never rerun an unchanged prompt. For a failed clip, record the defect, change only the relevant prompt or reference, and allow at most one targeted retry before revising the scene plan.
- Keep a checkpoint after every clip: scene ID, prompt version, source image, video asset, measured runtime, endpoint image, visible credit use, QA notes, and next scene.
- Existing membership generations are authorized for this pilot. Do not purchase top-ups, upgrades, or another subscription without explicit user authorization. Record usage only when shown in the account.

## Transition chain and current observations

The revised v3 prompt book is authoritative. Every clip must begin and end with a gradual in-clip light or optical effect; place clips directly adjacent with no editor-side cut, dissolve, wipe, fade, or separate transition duration. Preserve each subject's identity, species, silhouette, anatomy, proportions, texture, and position. Any color or subject change must happen gradually through plausible light, focus, refraction, bokeh, or shadow; reveal a new subject as distinct, never morph one into another. All effects fit inside the 10-second clip.

| Clip | Timeline | Current result | QA note |
|---|---:|---|---|
| BB-001 Iris | 00:00–00:10 | 10s, 1920×1080; endpoint `BB-001_IRIS_LAST_FRAME_10S` | Test render is on the saved timeline; visual approval and QA score pending. |
| BB-002 Orchid | 00:10–00:20 | 10s, 1920×1080; endpoint `BB-002_ORCHID_LAST_FRAME_10S.png` | Opening keeps violet petal/dew-drop composition. Mid-clip is soft lilac focus; orchid identity is unclear. Review before using as a quality target. |
| BB-003 Rose retry | 00:20–00:30 | Job `8ebacb3e-4a65-496f-b12c-357270cf3eb5`, 10s, 1920×1080; endpoint `BB-003_ROSE_RETRY_LAST_FRAME_10S.png` | Retrieved from My AI Videos, replaces the soft original, and resolves into a recognizable focused ivory rose. Exit is a warm close rose, not the planned creamy crescent. |
| BB-004 Calendula | 00:30–00:40 | Job `9725abe9-0160-4b10-a305-770a5f2ef303`, 10s, 1920×1080; endpoint `BB-004_CALENDULA_LAST_FRAME_10S` | Corrected render shows one orange flower with clear radial grooves and no rose overlap. Exit is a small dark orange-green bud, not the planned amber bokeh. Two earlier overlay/unclear candidates were rejected. |
| BB-005 Dahlia | 00:40–00:50 | Job `47376f6e-b3ce-445b-9829-4e270846ae0e`, 10s, 1920×1080; endpoint `BB-005_DAHLIA_LAST_FRAME_10S` | Opens on the actual BB-004 bud, shows a recognizable burgundy dahlia near 00:05, and fades nearly to black at 00:10. |

The current sequence is a **continuity and workflow proof**, not yet an approved quality master. BB-002 legibility and the BB-003→BB-004 visual handoff need review. BB-004→BB-005 follows the actual saved bud, so it no longer depends on the originally planned bokeh cue.

## Pilot review and scale gate

Score each clip 0–5 for botanical realism, water physics, camera stability, lighting continuity, entry/exit match, and temporal stability. Reject obvious anatomy defects, floating droplets, conspicuous morphing, flicker, or motion jumps.

Before extending production, review the complete 00:00–00:50 timeline at clip boundaries, record the scores, and decide whether to revise the weak links. Do not mark this pilot approved for a 60-minute production until that review is complete.

A 60-minute timeline made only from contiguous 10-second clips would require 360 clips. Treat that as a duration calculation, not a recommendation: test longer pacing and editorial reuse (carefully reviewed loops, still-image camera moves, and sound beds) before estimating generation volume. Measure the assembled timeline; transitions and overlaps affect runtime.

## Records

`pilot_state.example.json` contains the render IDs, current statuses, endpoint names, and verified workflow. This pilot is managed through the Artistly and VideoExpress interfaces; the repository does not contain an API integration. Keep credentials out of the repository.


## User correction · one-image chain and transition prompt v3

The first-pass review identified four requirements for the corrected run:

1. Every clip visibly opens with a transition-in effect and closes with a transition-out effect.
2. Keep principal subjects stable and recognizable. Avoid extreme changes, deformation, stretching, duplication, or species morphing; show only gradual, plausible macro-photography changes.
3. A subject or color change may occur within a clip through a creative but realistic light/optical effect.
4. The paired in-clip effects alone mark adjacent scene boundaries. Place clips directly together and add no editor-side transition or extra duration.

The copy-ready video prompt uses the exact section order and timing the user supplied: **ENTRY TRANSITION, 0–2s; MAIN ACTION, 2–8s; EXIT TRANSITION, 8–10s**. Generate only the BB-001 master still; each subsequent clip uses the actual last frame of the previous clip.

The Artistly master still generated for BB-001 is visible in Artistly Personal Designs, but the VideoExpress **My Artistly Images** folder was empty, so it was not available as a source for the video render. The two v3 jobs instead used the already available `BB-001_IRIS_LAST_FRAME_10S.png` in **My AI Images**.

Two v3 candidates are present in **My AI Videos** (6.17 MB and 4.73 MB; the UI did not map their IDs to file sizes). The 6.17 MB candidate was reviewed first; its 0:10 frame was too soft/defocused to use. The 4.73 MB candidate was then played in VideoExpress; it also progressively pushed into the droplet but ended with the droplet/petal visibly soft and lacking sufficient detail for a chain endpoint. Neither candidate was added to the timeline, and no endpoint was saved. The duplicate submission resulted in two renders. A single planned targeted retry also completed; no further generation is authorized under the current pilot retry rule.

**Resume:** the v3.1 retry (job `61e23ee8-24a8-446b-adf2-74cb15ee8c7c`, 6.25 MB) completed at 10 seconds but its 0:10 frame is nearly black and lacks useful droplet/petal detail. It was rejected, not added to the timeline, and no endpoint was saved. Replan BB-001 to keep the subject visibly detailed at 0:10 and avoid a whole-frame exposure fade. The prompt book now has a revised v3.2 shot plan: fixed camera, locked focus and subject exposure, localized light effects only, and no whole-frame fade. Review that prompt before considering any further generation.
