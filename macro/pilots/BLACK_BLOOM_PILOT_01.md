# BLACK BLOOM · Pilot production 01

**Status:** Five 10-second clips are chained contiguously on `Black Bloom Pilot 01` from 00:00 to 00:50. BB-003 uses its focused retry, BB-004 uses the corrected isolated-flower render, and BB-005 closes on a fade to black. All five endpoints are saved in My AI Images. The timeline project is saved; full-sequence quality review remains.

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

The editor frame-save and library-reuse steps were verified across BB-001→BB-002→BB-003. BB-003 (`d7b72c78-d88c-4d95-9aa1-b83ab6e98392`, 3.17 MB) rendered at 10 seconds / 1920×1080 from `BB-002_ORCHID_LAST_FRAME_10S.png`, then was added contiguously at 00:20–00:30. The opening matches the violet droplet. Later frames show cream layered petal forms, but remain soft focus and the rose identity is only partly legible. `BB-003_ROSE_LAST_FRAME_10S.png` (545.04 KB) was saved and confirmed in My AI Images. Do not propagate this soft endpoint as a quality reference without review; consider an editor-side match cut into BB-004’s amber crescent.

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


### BB-003 targeted retry
A single targeted retry was submitted from `BB-002_ORCHID_LAST_FRAME_10S.png` with explicit instructions to keep a recognizable layered ivory rose in focus. VideoExpress reported successful completion for job `8ebacb3e-4a65-496f-b12c-357270cf3eb5`, but the file was not exposed in the library’s `My AI Videos` or `Videos` folders during retrieval. It has not been visually reviewed or added to the timeline. Do not generate another retry; retrieve and inspect this candidate first.


### BB-004 render review
Two completed 10-second, 1920×1080 renders appeared in **Media Library → My AI Videos** after the creator was closed. The 3.88 MB preview shows rose and orange calendula-like tissue visibly overlaid around 00:06. The 3.35 MB preview holds the rose longer, then begins introducing an orange petal edge, but did not present a clearly resolved calendula in the observed preview. Neither candidate was added to the timeline or used as an endpoint. Two generation identifiers were observed in the creator (`18ce2235-8041-4ce5-b6fd-3f1f274af87a`, `bfb5d5dc-4cee-4d49-9e08-ed54bcac3b0d`), but the UI did not expose a reliable mapping from those IDs to the two files. Revise the BB-004 prompt to request a distinct calendula cut/reveal with one non-overlapping specimen before another generation.

### BB-004 targeted correction
After rejecting two rose/calendula overlay candidates, one revised render was submitted with an explicit full-black separation and a single flower reveal. VideoExpress job `9725abe9-0160-4b10-a305-770a5f2ef303` completed as a 10-second, 1920×1080 file (2.36 MB). Preview at 00:02 shows a single orange flower on black; at 00:06 the radial petal grooves are clear and no rose overlaps it. At 00:10 the subject has closed into a small, dark orange-green bud rather than the planned amber bokeh point. The clip was added at 00:30–00:40, its endpoint was saved as `BB-004_CALENDULA_LAST_FRAME_10S` to My AI Images, and `Black Bloom Pilot 01` was saved. BB-004 is a provisional continuity pass; assess the BB-005 opening against this actual endpoint.

### BB-005 final clip
Job `47376f6e-b3ce-445b-9829-4e270846ae0e` rendered as a 10-second, 1920×1080 file (1.39 MB), sourced from `BB-004_CALENDULA_LAST_FRAME_10S.png`. Preview at 00:00 matches the saved dark orange-green bud, around 00:05 shows a recognizable burgundy dahlia against black, and 00:10 is nearly black after the planned fade. Added contiguously at 00:40–00:50. Endpoint `BB-005_DAHLIA_LAST_FRAME_10S` saved to My AI Images. The project now contains five 10-second clips / 00:50 and is saved.