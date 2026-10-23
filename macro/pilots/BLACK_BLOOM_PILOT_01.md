# BLACK BLOOM · Pilot production 01

**Status:** Five 10-second clips are chained contiguously on `Black Bloom Pilot 01` from 00:00 to 00:50. BB-003 uses its focused retry, BB-004 uses the corrected isolated-flower render, and BB-005 closes on a fade to black. All five endpoints are saved in **My AI Images**. The timeline project is saved; full-sequence quality review and export decision remain pending.

## Goal

Produce five connected 10-second macro clips with intentional entry and exit transitions on a pure black background. Style: premium botanical studio macro, realistic water droplets, very shallow optical focus, professional upper-left lighting, restrained motion. Nominal sequence length: **50 seconds** using direct cuts. Timeline overlaps reduce runtime.

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
- Generate only the missing source image for the first clip. For later clips, use the preceding saved endpoint as the next reference; create a new still only when the transition cannot be reached plausibly.
- Run one clip at a time because each next input depends on the actual preceding output.
- Check prompt, reference, aspect ratio, and 10-second setting before submitting.
- Never rerun an unchanged prompt. For a failed clip, record the defect, change only the relevant prompt or reference, and allow at most one targeted retry before revising the scene plan.
- Keep a checkpoint after every clip: scene ID, prompt version, source image, video asset, measured runtime, endpoint image, visible credit use, QA notes, and next scene.
- Existing membership generations are authorized for this pilot. Do not purchase top-ups, upgrades, or another subscription without explicit user authorization. Record usage only when shown in the account.

## Transition chain and current observations

The prompt book remains authoritative for the authored transition cues. Preserve each entry/exit shape, color, focus, and lighting cue where the generated footage allows it. Use an editor-side match cut or short dissolve when the saved endpoint differs; count any overlap in the final duration.

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
