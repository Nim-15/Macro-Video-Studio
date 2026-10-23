# BLACK BLOOM · Pilot production 01

**Status:** workflow preflight verified; two BB-001 tests and one chained BB-002 test render completed. BB-001 produced a verified 10-second clip and saved endpoint. BB-002 rendered at 10 seconds from the BB-001 saved endpoint; its new endpoint was saved and selected in the next prompt form. BB-002 needs visual review because the orchid is not clearly recognizable. BB-003–BB-005 have not been generated.

## Goal
Produce five connected 10-second macro clips with intentional entry and exit transitions on a pure black background. Style: premium botanical studio macro, realistic water droplets, very shallow optical focus, professional upper-left lighting, restrained motion. Nominal sequence length: **50 seconds** using direct cuts; timeline dissolves reduce runtime by their overlap.

## Verified VideoExpress route
Use **Create Video From Prompt** for the 10-second target. In Advanced Mode, enable **Manual Video Length, sec** and set it to **10**. The BB-001 prompt-mode test played at 0:10 / 0:10 in 16:9 at 1920×1080.

For each dependent clip, use the preceding clip's saved last frame as the next input image:
1. In My AI Videos, open the finished clip's context menu and choose **Add to Timeline**.
2. Use the finished clip's context menu → **Save Last Frame**, name it `BB-00N_SUBJECT_LAST_FRAME_10S`, and confirm it appears in **My AI Images**. This avoids seeking to the exact timeline boundary, which can show black after the clip ends.
3. Start **Create Video From Prompt**. Choose **Use from Library → My AI Images** and select the previous scene's saved endpoint.
4. Confirm the correct image is visible, set 16:9 and **Photorealistic (Cinematic)**, enable Advanced Mode and Manual Video Length = 10, and replace both sample prompts.
5. State in the image/video prompt that the selected image is the exact opening composition. Describe only plausible motion and the planned exit state. Do not ask the model to morph one flower species into another.
6. Generate one clip. When complete, play it and verify actual runtime, opening continuity, visual stability and exit frame. Add it to the timeline, save its endpoint, and continue to the next scene.

The editor frame-save and library-reuse steps were verified for BB-001. BB-002 then rendered from the selected BB-001 endpoint, was added directly after BB-001 on the timeline, and its `BB-002_ORCHID_LAST_FRAME_10S.png` endpoint was saved via **Save Last Frame** and selected in a new prompt form. The clip held the violet droplet palette, but the orchid did not become clearly recognizable; the ending also resolves to a soft lilac droplet. For BB-003, explicitly request a recognizable ivory rose petal edge and a controlled focus pull from this saved droplet reference. Review before spending the next generation.

## Generation discipline
- Use assets already present in My AI Images/My AI Videos before creating replacements.
- Generate only the missing source image for the first clip. For later clips, reuse the preceding saved endpoint as the starting reference; create a new still only when the next scene cannot be reached with a controlled, plausible visual transition.
- Run one clip at a time because each next input depends on the actual preceding output. Do not queue dependent scenes in advance.
- Review each prompt and selected reference before submitting. Catch wrong aspect ratio, placeholder text, incorrect frame, wrong species, or a non-10-second setting before rendering.
- Never rerun an unchanged prompt. For a failed clip, record the specific defect, change only the relevant prompt or reference, then allow at most one targeted retry before revising the scene plan.
- Keep a checkpoint after every completed clip: scene ID, prompt version, source image, video asset, measured runtime, last-frame asset, observed credit use if exposed, QA observations and next scene. Prefer the Media Library's **Save Last Frame** action over frame-by-frame timeline seeking.
- Existing membership credits may be used for this pilot. Do not purchase top-ups, upgrades or another subscription without explicit user authorization. Track usage where the account exposes it.

## Transition chain and scene order
The prompt book remains authoritative. Preserve each authored entry/exit shape, color, focus and lighting cue:

1. **BB-001 Iris:** iris detail and left-third droplet → soft violet highlight on left third.
2. **BB-002 Orchid:** open on the violet highlight; resolve into orchid detail → pale lilac glint near upper center.
3. **BB-003 Rose:** enter on the glint; resolve into ivory rose petal → creamy crescent at right.
4. **BB-004 Calendula:** enter on the crescent; resolve into amber petal → small amber bokeh lower center.
5. **BB-005 Dahlia:** enter on the amber point; resolve into burgundy petal → stable dark silhouette/fade.

If generated endpoint and next opening do not match, use an editor-side match cut or short dissolve guided by the continuity card. Keep the subject transition physically plausible; avoid literal flower morphing. Count all overlaps in final timing.

## Pilot review
Rate each clip 0–5 on botanical realism, water physics, camera stability, lighting continuity, entry/exit match and temporal stability. Reject obvious anatomy defects, floating droplets, conspicuous morphing, flicker or motion jumps. Review every clip before expanding to the 60-minute workflow.

## Run records
Update `pilot_state.example.json` (or a project-local copy) after every clip. Record measured durations and actual credit use only when visible in the account. Planning files do not represent an Artistly/VideoExpress API integration; keep credentials out of this repository.
